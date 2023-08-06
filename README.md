# FileParser
A Python CSV file parsing script that accesses a file hierarchy of sensor data using the OS library to perform transformations for every file and combine rows from different files together

problem:
- a client has the sensor data stored in files titled by year from 1975 to 2023
- each year file has 8 different csv files for a total of 384 files.
- each file has a time series column as primary recording different parameters

Required:
1. transform the following columns in all files
  - extract the 3rd comma-separated value in the wnd column and divide it by 10 
  - extract the first comma-separated value in vis column
  - extract the first comma-separated value in tmp and divide it by 10 
  - extract the first comma-separated value in dew and divide it by 10
2. transform the data column
  - set the date frequency to 3 hours and fill in any missing dates leaving the sensors values as nulls
  - set the date format to India Kolkata
3. merge the November and December of a year with January of the next year file for all years