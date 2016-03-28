# Getting and Cleaning Data - Course Project

This repository contains R Code and files related to the course assignment. The R Code relies on the data that is processed is in the same folder, is not compressed and without names altered.

`run_analysis.R` contains the Code to do the following functions in R Studio:
1.  Download the dataset (if it does not already exist in the working directory)
2.  Load the activity 
3.  Load the Training and Test Datasets; keeping only columns with a mean or standard deviation
4.  Load the Activity and Subject data for both datasets, and merge columns with the dataset
5.  Merge both datasets
6.  Convert the `Activity` and `Subject` columns into factors
7.  Create a tidy dataset with an average (mean) value of each variable for each subject and activity pair.

The R Code can be launched in RStudio by just importing the file. 

`CodeBook.md` explains the transformations performed and the resulting data and variables.

The final file `tidy.txt` is uploaded in the course project's form.
