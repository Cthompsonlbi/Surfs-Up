# Surfs-Up
Module 9 Challenge

## Overview of Project

Apply skills aquired ind Advanced Data Storage and Retrieval to access data using SQLite, Flask, Python and libraries to access specific data, query subsets of data from the tables and analyze this data to provide specific information and analysis that will assist investors with decision making.

### Purpose

Back from a recent vacation to Hawaii, the protagonist would like to move to Oahu to open a Surf and Shake shop so that they may live there full time. Although this individual has some money to invest, they quickly realize that additional investors will be needed to get this venture off the ground.  Consulting with a local Hawaiian investor W. Avy, he request for very specific data regarding the weather in Oahu.  Our analysis will provide W. Avy and other potential investors with the information that they need to make an informed decision on whether thhis investment is the right one for them.  After analyzing the weather data over several years in Oahu, W. Avy requested the analysis to be conducted on specific months. These months are June and December.  The results of the weather analysis for the months of June and December can be found below.

## Results

### Deliverable 1: June Weather Analysis Process

One of W. Avy's request was retrieve data from the dataset that would focus on the temperatures during the month of June.  This would allow the investors to see how the weather during the summer month of June would compare to the winter month of December.  After importing all of the proper libraries and supporting files, below is the query that was constructed to retrieve the temp data from the weather recording stations throught Oahu.


* Below is the 'June Temperature Query' that pulls back all temperatures recorded during the month of June from all recording stations over multiple years.  

![JuneQuery](Resources/JuneQuery.png)

* Please review the plot below resulting from the 'June Temperature Query'

![JuneTempPlot](Resources/JuneTempPlot.png)

After reviewing the plot above we felt that the visual was a nice touch but, as way to help quantify the visual we decided to utilize the .describe() function found in the pandas library to provide a way for the investor(s) to quickly review the min, max, means, etc.

* Below is the same 'June Temperature Query' calculating and formatting the data in a central tendency format.  

![JuneTempStats](Resources/JuneTempStats.png)


### Deliverable 2: December Weather Analysis Process

The second requested deliverable of W. Avy's request was as we did for June, retrieve data from the dataset that would focus on the temperatures during the month of December.  This would allow the investors to see how the weather during the summeer month of June would compare to the winter month of December.  Below is the query that was constructed to retrieve the temp data from the weather recording stations throught Oahu.

* Below is the 'December Temperature Query' that pulls back all temperatures recorded during the month of December from all recording stations over multiple years.  

![DecemberQuery](Resources/DecemberQuery.png)

* Please review the plot below resulting from the 'December Temperature Query'

![DecTempPlot](Resources/DecTempPlot.png)

For consistancy, Just as we did with June's data, after reviewing the plot above we decided to utilize the .describe() function again to provide a way for the investor(s) to quickly review the min, max, means, etc.

* Below is the same 'December Temperature Query' calculating and formatting the data in a central tendency format.  

![DecTempStats](Resources/DecTempStats.png)

### Summaray of June and December Analysis

* For ease of reference, please see the central tendency information plotted above in a side by side format below.  

![centraltendencytemp](Resources/centraltendencytemp.png)

Based of the queries for June and December one will notice the following by comparing the outcomes:
  * Temperaturess are three degrees warmer for June than December
  * June max temp is two degrees warmer than December
  * The average temperature is also four degrees higher in June than in December
  * The min temperature is eight degrees cooler in December than compared to June.
  * The December bar plot above shows a greater concentration of temperatures at the 71-72 degree range, while June shows a wider range of temperature variations.

Soley based on these two queries and resulting output, there are not red flags as to whether or not a Surf and Shake shop could thrive based on temperature alone.  However, knowing that W. Avy had issues with past business ventures due to issues with weather, particularly precipitation, we believe it would be prudent to expand the analysis to account other factors.  That analysis can be found below.

## Additional Analysis

Apart from temperature, other issues that should be taken into consideration to gain a level of confidence if an investment in the Surf and Shake shop would be successful is a measurement of precipitation, particularly near the coast.  Focusing on temperature and percipitation near the coastal areas of Oahu would allow us to remove data acquired from areas that are not the target customers of the Surf and Shake shop. Catering to the surf and tourist community would mean that the shops locations would be closer to the coast and not in-land. Because of this, in-land weather data should be excluded from the data set so that the investors could get a more accuratae depiction of the weather in areas the shop tend to service. 

In order to complete this task, we would need to create a query that would return locations closer to the coast.  A simple way to do this for the Oahu dataset was to remove data acquired by stations in the upper elevations.  These higher elevations are located further away from the coast and based on their elevations their percipitation data and temperature data could vary significantly when compared to stations closer to sea-level.  Removing the data of stations located at higher elevations could provide a more accurate picture of what the weather is actually like for prospective Surf and Shake Shops.  To achieve this please see the queries created for June and December that removed weather stations that are at an elevation of 40 feet or higher.

* Query returning June temperature data from weather stations at elevations below 40ft.
 
![JuneElevQuery](Resources/JuneElevQuery.png)

* Query returning December temperature data from weather stations at elevations below 40ft.
 
![DecTempLowElevQuery](Resources/DecTempLowElevQuery.png)

Using the queries above, we are able to generate plots of June and December data that shows weather of locations that are more likely candidates for the Shake and Surf Shop and remove any contribution attributed by in-land stations, where the weather patterns may be different.

Below you will find plots showing the temperatures for June and December representing only locations that are closer to the coastal areas of Oahu.

![JuneTempLowElevPlot](Resources/JuneTempLowElevPlot.png)
![DecTempLowElevPlot](Resources/DecTempLowElevPlot.png)

Just as we did for Deliverables one and two, we used the .describe() function to return the central tendency calculations of temperatures but,  for the coastal locations only.

![JuneTempLowElevStats](Resources/JuneTempLowElevStats.png)
![DecTempLowElevStats](Resources/DecTempLowElevStats.png)

The one thing that W. Avy
* Query returning June percipitation data from weather stations at elevations below 40ft.
 
![JunePrcpLowEvelQuery](Resources/JunePrcpLowEvelQuery.png)

* Query returning December percipitation data from weather stations at elevations below 40ft.
 
![DecPrcpLowElevQuery](Resources/DecPrcpLowElevQuery.png)

Below you will find plots showing the percipitation levels for June and December representing only locations that are closer to the coastal areas of Oahu.

![JunePrcpLowEvelPlot](Resources/JunePrcpLowEvelPlot.png)
![DecPrcpLowElevPlot](Resources/DecPrcpLowElevPlot.png)

Finally, Just as we did for Deliverables one and two, we used the .describe() function to return the central tendency calculations for percipitation but, for only the coastal locations.

![JunePrcpLowEvelStat](Resources/JunePrcpLowEvelStat.png)
![DecPrcpLowElevStats](Resources/DecPrcpLowElevStats.png)

## Analysis of the Analysis

Although we were only supposed to propose two or three additional suggestions for analysis, we went ahead and completed the analysis by providing June and December data for coastal areas, the temperature of those coastal areas, and the percipiation levels for those areas.  This will help the investors feel more confident in their decision knowing that the data is cleaner and more relevant to the business opportunity.

After reviewing the data of the lower elevation coastal areas it is found that the weather in-land does not contribute significantly to the original data set.  The analysis is quite similar if the in-land weather stations are included or not.  The following are the observations made comparing the original analysis with the coastal only analysis:

* June average temperatures are only .5 degrees warmer when comparing original June temps (74.94) and coastal area June temps (75.45). The min and max temps remained unchanged.
* December average and minimum temperatures roughly the samne when comparing the two data sets. While the Max temp is one degree cooler for coastal areas (82.0) compared to the original data set (83.0)
* While referencing to the bar charts comparing June and December coastal area precipitation, December appears to have significantly wetter month than compared to June. However, by looking at the bar chart, it appears that 2010 as paricularly a wet year for 2010.  Looking at the central tendency plot could yield more accurate analysis.
* Comparing the central tendency of precipitation levels for the coastal locations during the month of June and December, the mean for December is higher than June but not significantly.  The delta observed could be due to the impact of 2010 high level of percipitation that skewed the data for December. The December Max of 4.94 is indicative of the high level of rain for 2010.

## Additional Analysis Opportunities

Further analysis will need to be done to help further zero an appropriate location if the investors would like to move forward.  Population analysis would be a complimentary data point that could help identify prime locations.  Having an analysis of area population size, demographics, income, and tourists influx will help identify primary locations to sustain such a business adventure. 
