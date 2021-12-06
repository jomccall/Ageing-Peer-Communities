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

+ *Prep Time Series Two Five Year Estimates CBSA Level:* This file contains API calls that can be updated to reflect the most recent 5 Year Estimate and the previous, non-overlapping Estimate, for population by age and sex as well as home value (an indicator for area wealth), and any other factors that you want to add.

## Scenarios  

### *Scenario One*
