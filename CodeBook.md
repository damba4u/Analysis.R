# CodeBook for Getting & Cleaning Data Assignment Week4

The codebook explains the variables, the source of data, all transformations made, and other information worth noting.

# The Key Data Sources
Description of dataset: http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones
Zipped Data: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

# Information about the Data
This experiment looks at information of volunteers within the age group of 19 - 48 years. Each person performed six 
activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung 
Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration 
and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data 
manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected
for generating the training data and 30% the test data.

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-
width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has 
gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and 
gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff 
frequency was used. From each window, a vector of features was obtained by calculating variables from the time and 
frequency domain.

# Data
The dataset contains the following files:
 1. 'README.txt'
 2. 'features.txt': List of all features.
 3. 'features_info.txt': Shows information about the variables used on the feature vector.
 4. 'activity_labels.txt': Links the class labels with their activity name.
 5. 'train/X_train.txt': Training set.
 6. 'train/y_train.txt': Training labels.
 7. 'test/X_test.txt': Test set.
 8. 'test/y_test.txt': Test labels.

# Files are available for the train and test data. 
 1. 'train/subject_train.txt': Each row identifies the subject who performed the activity for each window sample. 
    Its range is from 1 to 30.
 2. 'train/Inertial Signals/total_acc_x_train.txt': The acceleration signal from the smartphone accelerometer X axis in standard gravity 
    units 'g'. Every row shows a 128 element vector. The same description applies for the 'total_acc_x_train.txt' and 
    'total_acc_z_train.txt' files for the Y and Z axis.
3. 'train/Inertial Signals/body_acc_x_train.txt': The body acceleration signal obtained by subtracting the gravity from the 
    total acceleration.
4. 'train/Inertial Signals/body_gyro_x_train.txt': The angular velocity vector measured by the gyroscope for each window sample. The     
    units are radian/seconds.

# Data Transformation Stages
The 5 parts of the data are:
  1. Merges the training and the test sets to create one data set.
  2. Extracts only the measurements on the mean and standard deviation for each measurement.
  3. Uses descriptive activity names to name the activities in the data set.
  4. Appropriately labels the data set with descriptive activity names.
  5. Creates a second, independent tidy data set with the average of each variable for each activity and each subject.
  
# Data Running Processes
 1. The following packages should be run in R: data.tables & reshape2.
 2. Load the two dataset which are test and train data.
 3. Load the following: features and activity labels.
 4. Extract the mean and standard deviation column names and data.
 5. Process the data. There are two parts processing test and train data respectively.
 6. Merge data set.
 
