# COVID19-in-Midwest

This project aims to identify some trends of current Covid-19 spread specifically in the upper midwest of the US. The states observed in this analysis are Missouri, Michigan, Illinios, Indiana and Ohio. 

As of producing this analysis we are nine months into the global Covid-19 pandemic, and the US has struggled since its initial case to manage both infections and the death toll. Using current (mid September 2020) infection data we wished to unravel any connection between population statistics and infection rates using several criterion. 

The first criterion was indicence rates, and comparing Covid hotspots to population. While it is expected that there will be a greater number of cases in large population areas we wanted to identify any counties or states that had particular issue with infections relative to the average. 

The second criterion we chose to observe was any relationship between mean income of specific counties to their infections or death rates. We wanted to see if more wealthy counties were able to afford more agile reactions to the spread of infection, and if poorer counties faced a greater fatality rate.

Finally we obtained self-reported mask wearing behavior from the middle of July from a New York Times requested survey of 250,000 people in the US. This data gave an approximate percentage of people's mask wearing behavior in public. This was a five-choice scale from NEVER to ALWAYS. We wanted to obeserve if places that had better mask-wearing habits had lower Covid infection rates.

Overall these topics will be compared state by state to identify if any state had more positive results in terms of infections or deaths.

## Results
---
More more specific results graphical representations can be found in the 'png's' folder within this repository. Running the given code will also replicate our initial findings.

When observing general infections in the upper midwest we found that indeed the larger number of infections correlated with large population centers. This was true for all states. However when we obersved infection rates (total cases per 100,000 residence) There were many rural counties that had higher rates than expected, and most of the cities were actually lower than average with respect to population. The infection rates were more uniform than expected, which was suprising. No state observed was particularly different in its infection rates than any other.

The mask data was particularly interesting. To get a more general understanding of the spread of answers per county we reduced the five percentages measured to a single percentage. This value approximated the odds that a person in that county would wear a mask. This percentage was obtained through linear interpolation assuming each possible answer on the survey was equidistant. We found that mask usage tended to be higher in counties with greater populations. This was suprising as it suggests that masks do not seem to reflect to intended results within the infection numbers. We believe however that this relationship is muddled by many factors. The first factor is that it makes sense that mask usage would be higher in areas (such as cities) where the risk of infection may be higher. In addition this analysis does not take into account the non-linear nature of viral spread. Thus one would expect without mask usage there may be exponentially more cases in potential hotbeds. A more proper analysis of the usefulness of mask wearing would be oberving time series data of the counties that wear masks more often against those that do not. 

Future goals of this project would be to compare these factors over time, to see if changes in the rate of infection were affected by population statistics. The infection data was cumulative, thus some cities/states may have had a rough start but due to specific policies thier rates may have changed over time. 

Many factors play a role in the spread and contraction of Covid-19. While the data presented here was exploritory the psuedo-randomness of the infection behavior is alarming. More data and presice statistical models should be used to better plan for and identify a safe path forward. 

Stay safe out there.

## Data Used in our Analysis
---
This analysis used the following sources for our analysis:

[2018 ACS5 US Census Data](https://api.census.gov/data/2018/acs/acs5.html)

[Johns Hopkins Covid-19 Database](https://github.com/CSSEGISandData/COVID-19)

[New York Times Mask Survey Data](https://github.com/nytimes/covid-19-data)



## Tips to run your own Analysis!
---
We invite all who are interested in generating and understanding covid data to use this code if they so please. The 

You will need a US census API key to run this anlysis.

If you wish to run the analysis with data from other timepoints, the csvs to do so can be found at the John's Hopkins link above. 

All data for all US states are actually loaded into our initial dataframe. If you wish to view other counties throughout the country that data is availible to use! Each state within the set can be searched for through thier specific FIPS code.

### Python Libraries used
---
numpy

pandas

matplotlib

requests

census

plotly.express