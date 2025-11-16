# project2

# Air Quality Data Analysis (2018-2020)

## Project Overview
This project analyzes daily air quality measurements for three major pollutants (CO, PM2.5, and O3) across three years (2018-2020). The analysis includes data cleaning, processing, and visualization of temporal patterns in air pollution concentrations.

## Data Description

### Input Files
`AQ_2018.csv`: Air quality data for 2018
`AQ_2019.csv`: Air quality data for 2019  
`AQ_2020.csv`: Air quality data for 2020 (January-April only)

### Variables
Date: Date of measurement
Daily Max 8-hour CO Concentration: Maximum 8-hour average carbon monoxide concentration (ppm)
Daily Mean PM2.5 Concentration: Daily mean particulate matter 2.5 concentration (µg/m³)
Daily Max 8-hour Ozone Concentration: Maximum 8-hour average ozone concentration (ppm)

## Data Processing Steps

1. Converts dot-separated column names to space-separated format for better readability
2. Parses dates using `lubridate` package
3. Calculates daily averages for days with multiple measurements
4. Removes any duplicate rows in the dataset
5. Sets negative concentration values to zero (addresses measurement errors)

## Visualizations

### Plot 1: Monthly CO and O3 Concentrations with Confidence Intervals
X-axis: Month (Jan-Dec)
Y-axis: Pollutant concentration

### Plot 2: Monthly PM2.5 Concentrations by Year
X-axis: Month (Jan-Dec)
Y-axis: PM2.5 concentration (µg/m³)

## Required R Packages

```r
library(dplyr)
library(lubridate)
library(ggplot2)
library(tidyr)
library(here)
```