gettingandcleaningdata project codebook:

Below information captured from http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

Data Set Information:

The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data.

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain. 

Attribute Information:

For each record in the dataset it is provided:
- Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration.
- Triaxial Angular velocity from the gyroscope.
- A 561-feature vector with time and frequency domain variables.
- Its activity label.
- An identifier of the subject who carried out the experiment. 

Here are the data for the project:

https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

Section 1. Merge the training and the test sets to create one data set.
After setting the source directory for the files using setwd() in RStudio, read  them into tables the data located in below files.
- features.txt
- activity_labels.txt
- subject_train.txt
- x_train.txt
- y_train.txt
- subject_test.txt
- x_test.txt
- y_test.txt

merge trainingdata and testdata into final data.

2. Extracts only the measurements on the mean and standard deviation for each measurement. 
Create a logicalVector that contains TRUE values for the ID, mean() & stddev() columns and FALSE for others and setset the final data.

3. Uses descriptive activity names to name the activities in the data set
Merge the finalData set with the acitivityType table to include descriptive activity names and updating colnames

4. Appropriately labels the data set with descriptive variable names.
Cleaning up the variable names, Reassigning the new descriptive column names to the finalData set

5. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.

create tidydata set as a txt file created with write.table() using row.name=FALSE as output.

Intially we need to setwd() to local directory of data downloaded. Then run run_analysis.R script to get approrpiate output mentioned above.
