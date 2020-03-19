# COVID-19 Data sets
The repository contains the data set used for modeling spread of COVID and impact of control measures in Germany. We first list the resources from where we have collected the data for this research. We follow it up with the data dictionary explaining the dataset used in our model. Some of the data sets which need approval from the provider firm could NOT be umade available.

## Data Sources

The data dictionary and the different sources: 
1. Train Routes (to and within Germany): <a href="https://www.bahn.de/p/view/mdb/kursbuch/mdb_305019_frankfurt_main_hbf_1920_an_heft_115221.pdf">here</a>
2. Bus Routes (to and within Germany): <a href="https://en.wikipedia.org/wiki/2020_coronavirus_pandemic_in_Germany">here</a>
3. Air Routes (to and within Germany and needs approval for data access): <a href="https://opensky-network.org">here</a>
4. Aircraft information: <a href="https://opensky-network.org/datasets/metadata/">here</a>
5. Airport information : <a href="https://openflights.org/data.html#airport">here</a>
6. State wise COVID infections in Germany: <a href="https://en.wikipedia.org/wiki/2020_coronavirus_pandemic_in_Germany">here</a>
7. Total number of tests conducted (world wide): <a href="https://ourworldindata.org/coronavirus\#current-covid-19-test-coverage-estimates">here</a>
8. State wise Demographics information (Germany): <a href="https://www.citypopulation.de/en/germany/">here</a>
9. Data for South Korea: <a href="https://ourworldindata.org/grapher/daily-cases-covid-19-who?time=1..52&country=KOR">here</a>
10. Data for South Korea: <a href="https://ourworldindata.org/grapher/daily-cases-covid-19-who?time=1..52&country=KOR">here</a>

## News Articles
1. Travel restrictions in Germany: <a href="www.bbc.com/news/world-europe-51897069">here</a> and <a href="www.dw.com/en/coronavirus-germany-implements-non-eu-travel-ban/a-52802039">here</a>
2. Footfall has fallen in major cities post corona outbreak: <a href="www.economist.com/graphic-detail/2020/03/14/foot-traffic-has-fallen-sharply-in-cities-with-big-coronavirus-outbreaks">here</a>
3. Project baseline by Verily: <a href="">here</a>
4. Airlines cancelling more flights to Europe: <a href="techcrunch.com/2020/03/12/airlines-start-cancelling-more-flights-from-europe-as-new-restrictions-go-into-effect/">here</a>
5. Italy under lock down: <a href="graphics.reuters.com/HEALTH-CORONAVIRUS-ITALY/0100B5J33XY/index.html">here</a> 
6. Spreads person-to-person (cars): <a href="www.cdc.gov/coronavirus/2019-ncov/prepare/transmission.html?CDC_AA_refVal=https\%3A\%2F\%2Fwww.cdc.gov\%2Fcoronavirus\%2F2019-ncov\%2Fabout\%2Ftransmission.html">here</a>
7. Italy’s aging population is more susceptible to corona: <a href="www.wsj.com/articles/italy-with-elderly-population-has-worlds-highest-death-rate-from-virus-11583785086">here</a> 
8. What 1918 pandemic has taught us: <a href="www.popsci.com/story/health/coronavirus-1918-flu-pandemic/?utm_medium=syndication&utm_source=smartnews">here</a>


## Data Dictionary
1. **demographics**.csv contains demographics data for the different states.
   - Column A: name of the states
   - Column B: variable data field
   - Column C: count of population for the corresponding data field

2. **flight-updated.csv** contains flights data. *Only to be used for Academic purpose*.
   - Column A: icao codes for the flights
   - Column B: UNIX flight first seen
   - Column C: departure airport
   - Column D: UNIX flight last seen
   - Column E: airport airport
   - Column F: UNIX time for day (we can use any one of Column B, D, or F for the day)
   - Column G: departure country
   - Column H: arrival country
   - Column I: departure state (if the airport is not in Germany, it says FOREIGN-COUNTRY)
   - Column J: arrival state (if the airport is not in Germany, it says FOREIGN-COUNTRY)

3. **infected-updated.csv**contains data on day-wise infections in various countries from where international flights arrived to Germany. We know the corresponding German states in the flight-updated file
   - Column E: total cases reported
   - Column F: total deaths
   - Column G: Country
   - Column I: Relative Days: December 1, 2019 is day 0, Dec 1 is day 1 and so on. This column can be used if we do not want to deal with string data of date.
