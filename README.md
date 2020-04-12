# Predictors of Lake Level Changes in Lake Tahoe, CA

## Summary

This repository is for Duke's Nicholas School of the Environment Data Analytics Course (ENVIRON 872). The associated project explores how water level changes from October 1, 1957 to April 10, 2020 in Lake Tahoe, California and explores possible atmospheric reasons behind the changes in water level. Time series analysis and linear regression models will be used to determine conclusions. 

## Investigators

Nikki Shintaku, Nicholas School of the Environment, Duke University, nikki.shintaku@duke.edu 

## Keywords

Lake Tahoe, precipitation, air temperature, weather, climate, climate change, snow, California, time series, linear regression, lakes, water level

## Database Information

Data on Lake Tahoe gage height (or water level) was downloaded from the USGS Water-Quality Data for the Nation website (https://waterdata.usgs.gov/nwis/dv?cb_00065=on&format=html&site_no=10337000&referred_module=sw&period=&begin_date=1990-04-30&end_date=2020-04-01). More information can be found here: https://waterdata.usgs.gov/nwis/qw. 
From the Data homepage, the following selections were made:
* Daily Data
* Site Number (Site Identifier)
* Site Number - 10337000
* First date: 1957-10-01 Last date: 2020-04-10 (Retrieve data for the date range)
* Tab-separated data (Output Options)

csv file is saved as 'USGS_Tahoe_gage_height.csv'

This data was accessed on April 11, 2020. 

Data on precipitation, snow fall, and air temperature was downloaded from NOAA National Centers for Environmental Information (https://www.ncdc.noaa.gov/cdo-web/datasets#GHCND).
From the Data homepage, the following selections were made:
* Daily Summaries 
* Zip Code (Search for)
* 96145 (Enter a Search Term)

Data for TAVG, TMAX, TMIN, PRCP, SNOW and SNWD were downloaded. csv file is saved as 'NOAA_Tahoe_climate_data.csv'

This data was accessed on April 3, 2020. 

## Folder structure, file formats, and naming conventions 

This repository contains the folders:
* Data
* Code
* Output

The Data folder contains two subfolders: Raw and Processed. The data folder and subfolders contain files 
in .csv format. 

The Code folder contains files in .Rmd format. 

The Outout folder contains files in .csv or .pdf formats. 

Files in .csv are datasets in table format that are uploaded into the R markdown for data analysis purposes. All processed datasets in R will be saved as a .csv file. There is separate .Rmd files that contain code for each step of the data analysis. The final report for the repository is saved in .pdf format for an easy read. 

Files are named according to the following naming convention: 'databasename_location_details.format', where:

**databasename**  refers to the database from where the data originated

**location** is where the data station was located

**details** is a description of the data

**format** is file format (e.g., .csv, .txt, .pdf)

## Metadata

* USGS_Tahoe_gage_height.csv
  + agency_cd: USGS 
  + site_no: A unique number that corresponds to the site identifier or gage station.
  + datetime: month/day/year
  + gage_height: numeric value, gage height recorded in feet. Current lake elevation is measured at 6,220 feet + current gage height measurements will give the changes in lake level
  + qual_code: data-value qualification code where A is Approved for publication (processing and review completed), P is Provisional data subject to revision, and e is value has been estimated

Information gathered from https://waterdata.usgs.gov/nwis/qw

* NOAA_Tahoe_climate_data.csv
  + STATION: A unique code within the zip code identifying the station from which measurements were taken.
  + NAME: Name of the station
  + LATITUDE
  + LONGITUDE
  + ELEVATION: Elevation above mean sea level (tenths of meters)
  + DATE: month/day/year
  + PRCP: Daily precipitation in inches
  + SNOW: Daily snowfall in inches
  + SNWD: Daily snow depth in inches
  + TAVG: Daily Average Temperature in degrees fahrenheit
  + TMAX: Daily Maximum Temperature in degrees fahrenheit
  + TMIN: Daily Minimum Temperature in degrees fahrenheit
  
Information gathered from: https://www.ncdc.noaa.gov/cdo-web/datasets

## Scripts and code

*To Be Updated*

## Quality assurance/quality control

Outliers in the data will be identified by visualization, and if deemed unnescessary they will be removed. Any flagged data such a value marked as estimated will be noted. In addition, if needed, missing values may be interpolated to run a complete time series on the data. Values ranges will also be checked to ensure they are within sensible range of the instrument measurements and the property being measured. 
