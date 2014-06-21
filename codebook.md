## Subject and Activity Overview

These data were collected from 30 subjects wearing a Samsung Galaxy S II smartphone on the waist.  Measurements from the smartphone's accelerometer and gyroscope were used to obtain data during the performance of 6 activities.  In the tidy.txt dataset, each subject is listed numerically in column 1 (Subject), with the following activities listed in column 2 (Activity):

Walking
WalkingUpstairs
WalkingDownstairs
Sitting
Standing
Laying

Each subject performed the above activities across a variable number of measurement periods.  Each row of the dataset represents the mean values obtained for each combination of subject and activity for all available timepoints.  

## Variables included and units

The variables selected for analysis were the mean and standard deviation values of the following raw features collected from the accelerometer and gyroscope:

timeBodyAccXYZ [Columns 3-8]
timeGravityAccXYZ  [Columns 9-14]
timeBodyAccJerkXYZ [Columns 15-20]
timeBodyGyroXYZ [Columns 21-26]
timeBodyGyroJerkXYZ [Columns 27-32]
timeBodyAccMag [Columns 33-34]
timeGravityAccMag [Columns 35-36]
timeBodyAccJerkMag [Columns 37-38]
timeBodyGyroMag [Columns 39-40]
timeBodyGyroJerkMag [Columns 41-42]
frequencyBodyAccXYZ [Columns 43-48]
frequencyBodyAccJerkXYZ [Columns 49-54]
frequencyBodyGyroXYZ [Columns 55-60]
frequencyBodyAccMag [Columns 61-62]
frequencyBodyAccJerkMag [Columns 63-64]
frequencyBodyGyroMag [Columns 65-66]
frequencyBodyGyroJerkMag [Columns 67-68]

Further detail on the physical meaning of these features appears below, but briefly, 'XYZ' is used to denote 3-axial signals in the X, Y and Z directions.  'Acc' denotes acceleration.  'Mag' denotes magnitude.  Each of these features was summarized as mean and standard deviation values, denoted by "Mean" and "Std", respectively.  Recall that in this dataset we are averaging over Subject and Activity pairs.  Thus the "timeBodyAccMeanX" variable in column 3 denotes the average of the mean acceleration in the X direction of the body in the time domain.  Similarly, "timeBodyAccStdX" denotes the average of the standard deviation of the acceleration of the body in the X direction in the time domain.

All features are normalized and bounded within [-1,1].
Units for all accelerometer (Acc) features are in standard gravity units, g.
Units for all gyroscope (Gyro) features are in radians/second.

## Physical meaning of features and technical details on collection

The features selected for this database come from the accelerometer and gyroscope 3-axial raw signals timeAccXYZ and timeGyroXYZ. These time domain signals were captured at a constant rate of 50 Hz. Then they were filtered using a median filter and a 3rd order low pass Butterworth filter with a corner frequency of 20 Hz to remove noise. Similarly, the acceleration signal was then separated into body and gravity acceleration signals (timeBodyAccXYZ and timeGravityAccXYZ) using another low pass Butterworth filter with a corner frequency of 0.3 Hz. 

Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals (timeBodyAccJerkXYZ and timeBodyGyroJerkXYZ). Also the magnitude of these three-dimensional signals were calculated using the Euclidean norm (timeBodyAccMag, timeGravityAccMag, timeBodyAccJerkMag, timeBodyGyroMag, timeBodyGyroJerkMag). 

Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing frequencyBodyAccXYZ, frequencyBodyAccJerkXYZ, frequencyBodyGyroXYZ, frequencyBodyAccJerkMag, frequencyBodyGyroMag, frequencyBodyGyroJerkMag. 
