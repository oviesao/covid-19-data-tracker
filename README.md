# COVID-19 Data Tracker

## Project Overview

This project tracks COVID-19 statistics across different countries using data from March 9, 2023. It reads a CSV file, processes it using R, and generates visualizations for insights on confirmed cases, deaths, and recoveries. The analysis is presented through graphs and summary reports.

The data used comes from [CSSEGISandData's COVID-19 Data Repository](https://github.com/CSSEGISandData/COVID-19), maintained by the Johns Hopkins University Center for Systems Science and Engineering (JHU CSSE).

## Features

- **COVID-19 Data Import:** Reads COVID-19 data from a CSV file (`03-09-2023.csv`).
- **Data Analysis:** Analyzes total confirmed cases, deaths, and recoveries by country.
- **Visualizations:** Plots the top 10 countries for confirmed cases, deaths, and recoveries.
- **CSV File Updates:** Supports manual updates to the CSV file for continued tracking.

## Files and Folders

- **analysis.R**: Main R script for analyzing and visualizing COVID-19 data.
- **data/**: Folder containing the raw CSV data files.
- **plots/**: Folder containing the generated visualizations.
- **README.md**: Project documentation.

## How to Use

 **Install Dependencies:**
   - You will need to have `dplyr` and `ggplot2` packages installed in your R environment.
   
   To install, run the following commands in R:
   ```R
   install.packages("dplyr")
   install.packages("ggplot2")
