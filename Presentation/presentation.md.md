presentation.md
Developing Data Products - Course Project
========================================================
author: Paolo Baglioni
date: Fri Apr 29 14:42:43 2016
transition: rotate
width: 1440
height: 900


Storm Database Analysis
========================================================
type: sub-section

This presentation is being created as part of the peer assessment for the coursera developing data products class. The assignment is geared toward ensuring the following concepts were well understood by the students

- **shiny** to build data product application
- **R-Presentation or slidify** to create data product related presentations

The Application
========================================================
type: sub-section
The application developed for the first part of the assignment is called **Storm Database Analysis** and is avalilable at: 
https://pbaglioni.shinyapps.io/developing-data-products-shiny/

The application allows the user to:
- Select the inputs like range of years or types of events. 
- Select the output to be displayed on the map, as a graph or as a table 
- Use the option to download the filtered data.


The Data
========================================================
type: sub-section
This application is based on the U.S. National Oceanic and Atmospheric Administration's (NOAA) storm database.

Dataset should be obtained from [here](https://d396qusza40orc.cloudfront.net/repdata%2Fdata%2FStormData.csv.bz2) and processed for the course project. This dataset is the same used for the Cousera's Reproducible Research Course.

Source code for ui.R and server.R files are available on the [GitHub](https://github.com/pbaglioni/developing-data-products).

Data
=====================
type: sub-section
Read Data

```r
library(data.table)
dt <- fread('events.agg.csv')
head(dt)
```

```
   YEAR   STATE  EVTYPE COUNT FATALITIES INJURIES PROPDMG CROPDMG
1: 1950 alabama TORNADO     2          0       15 0.02750       0
2: 1951 alabama TORNADO     5          0       13 0.03500       0
3: 1952 alabama TORNADO    13          6      116 5.45250       0
4: 1953 alabama TORNADO    22         16      248 3.07000       0
5: 1954 alabama TORNADO    10          0       36 0.60753       0
6: 1955 alabama TORNADO     8          5       27 7.58000       0
```



