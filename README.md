# Ageing-Peer-Communities

## *Table of Contents*
+ Overview   
+ Data Prep  
+ Scenario One
    + *Use K-Means Clustering to cluster off CBSAs and Counties based on change in elderly (65+) population share and total..... from two American Community Survey 5-Year Estimates.*  
+ Scenario Two  
    + *Use a Linear Regression algorithm to find our peers for predicted elderly population share growth based on percent change of the total population for all CBSAs. This scenario uses 10 years of ACS 1-Year Estimates, and we stick to CBSAs so that the 1-Year Estimates are more reliable.*
  +

## Overview

This repository hosts a walkthrough of our process to determine peer communities based on age and population data. Some datapoints we are concerned with include the size and share of our ageing community, how this compares to other population groups, and where our peers are across a variety of geographies. This project is a prototype for approaching different strategies for finding peer communities using different kinds of data. In light of this, the format has shaped into a collection of scenarios. Find introductions to these scenarios and notebook structure below.

## Data Prep

In order to carry out this set of analyses, a number of different dataframes need to be prepped and exported. While we will be visualizing different parts of the scenarios geographically, we won't be bringing any shapefiles into the file prep because it takes less memory to clean data and export it as a csv and then quickly join the Census Tiger files when they are needed further down the line. The dataframes that are prepped are listed below:  

+ *Prep Time Series Two Five Year Estimates CBSA Level:* This file contains API calls that can be updated to reflect the most recent 5 Year Estimate and the previous, non-overlapping Estimate, for population by age and sex as well as home value (an indicator for area wealth), and any other factors that you want to add. This notebook goes through joining these dataframes together, cleaning the data, summing groups together that represent ages under 18, ages 18-64, and ages 65+. Finally, real change, percent change, and change in total population share are calculated for these groups respectively. Males and females are summed together to create total population, however this could be disaggregated. The data is also available by race, so this could be disaggregated as well.

+ *Prep Time Series Two Five Year Estimates County Level:* This notebook is a duplicate of the CBSA notebook of the same name, adjusted for county level geography and the data cleaning is altered to reflect this.

    + *The ACS 5-Year Estimates allow us to have a high level of confidence when we look at the numbers, and this format is used for clustering scenarios.*

+ *Prep Decade of One Year Estimates CBSA Level:* This file contains API calls that can be updated to reflect the last decade of One-Year Estimates for population by age and sex as well as home value (an indicator for area wealth), and any other factors that you want to add. This notebook goes through joining these dataframes together, cleaning the data, summing groups together and calculating change measures.

+ *Prep Decade of One Year Estimates County Level:* This notebook is a duplicate of the CBSA notebook of the same name, adjusted for county level geography and the data cleaning is altered to reflect this.

    + *The ACS 1-Year Estimates allow us to examine year over year shifts instead of looking at entire 5-year periods. While this data is a relatively small sample size, especially for smaller geographies like Counties, it can still be used to reliably examine trends. This data is used to perform linear regressions and find our peer communities by projecting patterns.*



## Scenarios  

### *Linear Regression for Dependent and Independent Variables*

+ Use one decade of one-year ACS estimates to examine the relationship between population growth of various groups and with area wealth. Create visualizations of these relationships.   
+ Select a couple pairs of variables with a close linear relationship.
+ Use `sklearn` to create a linear regression and then project share of elderly population and total elderly population 5 and 10 years into the future.  
+ Break these projections into percentiles and isolate the percentile of geographies in the same category as our geography in question.  
+ Map these geographies and give example of other sorts of data or information you can examine about our *peers*.

### *K-Means Clustering for Two - Four Variables*

### *Hierarchical Clustering for Two - Four Variables*
