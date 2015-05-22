#Files in initial data
- 'features_info.txt': Shows information about the variables used on the feature vector.
- 'features.txt': List of all features.
- 'activity_labels.txt': Links the class labels with their activity name.
- 'train/X_train.txt': Training set.
- 'train/y_train.txt': Training labels.
- 'test/X_test.txt': Test set.
- 'test/y_test.txt': Test labels.
The following files are available for the train and test data. Their descriptions are equivalent. 
- 'train/subject_train.txt': Each row identifies the subject who performed the activity for each window sample. Its range is 
    from 1 to 30. 
- 'train/Inertial Signals/total_acc_x_train.txt': The acceleration signal from the smartphone accelerometer X axis in standard 
    gravity units 'g'. Every row shows a 128 element vector. The same description applies for the 'total_acc_x_train.txt' and 
    'total_acc_z_train.txt' files for the Y and Z axis. 
- 'train/Inertial Signals/body_acc_x_train.txt': The body acceleration signal obtained by subtracting the gravity from the 
    total acceleration. 
- 'train/Inertial Signals/body_gyro_x_train.txt': The angular velocity vector measured by the gyroscope for each window sample.
    The units are radians/second.

#Analysis Performed
1. Merge training and test sets to create one data set
      read in each data set
2. Extracts only measurements on the mean and stand dev for each measurement
      read features.txt (contains col names of the train.data and test.data sets)
      use grep to pull out just the mean and sd from feature list
      use the features list to pull out means and sd from data 
      +2 to account for subjects and labels in the beginning of data
3. Uses descriptive activity names to name the activities in the data set
      read in activity labels 
      replace labels in data with label names
4. Appropriately labels the data set with descriptive variable names
      make list of current column names and feature names
      clean up names (remove non-alphabetic character, convert to lowercase)
      then use the list as column names for data
5. From data in step 4, create a tidy data set with avg of each var for each activity and each subject
      aggregate to find the mean for each combination of subject and label
      write the data to upload


#Resulting Variables/Data
- 'data': combined test and training data
- 'data.mean.std': means and sd from data
- 'labels': activity_labels.txt
- 'aggregate.means': the mean for each combination of subject and label
- 'tidy.txt':table to be uploaded for coursera project
