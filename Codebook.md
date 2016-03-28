# Codebook for Tidy Dataset

## Original Data

The original data comes from the smartphone accelerometer and gyroscope 3-axial raw signals, 
which have been processed using various signal processing techniques to measurement vector consisting
of 561 features. For detailed description of the original dataset, please see `features_info.txt` in
the zipped dataset file.

- [source](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip) 
- [description](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones)


### Conventions Followed

Processing code and dataset variable naming follows the conventions described in 
[Google R Style Guide](http://google-styleguide.googlecode.com/svn/trunk/Rguide.xml).

## Data Sets

### Raw Data Set

The raw dataset was created using the following regular expression to filter out required
features, eg. the measurements on the mean and standard deviation for each measurement
from the original feature vector set 

`-(mean|std)\\(`

This regular expression selects 66 features from the original data set.
Combined with subject identifiers `subject` and activity labels `label`, this makes up the
68 variables of the processed raw data set.

The training and test subsets of the original dataset were combined to produce final raw dataset.

### Tidy Data Set

The Tidy Data Set contains the average of all standard deviation and mean values of the raw dataset. 
Original variable names were modified in the follonwing way:

 1. Replaced `-mean` with `Mean`
 2. Replaced `-std` with `Std`
 3. Removed parenthesis `-()`
 4. Replaced `BodyBody` with `Body`

#### Sample of Renamed Variables Compared to the Original Variable Name

	 Raw Data            | Tidy Data 
	 --------------------|--------------
	 `subject`           | `subject`
	 `label`             | `label`
	 `tBodyAcc-mean()-X` | `tBodyAccMeanX`
	 `tBodyAcc-mean()-Y` | `tBodyAccMeanY`
	 `tBodyAcc-mean()-Z` | `tBodyAccMeanZ`
	 `tBodyAcc-std()-X`  | `tBodyAccStdX`
	 `tBodyAcc-std()-Y`  | `tBodyAccStdY`
	 `tBodyAcc-std()-Z`  | `tBodyAccStdZ`
