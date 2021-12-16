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

![JuneTempPlots](Resources/JuneTempPlots.png)

After reviewing the plot above we felt that the visual was a nice touch but, as way to help quantify the visual we decided to utilize the .describe() function found in the pandas library to provide a way for the investor(s) to quickly review the min, max, means, etc.

* Below is the same 'June Temperature Query' calculating and formatting the data in a central tendency format.  

![JuneTempStats](Resources/JuneTempStats.png)


### Deliverable 2: December Weather Analysis Process

The second requested deliverable of W. Avy's request was as we did for June, retrieve data from the dataset that would focus on the temperatures during the month of December.  This would allow the investors to see how the weather during the summeer month of June would compare to the winter month of December.  Below is the query that was constructed to retrieve the temp data from the weather recording stations throught Oahu.

* Below is the 'December Temperature Query' that pulls back all temperatures recorded during the month of December from all recording stations over multiple years.  

![DecemberQuery](Resources/DecemberQuery.png)

* Please review the plot below resulting from the 'December Temperature Query'

![DecTempPlots](Resources/DecTempPlots.png)

For consistancy, Just as we did with June's data, after reviewing the plot above we decided to utilize the .describe() function again to provide a way for the investor(s) to quickly review the min, max, means, etc.

* Below is the same 'December Temperature Query' calculating and formatting the data in a central tendency format.  

![DecTempStats](Resources/DecTempStats.png)

### Summaray of June and December Analysis

## Additional Analysis

