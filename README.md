run_analysis.R performs the data preparation and then followed by the 5 steps required as described in the course project’s definition:
Merges the training and the test sets to create one data set.
Extracts only the measurements on the mean and standard deviation for each measurement.
Uses descriptive activity names to name the activities in the data set
Appropriately labels the data set with descriptive variable names.
From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.

FinalData.txt is the exported final data after going through all the sequences described above


Codebook

run_analysis.R performs the required steps in dataset as given in course project

Step1:Dataset download

Step2:Allot data to different variable names 
 features <- features.txt: features comes from accelerometer
 activities <- activity_labels.txt: when measurements ar eperformed correspondingly
 subject_test <- test/subject_test.txt: has test data of subjects in observation
 x_test <- test/X_test.txt :has test data
 y_test <- test/y_test.txt :has test data of code label
 subject_train <- test/subject_train.txt : has training data of subjects in observation
 x_train <- test/X_train.txt :has train data recorded
 y_train <- test/y_train.txt :has train data of activity label

Step3:Merges the training and the test sets to create one data set
 X is merged data set of train and test of x labels
 Y is merged data set of train and test of y labels
 Subject is merged data of subjects of corresponding x and y labels
 Merged_Data is created by merging X,Y and Subject

Step4:Extracts only the measurements on the mean and standard deviation for each measurement
 TidyData created by subset from Merged_Data, extracting measurements on the mean and standard deviation (std) 

Step5:Uses descriptive activity names to name the activities in the data set
 code column of TidyData replaced with corresponding activity 
Step6:Appropriately labels the data set with descriptive variable names
 code column in TidyData renamed into activities
 Acc replaced by Accelerometer
 Gyro replaced by Gyroscope
 BodyBody replaced by Body
 Mag replaced by Magnitude
 f in column’s name replaced by Frequency
 t in column’s name replaced by Time
Step7: From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject
FinalData is created by taking summary from TidyData getting the means of each variable from each activity and subject.
