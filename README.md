# Coursera-Getting-and-Cleaning-Data

##Introduction
This is for the Coursera course called "Getting and Cleaning Data." In this README.md, you will find the information on the R script used for analysis, the codebook, and the raw data.

##Script

The script is saved in this repository as run_analysis.R, which will merge the test and training sets together. Be aware that:

1. The UCI HAR Dataset must be extracted
2. Working directory must be set to the extracted "UCI HAR Dataset" folder

The script will create a tidy data set containing the means of all the columns per test subject and per activity. This tidy dataset will be written to a tab-delimited file called tidy.txt, which can also be found in this repository.

##Codebook

The codebook describes the variables that occur as a result of transformation in the script.

##Data

The data can be dowloaded as a zip file from "https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip"
