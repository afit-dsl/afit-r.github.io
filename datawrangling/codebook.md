---
layout: tutorial
title: Review the Codebook
permalink: /codebook
---

A codebook is a technical description of the data that was collected for a particular purpose. It describes how the data are arranged in the computer file or files, what the various numbers and letters mean, and any special instructions on how to use the data properly. Like any other kind of "book," some codebooks are better than others. The best codebooks have:

1. Original source of the data:
    - Citation of data base or study that original collected the data.
    - Original intent of the data collection.
    - If data collection was a result of a study - who did it, why they did it, how they did it.
2. Sampling information
    - Where are the data generated.
    - What is the data collection process - are their multiple data scrubbing processes or are the data considered "raw".
    - What population are the data collected from.
    - How was the sample drawn.
    - What was the response rate.
3. Details about the data such as:
    - Variable name: The name or number assigned to each variable in the data collection.
    - Variable label: A brief description to identify the variable for the user.
    - Question text: Where applicable, the exact wording from survey questions. ["In general, would you say your health is . . ."]
    - Values: The actual coded values in the data for this variable. [i.e. 1, 2, 3, 4, 5]
    - Value labels: The textual descriptions of the codes if the "true" value differs from the numeric values recorded. [i.e. Excellent, Very Good, Good, Fair, Poor]
    - Summary statistics: Number of observations, record length, number of records per observation, etc.
    - Missing data: Where applicable, the values and labels used to code missing data. [i.e. -99 is commonly used for missing values in weather data]
4. Structure of the data: hierarchical/aggregated, centralized or disparate data sources that need to be, or have been, merged, etc.
    
R comes with many built-in data sets. To see the 100+ data sets that come with R just type `data()` in your console and you'll see a list that looks like:

<center>
<img src="/public/images/dataWrangling/built-in-data.png" alt="Built-in Data" style="width: 75%; height: 75%">
</center> 

For any of these built-in data sets you will find the "codebook," the technical description of the data by typing `?` and then the name of the data set. This will bring up the "codebook" in your Help console. For instance, `?mtcars` will provide you with the technical information regarding the `mtcars` built-in data set. 

Getting the codebook for data that you are importing and using for your own analysis is a little more difficult. If you are using organizational data at your employer, this will likely require you to request the codebook from the database engineers or other folks that are intimately familiar with the data source. This seemingly simple task will surprise you by illustrating how few people truly understand the technical details underlying organizational data. If you are using publicly available online data, you may need to do some searching to identify the data. Sometimes codebooks are obviously and explicitly linked on the website, other times you have to do some digging to find the codebook. Some examples of codebooks follow:

- NOAA Hourly Precipitation: [[Data](https://catalog.data.gov/dataset/u-s-hourly-precipitation-data)] [[Codebook](https://www1.ncdc.noaa.gov/pub/data/cdo/documentation/PRECIP_HLY_documentation.pdf)] 
- Consumer Expenditure Survey: [[Data](https://www.icpsr.umich.edu/icpsrweb/ICPSR/series/20)] [[Codebook](https://www.icpsr.umich.edu/icpsrweb/ICPSR/ssvd/series/20/variables)]
- College Scorecard:  [[Data](https://catalog.data.gov/dataset/college-scorecard)] [[Codebook](https://collegescorecard.ed.gov/data/documentation/)]
- Consumer Complaints: [[Data](https://catalog.data.gov/dataset/consumer-complaint-database)] [[Codebook](https://cfpb.github.io/api/ccdb//)]

The important thing to remember is that you need to identify the documentation that explicitly tells you about the data you are working with. If not then in your analysis you need to state what the implied meaning of the data is; however, you should also state that ambiguity may exist if a codebook can not be identified.  With your final project, I expect you to explain the describe the source data you analyze and provide a citation (or URL link if possible) to the source database and codebook.

## Exercise

This [site](http://academic.udayton.edu/kissock/http/Weather/citylistUS.htm) contains files of daily average temperatures for 157 U.S. cities. Identify the following:

1. Where does this data originate?
2. How often are the data collected?
3. How do they compute the "average daily temperatures"?
4. How are missing data flagged in these data sets?
5. Do they provide options for imputing missing data?
