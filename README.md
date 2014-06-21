## Data location 

In order to use the run_analysis script to generate the tidy dataset, it must be in the current working directory.  The UCI machine learning data must also be downloaded and unzipped in the working directory.  Source data can be downloaded here:

[https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip)

##Reshape2 requirement
In addition to the base R install, this script also requires that the reshape2 package be installed.

##Overview of processing steps

When run, this script summarizes the raw unzipped UCI data according to the following steps:

1. Merges the training and the test sets to create one data set.
  1. Binds together information from the x_train, y_train, and subject_train txt files from the training dataset. This combines training session data measurements, activity type labels, and subject IDs, respectively, into a single data frame.
  2. Binds together information from the x_test, y_test, and subject_test txt files from the test dataset.  This combines test session data measurements, activity type labels, and subject IDs, respectively, into a single data frame.
  3. Binds together training and test data frames to create a merged dataset.
2.  Labels the data set with descriptive variable names. 
  1. Uses variable names in the features txt file as preliminary variable names
  2.  Converts these preliminary names to friendlier, human-readable versions by eliminating punctuation, expanding domain identifiers 't' to 'time' and 'f' to 'frequency', and capitalizing "Mean" and "Std" summary categories.
3. Extracts only the measurements on the mean and standard deviation for each measurement. 
  1. Determines which columns in the merged dataset to keep based on a search for "Mean" or "Std" in the variable name
  2. MeanFreq variables and angle variables, which contain the word mean but don't appear to be true mean summary measures, are removed.
4. Creates a tidy data set with the average of each variable for each activity and each subject. 
  1.  Uses the reshape 2 package to create a new data frame where each row denotes the average value of each variable for each combination of subject and activity.
5. Uses descriptive activity names to name the activities in the data set
  1. Converts the activity ID from a numeric value 1-6 to a human readable category such as "Walking".  Activity names are based on the description in the activity_labels txt file.
6. Writes a tidy data set into the working directory as a txt file separated by "," and names it "tidy.txt"


