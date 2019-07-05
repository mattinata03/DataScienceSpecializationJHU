<<<<<<< HEAD
## Creating a Tidy Data Set from Human Activity Recognition (HAR) Smartphone Data
### CodeBook.md

#### Getting and Cleaning Data Course -- Final Project
#### *Lisa Murray*
=======
---
title: "Creating a Tidy Data Set from Human Activity Recognition (HAR) Smartphone Data"
author: "Lisa Murray"
date: "7/4/2019"
output: html_document
---
>>>>>>> bf3ec3aa1614bae96a3360bf31d01651d125ffc1

## Raw data files used in this project
Description of the raw data files *(taken from the README.txt from the Human Activity Recognition on Smartphones using a Multiclass Hardware-Friendly Support Vector Machine study)* [1]

* features.txt': List of all features. *(i.e. the measurement data descriptions)*
* activity_labels.txt': Links the class labels with their activity name
* train/X_train.txt': Training set
* train/y_train.txt': Training labels *(activity code for each observation)*
* train/subject_train.txt': Each row identifies the subject who performed the activity for each window sample. Its range is from 1 to 30.
* test/X_test.txt': Test set
* test/y_test.txt': Test labels *(activity code for each observation)*
* subject_test.txt': Each row identifies the subject who performed the activity for each window sample. Its range is from 1 to 30.

## Input files to the run_analysis.R script

### activity
##### read from activity_labels.txt)

##### Dimensions:

---------------------------------
Feature                    Result
------------------------ --------
Number of observations          6

Number of variables             2
---------------------------------

##### Summary table

---------------------------------------------------------------------------
Label   Variable             Class         # unique  Missing  Description  
                                             values                        
------- -------------------- ----------- ---------- --------- -------------
        **[activityCode]**   integer              6  0.00 %                

        **[activity]**       character            6  0.00 %                
---------------------------------------------------------------------------

### headerFile
##### (read from features_info.txt)

##### Dimensions:

---------------------------------
Feature                    Result
------------------------ --------
Number of observations        561

Number of variables             2
---------------------------------

##### Summary table

-----------------------------------------------------------------
Label   Variable     Class       # unique  Missing  Description  
                                   values                        
------- ------------ --------- ---------- --------- -------------
        **[key]**    integer          561  0.00 %                

        **[name]**   factor           477  0.00 %                
-----------------------------------------------------------------

### subtest / subtrain
##### (read from subject_test.txt and subject_train.txt)

##### Dimensions:

---------------------------------
Feature                    Result
------------------------ --------
Number of observations       2947

Number of variables             1
---------------------------------

##### Summary table

----------------------------------------------------------------------
Label   Variable          Class       # unique  Missing  Description  
                                        values                        
------- ----------------- --------- ---------- --------- -------------
        **[subjectID]**   integer            9  0.00 %                
----------------------------------------------------------------------

### ytest / ytrain
##### (read from y_test.txt and y_train.txt)

##### Dimensions:
---------------------------------
Feature                    Result
------------------------ --------
Number of observations       2947 *7352 for y_train)*

Number of variables             1
---------------------------------

# Codebook summary table

-------------------------------------------------------------------------
Label   Variable             Class       # unique  Missing  Description  
                                           values                        
------- -------------------- --------- ---------- --------- -------------
        **[activityCode]**   integer            6  0.00 %                
-------------------------------------------------------------------------

### xtest / xtrain
##### (read from x_test.txt and x_train.txt)

##### Dimensions:

---------------------------------
Feature                    Result
------------------------ --------
Number of observations       2947 *7352 for y_train)*

Number of variables           561
---------------------------------

##### Summary table

-------------------------------------------------------------------------------------------------
Label   Variable                                     Class       # unique  Missing  Description  
                                                                   values                        
------- -------------------------------------------- --------- ---------- --------- -------------
        **[tBodyAcc-mean()-X]**                      numeric         2947  0.00 %                

        **[tBodyAcc-mean()-Y]**                      numeric         2947  0.00 %                

        **[tBodyAcc-mean()-Z]**                      numeric         2947  0.00 %                

        **[tBodyAcc-std()-X]**                       numeric         2947  0.00 %                

        **[tBodyAcc-std()-Y]**                       numeric         2947  0.00 %                

        **[tBodyAcc-std()-Z]**                       numeric         2947  0.00 %                

        **[tBodyAcc-mad()-X]**                       numeric         2947  0.00 %                

        **[tBodyAcc-mad()-Y]**                       numeric         2947  0.00 %                

        **[tBodyAcc-mad()-Z]**                       numeric         2947  0.00 %                

        **[tBodyAcc-max()-X]**                       numeric         2082  0.00 %                

        **[tBodyAcc-max()-Y]**                       numeric         2108  0.00 %                

        **[tBodyAcc-max()-Z]**                       numeric         2077  0.00 %                

        **[tBodyAcc-min()-X]**                       numeric         2118  0.00 %                

        **[tBodyAcc-min()-Y]**                       numeric         2117  0.00 %                

        **[tBodyAcc-min()-Z]**                       numeric         2088  0.00 %                

        **[tBodyAcc-sma()]**                         numeric         2947  0.00 %                

        **[tBodyAcc-energy()-X]**                    numeric         2906  0.00 %                

        **[tBodyAcc-energy()-Y]**                    numeric         2938  0.00 %                

        **[tBodyAcc-energy()-Z]**                    numeric         2941  0.00 %                

        **[tBodyAcc-iqr()-X]**                       numeric         2946  0.00 %                

        **[tBodyAcc-iqr()-Y]**                       numeric         2947  0.00 %                

        **[tBodyAcc-iqr()-Z]**                       numeric         2947  0.00 %                

        **[tBodyAcc-entropy()-X]**                   numeric         1936  0.00 %                

        **[tBodyAcc-entropy()-Y]**                   numeric         2693  0.00 %                

        **[tBodyAcc-entropy()-Z]**                   numeric         2812  0.00 %                

        **[tBodyAcc-arCoeff()-X,1]**                 numeric         2947  0.00 %                

        **[tBodyAcc-arCoeff()-X,2]**                 numeric         2947  0.00 %                

        **[tBodyAcc-arCoeff()-X,3]**                 numeric         2947  0.00 %                

        **[tBodyAcc-arCoeff()-X,4]**                 numeric         2947  0.00 %                

        **[tBodyAcc-arCoeff()-Y,1]**                 numeric         2947  0.00 %                

        **[tBodyAcc-arCoeff()-Y,2]**                 numeric         2947  0.00 %                

        **[tBodyAcc-arCoeff()-Y,3]**                 numeric         2947  0.00 %                

        **[tBodyAcc-arCoeff()-Y,4]**                 numeric         2947  0.00 %                

        **[tBodyAcc-arCoeff()-Z,1]**                 numeric         2947  0.00 %                

        **[tBodyAcc-arCoeff()-Z,2]**                 numeric         2947  0.00 %                

        **[tBodyAcc-arCoeff()-Z,3]**                 numeric         2947  0.00 %                

        **[tBodyAcc-arCoeff()-Z,4]**                 numeric         2947  0.00 %                

        **[tBodyAcc-correlation()-X,Y]**             numeric         2947  0.00 %                

        **[tBodyAcc-correlation()-X,Z]**             numeric         2947  0.00 %                

        **[tBodyAcc-correlation()-Y,Z]**             numeric         2947  0.00 %                

        **[tGravityAcc-mean()-X]**                   numeric         2947  0.00 %                

        **[tGravityAcc-mean()-Y]**                   numeric         2947  0.00 %                

        **[tGravityAcc-mean()-Z]**                   numeric         2947  0.00 %                

        **[tGravityAcc-std()-X]**                    numeric         2945  0.00 %                

        **[tGravityAcc-std()-Y]**                    numeric         2946  0.00 %                

        **[tGravityAcc-std()-Z]**                    numeric         2946  0.00 %                

        **[tGravityAcc-mad()-X]**                    numeric         2947  0.00 %                

        **[tGravityAcc-mad()-Y]**                    numeric         2946  0.00 %                

        **[tGravityAcc-mad()-Z]**                    numeric         2947  0.00 %                

        **[tGravityAcc-max()-X]**                    numeric         2302  0.00 %                

        **[tGravityAcc-max()-Y]**                    numeric         2322  0.00 %                

        **[tGravityAcc-max()-Z]**                    numeric         2302  0.00 %                

        **[tGravityAcc-min()-X]**                    numeric         2281  0.00 %                

        **[tGravityAcc-min()-Y]**                    numeric         2286  0.00 %                

        **[tGravityAcc-min()-Z]**                    numeric         2291  0.00 %                

        **[tGravityAcc-sma()]**                      numeric         2947  0.00 %                

        **[tGravityAcc-energy()-X]**                 numeric         2947  0.00 %                

        **[tGravityAcc-energy()-Y]**                 numeric         2947  0.00 %                

        **[tGravityAcc-energy()-Z]**                 numeric         2945  0.00 %                

        **[tGravityAcc-iqr()-X]**                    numeric         2945  0.00 %                

        **[tGravityAcc-iqr()-Y]**                    numeric         2947  0.00 %                

        **[tGravityAcc-iqr()-Z]**                    numeric         2947  0.00 %                

        **[tGravityAcc-entropy()-X]**                numeric         1312  0.00 %                

        **[tGravityAcc-entropy()-Y]**                numeric          554  0.00 %                

        **[tGravityAcc-entropy()-Z]**                numeric         1394  0.00 %                

        **[tGravityAcc-arCoeff()-X,1]**              numeric         2947  0.00 %                

        **[tGravityAcc-arCoeff()-X,2]**              numeric         2947  0.00 %                

        **[tGravityAcc-arCoeff()-X,3]**              numeric         2947  0.00 %                

        **[tGravityAcc-arCoeff()-X,4]**              numeric         2947  0.00 %                

        **[tGravityAcc-arCoeff()-Y,1]**              numeric         2947  0.00 %                

        **[tGravityAcc-arCoeff()-Y,2]**              numeric         2947  0.00 %                

        **[tGravityAcc-arCoeff()-Y,3]**              numeric         2947  0.00 %                

        **[tGravityAcc-arCoeff()-Y,4]**              numeric         2947  0.00 %                

        **[tGravityAcc-arCoeff()-Z,1]**              numeric         2947  0.00 %                

        **[tGravityAcc-arCoeff()-Z,2]**              numeric         2946  0.00 %                

        **[tGravityAcc-arCoeff()-Z,3]**              numeric         2947  0.00 %                

        **[tGravityAcc-arCoeff()-Z,4]**              numeric         2947  0.00 %                

        **[tGravityAcc-correlation()-X,Y]**          numeric         2947  0.00 %                

        **[tGravityAcc-correlation()-X,Z]**          numeric         2947  0.00 %                

        **[tGravityAcc-correlation()-Y,Z]**          numeric         2947  0.00 %                

        **[tBodyAccJerk-mean()-X]**                  numeric         2947  0.00 %                

        **[tBodyAccJerk-mean()-Y]**                  numeric         2947  0.00 %                

        **[tBodyAccJerk-mean()-Z]**                  numeric         2947  0.00 %                

        **[tBodyAccJerk-std()-X]**                   numeric         2945  0.00 %                

        **[tBodyAccJerk-std()-Y]**                   numeric         2947  0.00 %                

        **[tBodyAccJerk-std()-Z]**                   numeric         2945  0.00 %                

        **[tBodyAccJerk-mad()-X]**                   numeric         2945  0.00 %                

        **[tBodyAccJerk-mad()-Y]**                   numeric         2947  0.00 %                

        **[tBodyAccJerk-mad()-Z]**                   numeric         2946  0.00 %                

        **[tBodyAccJerk-max()-X]**                   numeric         2119  0.00 %                

        **[tBodyAccJerk-max()-Y]**                   numeric         2112  0.00 %                

        **[tBodyAccJerk-max()-Z]**                   numeric         2096  0.00 %                

        **[tBodyAccJerk-min()-X]**                   numeric         2105  0.00 %                

        **[tBodyAccJerk-min()-Y]**                   numeric         2137  0.00 %                

        **[tBodyAccJerk-min()-Z]**                   numeric         2120  0.00 %                

        **[tBodyAccJerk-sma()]**                     numeric         2946  0.00 %                

        **[tBodyAccJerk-energy()-X]**                numeric         2927  0.00 %                

        **[tBodyAccJerk-energy()-Y]**                numeric         2937  0.00 %                

        **[tBodyAccJerk-energy()-Z]**                numeric         2926  0.00 %                

        **[tBodyAccJerk-iqr()-X]**                   numeric         2947  0.00 %                

        **[tBodyAccJerk-iqr()-Y]**                   numeric         2947  0.00 %                

        **[tBodyAccJerk-iqr()-Z]**                   numeric         2947  0.00 %                

        **[tBodyAccJerk-entropy()-X]**               numeric         2017  0.00 %                

        **[tBodyAccJerk-entropy()-Y]**               numeric         2106  0.00 %                

        **[tBodyAccJerk-entropy()-Z]**               numeric         2255  0.00 %                

        **[tBodyAccJerk-arCoeff()-X,1]**             numeric         2947  0.00 %                

        **[tBodyAccJerk-arCoeff()-X,2]**             numeric         2947  0.00 %                

        **[tBodyAccJerk-arCoeff()-X,3]**             numeric         2947  0.00 %                

        **[tBodyAccJerk-arCoeff()-X,4]**             numeric         2947  0.00 %                

        **[tBodyAccJerk-arCoeff()-Y,1]**             numeric         2947  0.00 %                

        **[tBodyAccJerk-arCoeff()-Y,2]**             numeric         2947  0.00 %                

        **[tBodyAccJerk-arCoeff()-Y,3]**             numeric         2947  0.00 %                

        **[tBodyAccJerk-arCoeff()-Y,4]**             numeric         2947  0.00 %                

        **[tBodyAccJerk-arCoeff()-Z,1]**             numeric         2947  0.00 %                

        **[tBodyAccJerk-arCoeff()-Z,2]**             numeric         2947  0.00 %                

        **[tBodyAccJerk-arCoeff()-Z,3]**             numeric         2947  0.00 %                

        **[tBodyAccJerk-arCoeff()-Z,4]**             numeric         2947  0.00 %                

        **[tBodyAccJerk-correlation()-X,Y]**         numeric         2947  0.00 %                

        **[tBodyAccJerk-correlation()-X,Z]**         numeric         2947  0.00 %                

        **[tBodyAccJerk-correlation()-Y,Z]**         numeric         2947  0.00 %                

        **[tBodyGyro-mean()-X]**                     numeric         2946  0.00 %                

        **[tBodyGyro-mean()-Y]**                     numeric         2947  0.00 %                

        **[tBodyGyro-mean()-Z]**                     numeric         2947  0.00 %                

        **[tBodyGyro-std()-X]**                      numeric         2947  0.00 %                

        **[tBodyGyro-std()-Y]**                      numeric         2947  0.00 %                

        **[tBodyGyro-std()-Z]**                      numeric         2946  0.00 %                

        **[tBodyGyro-mad()-X]**                      numeric         2947  0.00 %                

        **[tBodyGyro-mad()-Y]**                      numeric         2947  0.00 %                

        **[tBodyGyro-mad()-Z]**                      numeric         2947  0.00 %                

        **[tBodyGyro-max()-X]**                      numeric         2187  0.00 %                

        **[tBodyGyro-max()-Y]**                      numeric         2142  0.00 %                

        **[tBodyGyro-max()-Z]**                      numeric         2173  0.00 %                

        **[tBodyGyro-min()-X]**                      numeric         2178  0.00 %                

        **[tBodyGyro-min()-Y]**                      numeric         2126  0.00 %                

        **[tBodyGyro-min()-Z]**                      numeric         2166  0.00 %                

        **[tBodyGyro-sma()]**                        numeric         2945  0.00 %                

        **[tBodyGyro-energy()-X]**                   numeric         2929  0.00 %                

        **[tBodyGyro-energy()-Y]**                   numeric         2932  0.00 %                

        **[tBodyGyro-energy()-Z]**                   numeric         2934  0.00 %                

        **[tBodyGyro-iqr()-X]**                      numeric         2947  0.00 %                

        **[tBodyGyro-iqr()-Y]**                      numeric         2947  0.00 %                

        **[tBodyGyro-iqr()-Z]**                      numeric         2947  0.00 %                

        **[tBodyGyro-entropy()-X]**                  numeric         2568  0.00 %                

        **[tBodyGyro-entropy()-Y]**                  numeric         2526  0.00 %                

        **[tBodyGyro-entropy()-Z]**                  numeric         2538  0.00 %                

        **[tBodyGyro-arCoeff()-X,1]**                numeric         2946  0.00 %                

        **[tBodyGyro-arCoeff()-X,2]**                numeric         2946  0.00 %                

        **[tBodyGyro-arCoeff()-X,3]**                numeric         2947  0.00 %                

        **[tBodyGyro-arCoeff()-X,4]**                numeric         2947  0.00 %                

        **[tBodyGyro-arCoeff()-Y,1]**                numeric         2947  0.00 %                

        **[tBodyGyro-arCoeff()-Y,2]**                numeric         2947  0.00 %                

        **[tBodyGyro-arCoeff()-Y,3]**                numeric         2947  0.00 %                

        **[tBodyGyro-arCoeff()-Y,4]**                numeric         2947  0.00 %                

        **[tBodyGyro-arCoeff()-Z,1]**                numeric         2947  0.00 %                

        **[tBodyGyro-arCoeff()-Z,2]**                numeric         2947  0.00 %                

        **[tBodyGyro-arCoeff()-Z,3]**                numeric         2947  0.00 %                

        **[tBodyGyro-arCoeff()-Z,4]**                numeric         2947  0.00 %                

        **[tBodyGyro-correlation()-X,Y]**            numeric         2947  0.00 %                

        **[tBodyGyro-correlation()-X,Z]**            numeric         2947  0.00 %                

        **[tBodyGyro-correlation()-Y,Z]**            numeric         2947  0.00 %                

        **[tBodyGyroJerk-mean()-X]**                 numeric         2946  0.00 %                

        **[tBodyGyroJerk-mean()-Y]**                 numeric         2947  0.00 %                

        **[tBodyGyroJerk-mean()-Z]**                 numeric         2947  0.00 %                

        **[tBodyGyroJerk-std()-X]**                  numeric         2946  0.00 %                

        **[tBodyGyroJerk-std()-Y]**                  numeric         2946  0.00 %                

        **[tBodyGyroJerk-std()-Z]**                  numeric         2947  0.00 %                

        **[tBodyGyroJerk-mad()-X]**                  numeric         2946  0.00 %                

        **[tBodyGyroJerk-mad()-Y]**                  numeric         2946  0.00 %                

        **[tBodyGyroJerk-mad()-Z]**                  numeric         2947  0.00 %                

        **[tBodyGyroJerk-max()-X]**                  numeric         2128  0.00 %                

        **[tBodyGyroJerk-max()-Y]**                  numeric         2134  0.00 %                

        **[tBodyGyroJerk-max()-Z]**                  numeric         2122  0.00 %                

        **[tBodyGyroJerk-min()-X]**                  numeric         2139  0.00 %                

        **[tBodyGyroJerk-min()-Y]**                  numeric         2117  0.00 %                

        **[tBodyGyroJerk-min()-Z]**                  numeric         2135  0.00 %                

        **[tBodyGyroJerk-sma()]**                    numeric         2947  0.00 %                

        **[tBodyGyroJerk-energy()-X]**               numeric         2917  0.00 %                

        **[tBodyGyroJerk-energy()-Y]**               numeric         2902  0.00 %                

        **[tBodyGyroJerk-energy()-Z]**               numeric         2904  0.00 %                

        **[tBodyGyroJerk-iqr()-X]**                  numeric         2946  0.00 %                

        **[tBodyGyroJerk-iqr()-Y]**                  numeric         2945  0.00 %                

        **[tBodyGyroJerk-iqr()-Z]**                  numeric         2945  0.00 %                

        **[tBodyGyroJerk-entropy()-X]**              numeric         2366  0.00 %                

        **[tBodyGyroJerk-entropy()-Y]**              numeric         2543  0.00 %                

        **[tBodyGyroJerk-entropy()-Z]**              numeric         2365  0.00 %                

        **[tBodyGyroJerk-arCoeff()-X,1]**            numeric         2947  0.00 %                

        **[tBodyGyroJerk-arCoeff()-X,2]**            numeric         2947  0.00 %                

        **[tBodyGyroJerk-arCoeff()-X,3]**            numeric         2947  0.00 %                

        **[tBodyGyroJerk-arCoeff()-X,4]**            numeric         2947  0.00 %                

        **[tBodyGyroJerk-arCoeff()-Y,1]**            numeric         2947  0.00 %                

        **[tBodyGyroJerk-arCoeff()-Y,2]**            numeric         2946  0.00 %                

        **[tBodyGyroJerk-arCoeff()-Y,3]**            numeric         2947  0.00 %                

        **[tBodyGyroJerk-arCoeff()-Y,4]**            numeric         2947  0.00 %                

        **[tBodyGyroJerk-arCoeff()-Z,1]**            numeric         2947  0.00 %                

        **[tBodyGyroJerk-arCoeff()-Z,2]**            numeric         2947  0.00 %                

        **[tBodyGyroJerk-arCoeff()-Z,3]**            numeric         2946  0.00 %                

        **[tBodyGyroJerk-arCoeff()-Z,4]**            numeric         2947  0.00 %                

        **[tBodyGyroJerk-correlation()-X,Y]**        numeric         2947  0.00 %                

        **[tBodyGyroJerk-correlation()-X,Z]**        numeric         2947  0.00 %                

        **[tBodyGyroJerk-correlation()-Y,Z]**        numeric         2947  0.00 %                

        **[tBodyAccMag-mean()]**                     numeric         2947  0.00 %                

        **[tBodyAccMag-std()]**                      numeric         2946  0.00 %                

        **[tBodyAccMag-mad()]**                      numeric         2947  0.00 %                

        **[tBodyAccMag-max()]**                      numeric         2147  0.00 %                

        **[tBodyAccMag-min()]**                      numeric         2082  0.00 %                

        **[tBodyAccMag-sma()]**                      numeric         2947  0.00 %                

        **[tBodyAccMag-energy()]**                   numeric         2938  0.00 %                

        **[tBodyAccMag-iqr()]**                      numeric         2947  0.00 %                

        **[tBodyAccMag-entropy()]**                  numeric         2391  0.00 %                

        **[tBodyAccMag-arCoeff()1]**                 numeric         2947  0.00 %                

        **[tBodyAccMag-arCoeff()2]**                 numeric         2947  0.00 %                

        **[tBodyAccMag-arCoeff()3]**                 numeric         2947  0.00 %                

        **[tBodyAccMag-arCoeff()4]**                 numeric         2947  0.00 %                

        **[tGravityAccMag-mean()]**                  numeric         2947  0.00 %                

        **[tGravityAccMag-std()]**                   numeric         2946  0.00 %                

        **[tGravityAccMag-mad()]**                   numeric         2947  0.00 %                

        **[tGravityAccMag-max()]**                   numeric         2147  0.00 %                

        **[tGravityAccMag-min()]**                   numeric         2082  0.00 %                

        **[tGravityAccMag-sma()]**                   numeric         2947  0.00 %                

        **[tGravityAccMag-energy()]**                numeric         2938  0.00 %                

        **[tGravityAccMag-iqr()]**                   numeric         2947  0.00 %                

        **[tGravityAccMag-entropy()]**               numeric         2391  0.00 %                

        **[tGravityAccMag-arCoeff()1]**              numeric         2947  0.00 %                

        **[tGravityAccMag-arCoeff()2]**              numeric         2947  0.00 %                

        **[tGravityAccMag-arCoeff()3]**              numeric         2947  0.00 %                

        **[tGravityAccMag-arCoeff()4]**              numeric         2947  0.00 %                

        **[tBodyAccJerkMag-mean()]**                 numeric         2947  0.00 %                

        **[tBodyAccJerkMag-std()]**                  numeric         2947  0.00 %                

        **[tBodyAccJerkMag-mad()]**                  numeric         2946  0.00 %                

        **[tBodyAccJerkMag-max()]**                  numeric         2110  0.00 %                

        **[tBodyAccJerkMag-min()]**                  numeric         2087  0.00 %                

        **[tBodyAccJerkMag-sma()]**                  numeric         2947  0.00 %                

        **[tBodyAccJerkMag-energy()]**               numeric         2930  0.00 %                

        **[tBodyAccJerkMag-iqr()]**                  numeric         2947  0.00 %                

        **[tBodyAccJerkMag-entropy()]**              numeric         2625  0.00 %                

        **[tBodyAccJerkMag-arCoeff()1]**             numeric         2947  0.00 %                

        **[tBodyAccJerkMag-arCoeff()2]**             numeric         2947  0.00 %                

        **[tBodyAccJerkMag-arCoeff()3]**             numeric         2947  0.00 %                

        **[tBodyAccJerkMag-arCoeff()4]**             numeric         2947  0.00 %                

        **[tBodyGyroMag-mean()]**                    numeric         2946  0.00 %                

        **[tBodyGyroMag-std()]**                     numeric         2947  0.00 %                

        **[tBodyGyroMag-mad()]**                     numeric         2944  0.00 %                

        **[tBodyGyroMag-max()]**                     numeric         2208  0.00 %                

        **[tBodyGyroMag-min()]**                     numeric         2119  0.00 %                

        **[tBodyGyroMag-sma()]**                     numeric         2946  0.00 %                

        **[tBodyGyroMag-energy()]**                  numeric         2940  0.00 %                

        **[tBodyGyroMag-iqr()]**                     numeric         2946  0.00 %                

        **[tBodyGyroMag-entropy()]**                 numeric         2654  0.00 %                

        **[tBodyGyroMag-arCoeff()1]**                numeric         2947  0.00 %                

        **[tBodyGyroMag-arCoeff()2]**                numeric         2947  0.00 %                

        **[tBodyGyroMag-arCoeff()3]**                numeric         2947  0.00 %                

        **[tBodyGyroMag-arCoeff()4]**                numeric         2947  0.00 %                

        **[tBodyGyroJerkMag-mean()]**                numeric         2947  0.00 %                

        **[tBodyGyroJerkMag-std()]**                 numeric         2947  0.00 %                

        **[tBodyGyroJerkMag-mad()]**                 numeric         2946  0.00 %                

        **[tBodyGyroJerkMag-max()]**                 numeric         2138  0.00 %                

        **[tBodyGyroJerkMag-min()]**                 numeric         2075  0.00 %                

        **[tBodyGyroJerkMag-sma()]**                 numeric         2947  0.00 %                

        **[tBodyGyroJerkMag-energy()]**              numeric         2913  0.00 %                

        **[tBodyGyroJerkMag-iqr()]**                 numeric         2946  0.00 %                

        **[tBodyGyroJerkMag-entropy()]**             numeric         2471  0.00 %                

        **[tBodyGyroJerkMag-arCoeff()1]**            numeric         2947  0.00 %                

        **[tBodyGyroJerkMag-arCoeff()2]**            numeric         2947  0.00 %                

        **[tBodyGyroJerkMag-arCoeff()3]**            numeric         2947  0.00 %                

        **[tBodyGyroJerkMag-arCoeff()4]**            numeric         2947  0.00 %                

        **[fBodyAcc-mean()-X]**                      numeric         2946  0.00 %                

        **[fBodyAcc-mean()-Y]**                      numeric         2946  0.00 %                

        **[fBodyAcc-mean()-Z]**                      numeric         2945  0.00 %                

        **[fBodyAcc-std()-X]**                       numeric         2947  0.00 %                

        **[fBodyAcc-std()-Y]**                       numeric         2947  0.00 %                

        **[fBodyAcc-std()-Z]**                       numeric         2947  0.00 %                

        **[fBodyAcc-mad()-X]**                       numeric         2947  0.00 %                

        **[fBodyAcc-mad()-Y]**                       numeric         2947  0.00 %                

        **[fBodyAcc-mad()-Z]**                       numeric         2947  0.00 %                

        **[fBodyAcc-max()-X]**                       numeric         2946  0.00 %                

        **[fBodyAcc-max()-Y]**                       numeric         2946  0.00 %                

        **[fBodyAcc-max()-Z]**                       numeric         2947  0.00 %                

        **[fBodyAcc-min()-X]**                       numeric         2947  0.00 %                

        **[fBodyAcc-min()-Y]**                       numeric         2947  0.00 %                

        **[fBodyAcc-min()-Z]**                       numeric         2947  0.00 %                

        **[fBodyAcc-sma()]**                         numeric         2947  0.00 %                

        **[fBodyAcc-energy()-X]**                    numeric         2902  0.00 %                

        **[fBodyAcc-energy()-Y]**                    numeric         2941  0.00 %                

        **[fBodyAcc-energy()-Z]**                    numeric         2939  0.00 %                

        **[fBodyAcc-iqr()-X]**                       numeric         2947  0.00 %                

        **[fBodyAcc-iqr()-Y]**                       numeric         2947  0.00 %                

        **[fBodyAcc-iqr()-Z]**                       numeric         2947  0.00 %                

        **[fBodyAcc-entropy()-X]**                   numeric         1597  0.00 %                

        **[fBodyAcc-entropy()-Y]**                   numeric         1718  0.00 %                

        **[fBodyAcc-entropy()-Z]**                   numeric         1663  0.00 %                

        **[fBodyAcc-maxInds-X]**                     numeric           27  0.00 %                

        **[fBodyAcc-maxInds-Y]**                     numeric           22  0.00 %                

        **[fBodyAcc-maxInds-Z]**                     numeric           23  0.00 %                

        **[fBodyAcc-meanFreq()-X]**                  numeric         2947  0.00 %                

        **[fBodyAcc-meanFreq()-Y]**                  numeric         2947  0.00 %                

        **[fBodyAcc-meanFreq()-Z]**                  numeric         2947  0.00 %                

        **[fBodyAcc-skewness()-X]**                  numeric         2947  0.00 %                

        **[fBodyAcc-kurtosis()-X]**                  numeric         2946  0.00 %                

        **[fBodyAcc-skewness()-Y]**                  numeric         2947  0.00 %                

        **[fBodyAcc-kurtosis()-Y]**                  numeric         2947  0.00 %                

        **[fBodyAcc-skewness()-Z]**                  numeric         2947  0.00 %                

        **[fBodyAcc-kurtosis()-Z]**                  numeric         2946  0.00 %                

        **[fBodyAcc-bandsEnergy()-1,8]**             numeric         2940  0.00 %                

        **[fBodyAcc-bandsEnergy()-9,16]**            numeric         2937  0.00 %                

        **[fBodyAcc-bandsEnergy()-17,24]**           numeric         2937  0.00 %                

        **[fBodyAcc-bandsEnergy()-25,32]**           numeric         2923  0.00 %                

        **[fBodyAcc-bandsEnergy()-33,40]**           numeric         2934  0.00 %                

        **[fBodyAcc-bandsEnergy()-41,48]**           numeric         2936  0.00 %                

        **[fBodyAcc-bandsEnergy()-49,56]**           numeric         2940  0.00 %                

        **[fBodyAcc-bandsEnergy()-57,64]**           numeric         2914  0.00 %                

        **[fBodyAcc-bandsEnergy()-1,16]**            numeric         2942  0.00 %                

        **[fBodyAcc-bandsEnergy()-17,32]**           numeric         2929  0.00 %                

        **[fBodyAcc-bandsEnergy()-33,48]**           numeric         2931  0.00 %                

        **[fBodyAcc-bandsEnergy()-49,64]**           numeric         2940  0.00 %                

        **[fBodyAcc-bandsEnergy()-1,24]**            numeric         2943  0.00 %                

        **[fBodyAcc-bandsEnergy()-25,48]**           numeric         2927  0.00 %                

        **[fBodyAcc-bandsEnergy()-1,8]**             numeric         2940  0.00 %                

        **[fBodyAcc-bandsEnergy()-9,16]**            numeric         2937  0.00 %                

        **[fBodyAcc-bandsEnergy()-17,24]**           numeric         2937  0.00 %                

        **[fBodyAcc-bandsEnergy()-25,32]**           numeric         2923  0.00 %                

        **[fBodyAcc-bandsEnergy()-33,40]**           numeric         2934  0.00 %                

        **[fBodyAcc-bandsEnergy()-41,48]**           numeric         2936  0.00 %                

        **[fBodyAcc-bandsEnergy()-49,56]**           numeric         2940  0.00 %                

        **[fBodyAcc-bandsEnergy()-57,64]**           numeric         2914  0.00 %                

        **[fBodyAcc-bandsEnergy()-1,16]**            numeric         2942  0.00 %                

        **[fBodyAcc-bandsEnergy()-17,32]**           numeric         2929  0.00 %                

        **[fBodyAcc-bandsEnergy()-33,48]**           numeric         2931  0.00 %                

        **[fBodyAcc-bandsEnergy()-49,64]**           numeric         2940  0.00 %                

        **[fBodyAcc-bandsEnergy()-1,24]**            numeric         2943  0.00 %                

        **[fBodyAcc-bandsEnergy()-25,48]**           numeric         2927  0.00 %                

        **[fBodyAcc-bandsEnergy()-1,8]**             numeric         2940  0.00 %                

        **[fBodyAcc-bandsEnergy()-9,16]**            numeric         2937  0.00 %                

        **[fBodyAcc-bandsEnergy()-17,24]**           numeric         2937  0.00 %                

        **[fBodyAcc-bandsEnergy()-25,32]**           numeric         2923  0.00 %                

        **[fBodyAcc-bandsEnergy()-33,40]**           numeric         2934  0.00 %                

        **[fBodyAcc-bandsEnergy()-41,48]**           numeric         2936  0.00 %                

        **[fBodyAcc-bandsEnergy()-49,56]**           numeric         2940  0.00 %                

        **[fBodyAcc-bandsEnergy()-57,64]**           numeric         2914  0.00 %                

        **[fBodyAcc-bandsEnergy()-1,16]**            numeric         2942  0.00 %                

        **[fBodyAcc-bandsEnergy()-17,32]**           numeric         2929  0.00 %                

        **[fBodyAcc-bandsEnergy()-33,48]**           numeric         2931  0.00 %                

        **[fBodyAcc-bandsEnergy()-49,64]**           numeric         2940  0.00 %                

        **[fBodyAcc-bandsEnergy()-1,24]**            numeric         2943  0.00 %                

        **[fBodyAcc-bandsEnergy()-25,48]**           numeric         2927  0.00 %                

        **[fBodyAccJerk-mean()-X]**                  numeric         2947  0.00 %                

        **[fBodyAccJerk-mean()-Y]**                  numeric         2947  0.00 %                

        **[fBodyAccJerk-mean()-Z]**                  numeric         2947  0.00 %                

        **[fBodyAccJerk-std()-X]**                   numeric         2944  0.00 %                

        **[fBodyAccJerk-std()-Y]**                   numeric         2947  0.00 %                

        **[fBodyAccJerk-std()-Z]**                   numeric         2947  0.00 %                

        **[fBodyAccJerk-mad()-X]**                   numeric         2947  0.00 %                

        **[fBodyAccJerk-mad()-Y]**                   numeric         2947  0.00 %                

        **[fBodyAccJerk-mad()-Z]**                   numeric         2947  0.00 %                

        **[fBodyAccJerk-max()-X]**                   numeric         2945  0.00 %                

        **[fBodyAccJerk-max()-Y]**                   numeric         2947  0.00 %                

        **[fBodyAccJerk-max()-Z]**                   numeric         2947  0.00 %                

        **[fBodyAccJerk-min()-X]**                   numeric         2947  0.00 %                

        **[fBodyAccJerk-min()-Y]**                   numeric         2947  0.00 %                

        **[fBodyAccJerk-min()-Z]**                   numeric         2946  0.00 %                

        **[fBodyAccJerk-sma()]**                     numeric         2947  0.00 %                

        **[fBodyAccJerk-energy()-X]**                numeric         2920  0.00 %                

        **[fBodyAccJerk-energy()-Y]**                numeric         2930  0.00 %                

        **[fBodyAccJerk-energy()-Z]**                numeric         2932  0.00 %                

        **[fBodyAccJerk-iqr()-X]**                   numeric         2947  0.00 %                

        **[fBodyAccJerk-iqr()-Y]**                   numeric         2947  0.00 %                

        **[fBodyAccJerk-iqr()-Z]**                   numeric         2947  0.00 %                

        **[fBodyAccJerk-entropy()-X]**               numeric         1455  0.00 %                

        **[fBodyAccJerk-entropy()-Y]**               numeric         1478  0.00 %                

        **[fBodyAccJerk-entropy()-Z]**               numeric         1446  0.00 %                

        **[fBodyAccJerk-maxInds-X]**                 numeric           41  0.00 %                

        **[fBodyAccJerk-maxInds-Y]**                 numeric           42  0.00 %                

        **[fBodyAccJerk-maxInds-Z]**                 numeric           45  0.00 %                

        **[fBodyAccJerk-meanFreq()-X]**              numeric         2947  0.00 %                

        **[fBodyAccJerk-meanFreq()-Y]**              numeric         2947  0.00 %                

        **[fBodyAccJerk-meanFreq()-Z]**              numeric         2947  0.00 %                

        **[fBodyAccJerk-skewness()-X]**              numeric         2947  0.00 %                

        **[fBodyAccJerk-kurtosis()-X]**              numeric         2947  0.00 %                

        **[fBodyAccJerk-skewness()-Y]**              numeric         2947  0.00 %                

        **[fBodyAccJerk-kurtosis()-Y]**              numeric         2947  0.00 %                

        **[fBodyAccJerk-skewness()-Z]**              numeric         2947  0.00 %                

        **[fBodyAccJerk-kurtosis()-Z]**              numeric         2947  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-1,8]**         numeric         2933  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-9,16]**        numeric         2927  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-17,24]**       numeric         2928  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-25,32]**       numeric         2923  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-33,40]**       numeric         2932  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-41,48]**       numeric         2938  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-49,56]**       numeric         2941  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-57,64]**       numeric         2909  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-1,16]**        numeric         2936  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-17,32]**       numeric         2923  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-33,48]**       numeric         2934  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-49,64]**       numeric         2938  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-1,24]**        numeric         2931  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-25,48]**       numeric         2926  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-1,8]**         numeric         2933  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-9,16]**        numeric         2927  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-17,24]**       numeric         2928  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-25,32]**       numeric         2923  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-33,40]**       numeric         2932  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-41,48]**       numeric         2938  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-49,56]**       numeric         2941  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-57,64]**       numeric         2909  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-1,16]**        numeric         2936  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-17,32]**       numeric         2923  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-33,48]**       numeric         2934  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-49,64]**       numeric         2938  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-1,24]**        numeric         2931  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-25,48]**       numeric         2926  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-1,8]**         numeric         2933  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-9,16]**        numeric         2927  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-17,24]**       numeric         2928  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-25,32]**       numeric         2923  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-33,40]**       numeric         2932  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-41,48]**       numeric         2938  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-49,56]**       numeric         2941  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-57,64]**       numeric         2909  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-1,16]**        numeric         2936  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-17,32]**       numeric         2923  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-33,48]**       numeric         2934  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-49,64]**       numeric         2938  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-1,24]**        numeric         2931  0.00 %                

        **[fBodyAccJerk-bandsEnergy()-25,48]**       numeric         2926  0.00 %                

        **[fBodyGyro-mean()-X]**                     numeric         2947  0.00 %                

        **[fBodyGyro-mean()-Y]**                     numeric         2947  0.00 %                

        **[fBodyGyro-mean()-Z]**                     numeric         2947  0.00 %                

        **[fBodyGyro-std()-X]**                      numeric         2946  0.00 %                

        **[fBodyGyro-std()-Y]**                      numeric         2946  0.00 %                

        **[fBodyGyro-std()-Z]**                      numeric         2946  0.00 %                

        **[fBodyGyro-mad()-X]**                      numeric         2946  0.00 %                

        **[fBodyGyro-mad()-Y]**                      numeric         2947  0.00 %                

        **[fBodyGyro-mad()-Z]**                      numeric         2946  0.00 %                

        **[fBodyGyro-max()-X]**                      numeric         2947  0.00 %                

        **[fBodyGyro-max()-Y]**                      numeric         2947  0.00 %                

        **[fBodyGyro-max()-Z]**                      numeric         2947  0.00 %                

        **[fBodyGyro-min()-X]**                      numeric         2946  0.00 %                

        **[fBodyGyro-min()-Y]**                      numeric         2946  0.00 %                

        **[fBodyGyro-min()-Z]**                      numeric         2947  0.00 %                

        **[fBodyGyro-sma()]**                        numeric         2947  0.00 %                

        **[fBodyGyro-energy()-X]**                   numeric         2920  0.00 %                

        **[fBodyGyro-energy()-Y]**                   numeric         2935  0.00 %                

        **[fBodyGyro-energy()-Z]**                   numeric         2937  0.00 %                

        **[fBodyGyro-iqr()-X]**                      numeric         2947  0.00 %                

        **[fBodyGyro-iqr()-Y]**                      numeric         2947  0.00 %                

        **[fBodyGyro-iqr()-Z]**                      numeric         2947  0.00 %                

        **[fBodyGyro-entropy()-X]**                  numeric         2115  0.00 %                

        **[fBodyGyro-entropy()-Y]**                  numeric         2166  0.00 %                

        **[fBodyGyro-entropy()-Z]**                  numeric         1990  0.00 %                

        **[fBodyGyro-maxInds-X]**                    numeric           21  0.00 %                

        **[fBodyGyro-maxInds-Y]**                    numeric           28  0.00 %                

        **[fBodyGyro-maxInds-Z]**                    numeric           22  0.00 %                

        **[fBodyGyro-meanFreq()-X]**                 numeric         2947  0.00 %                

        **[fBodyGyro-meanFreq()-Y]**                 numeric         2947  0.00 %                

        **[fBodyGyro-meanFreq()-Z]**                 numeric         2947  0.00 %                

        **[fBodyGyro-skewness()-X]**                 numeric         2947  0.00 %                

        **[fBodyGyro-kurtosis()-X]**                 numeric         2947  0.00 %                

        **[fBodyGyro-skewness()-Y]**                 numeric         2947  0.00 %                

        **[fBodyGyro-kurtosis()-Y]**                 numeric         2947  0.00 %                

        **[fBodyGyro-skewness()-Z]**                 numeric         2947  0.00 %                

        **[fBodyGyro-kurtosis()-Z]**                 numeric         2947  0.00 %                

        **[fBodyGyro-bandsEnergy()-1,8]**            numeric         2932  0.00 %                

        **[fBodyGyro-bandsEnergy()-9,16]**           numeric         2910  0.00 %                

        **[fBodyGyro-bandsEnergy()-17,24]**          numeric         2897  0.00 %                

        **[fBodyGyro-bandsEnergy()-25,32]**          numeric         2897  0.00 %                

        **[fBodyGyro-bandsEnergy()-33,40]**          numeric         2902  0.00 %                

        **[fBodyGyro-bandsEnergy()-41,48]**          numeric         2924  0.00 %                

        **[fBodyGyro-bandsEnergy()-49,56]**          numeric         2926  0.00 %                

        **[fBodyGyro-bandsEnergy()-57,64]**          numeric         2837  0.00 %                

        **[fBodyGyro-bandsEnergy()-1,16]**           numeric         2935  0.00 %                

        **[fBodyGyro-bandsEnergy()-17,32]**          numeric         2918  0.00 %                

        **[fBodyGyro-bandsEnergy()-33,48]**          numeric         2903  0.00 %                

        **[fBodyGyro-bandsEnergy()-49,64]**          numeric         2919  0.00 %                

        **[fBodyGyro-bandsEnergy()-1,24]**           numeric         2931  0.00 %                

        **[fBodyGyro-bandsEnergy()-25,48]**          numeric         2897  0.00 %                

        **[fBodyGyro-bandsEnergy()-1,8]**            numeric         2932  0.00 %                

        **[fBodyGyro-bandsEnergy()-9,16]**           numeric         2910  0.00 %                

        **[fBodyGyro-bandsEnergy()-17,24]**          numeric         2897  0.00 %                

        **[fBodyGyro-bandsEnergy()-25,32]**          numeric         2897  0.00 %                

        **[fBodyGyro-bandsEnergy()-33,40]**          numeric         2902  0.00 %                

        **[fBodyGyro-bandsEnergy()-41,48]**          numeric         2924  0.00 %                

        **[fBodyGyro-bandsEnergy()-49,56]**          numeric         2926  0.00 %                

        **[fBodyGyro-bandsEnergy()-57,64]**          numeric         2837  0.00 %                

        **[fBodyGyro-bandsEnergy()-1,16]**           numeric         2935  0.00 %                

        **[fBodyGyro-bandsEnergy()-17,32]**          numeric         2918  0.00 %                

        **[fBodyGyro-bandsEnergy()-33,48]**          numeric         2903  0.00 %                

        **[fBodyGyro-bandsEnergy()-49,64]**          numeric         2919  0.00 %                

        **[fBodyGyro-bandsEnergy()-1,24]**           numeric         2931  0.00 %                

        **[fBodyGyro-bandsEnergy()-25,48]**          numeric         2897  0.00 %                

        **[fBodyGyro-bandsEnergy()-1,8]**            numeric         2932  0.00 %                

        **[fBodyGyro-bandsEnergy()-9,16]**           numeric         2910  0.00 %                

        **[fBodyGyro-bandsEnergy()-17,24]**          numeric         2897  0.00 %                

        **[fBodyGyro-bandsEnergy()-25,32]**          numeric         2897  0.00 %                

        **[fBodyGyro-bandsEnergy()-33,40]**          numeric         2902  0.00 %                

        **[fBodyGyro-bandsEnergy()-41,48]**          numeric         2924  0.00 %                

        **[fBodyGyro-bandsEnergy()-49,56]**          numeric         2926  0.00 %                

        **[fBodyGyro-bandsEnergy()-57,64]**          numeric         2837  0.00 %                

        **[fBodyGyro-bandsEnergy()-1,16]**           numeric         2935  0.00 %                

        **[fBodyGyro-bandsEnergy()-17,32]**          numeric         2918  0.00 %                

        **[fBodyGyro-bandsEnergy()-33,48]**          numeric         2903  0.00 %                

        **[fBodyGyro-bandsEnergy()-49,64]**          numeric         2919  0.00 %                

        **[fBodyGyro-bandsEnergy()-1,24]**           numeric         2931  0.00 %                

        **[fBodyGyro-bandsEnergy()-25,48]**          numeric         2897  0.00 %                

        **[fBodyAccMag-mean()]**                     numeric         2947  0.00 %                

        **[fBodyAccMag-std()]**                      numeric         2947  0.00 %                

        **[fBodyAccMag-mad()]**                      numeric         2947  0.00 %                

        **[fBodyAccMag-max()]**                      numeric         2947  0.00 %                

        **[fBodyAccMag-min()]**                      numeric         2947  0.00 %                

        **[fBodyAccMag-sma()]**                      numeric         2947  0.00 %                

        **[fBodyAccMag-energy()]**                   numeric         2939  0.00 %                

        **[fBodyAccMag-iqr()]**                      numeric         2947  0.00 %                

        **[fBodyAccMag-entropy()]**                  numeric         1684  0.00 %                

        **[fBodyAccMag-maxInds]**                    numeric           21  0.00 %                

        **[fBodyAccMag-meanFreq()]**                 numeric         2947  0.00 %                

        **[fBodyAccMag-skewness()]**                 numeric         2947  0.00 %                

        **[fBodyAccMag-kurtosis()]**                 numeric         2947  0.00 %                

        **[fBodyBodyAccJerkMag-mean()]**             numeric         2947  0.00 %                

        **[fBodyBodyAccJerkMag-std()]**              numeric         2946  0.00 %                

        **[fBodyBodyAccJerkMag-mad()]**              numeric         2947  0.00 %                

        **[fBodyBodyAccJerkMag-max()]**              numeric         2947  0.00 %                

        **[fBodyBodyAccJerkMag-min()]**              numeric         2946  0.00 %                

        **[fBodyBodyAccJerkMag-sma()]**              numeric         2947  0.00 %                

        **[fBodyBodyAccJerkMag-energy()]**           numeric         2921  0.00 %                

        **[fBodyBodyAccJerkMag-iqr()]**              numeric         2947  0.00 %                

        **[fBodyBodyAccJerkMag-entropy()]**          numeric         1499  0.00 %                

        **[fBodyBodyAccJerkMag-maxInds]**            numeric           50  0.00 %                

        **[fBodyBodyAccJerkMag-meanFreq()]**         numeric         2947  0.00 %                

        **[fBodyBodyAccJerkMag-skewness()]**         numeric         2947  0.00 %                

        **[fBodyBodyAccJerkMag-kurtosis()]**         numeric         2947  0.00 %                

        **[fBodyBodyGyroMag-mean()]**                numeric         2947  0.00 %                

        **[fBodyBodyGyroMag-std()]**                 numeric         2947  0.00 %                

        **[fBodyBodyGyroMag-mad()]**                 numeric         2947  0.00 %                

        **[fBodyBodyGyroMag-max()]**                 numeric         2947  0.00 %                

        **[fBodyBodyGyroMag-min()]**                 numeric         2946  0.00 %                

        **[fBodyBodyGyroMag-sma()]**                 numeric         2947  0.00 %                

        **[fBodyBodyGyroMag-energy()]**              numeric         2937  0.00 %                

        **[fBodyBodyGyroMag-iqr()]**                 numeric         2947  0.00 %                

        **[fBodyBodyGyroMag-entropy()]**             numeric         2163  0.00 %                

        **[fBodyBodyGyroMag-maxInds]**               numeric           21  0.00 %                

        **[fBodyBodyGyroMag-meanFreq()]**            numeric         2947  0.00 %                

        **[fBodyBodyGyroMag-skewness()]**            numeric         2947  0.00 %                

        **[fBodyBodyGyroMag-kurtosis()]**            numeric         2947  0.00 %                

        **[fBodyBodyGyroJerkMag-mean()]**            numeric         2947  0.00 %                

        **[fBodyBodyGyroJerkMag-std()]**             numeric         2947  0.00 %                

        **[fBodyBodyGyroJerkMag-mad()]**             numeric         2947  0.00 %                

        **[fBodyBodyGyroJerkMag-max()]**             numeric         2947  0.00 %                

        **[fBodyBodyGyroJerkMag-min()]**             numeric         2946  0.00 %                

        **[fBodyBodyGyroJerkMag-sma()]**             numeric         2947  0.00 %                

        **[fBodyBodyGyroJerkMag-energy()]**          numeric         2899  0.00 %                

        **[fBodyBodyGyroJerkMag-iqr()]**             numeric         2947  0.00 %                

        **[fBodyBodyGyroJerkMag-entropy()]**         numeric         1721  0.00 %                

        **[fBodyBodyGyroJerkMag-maxInds]**           numeric           40  0.00 %                

        **[fBodyBodyGyroJerkMag-meanFreq()]**        numeric         2947  0.00 %                

        **[fBodyBodyGyroJerkMag-skewness()]**        numeric         2947  0.00 %                

        **[fBodyBodyGyroJerkMag-kurtosis()]**        numeric         2947  0.00 %                

        **[angle(tBodyAccMean,gravity)]**            numeric         2947  0.00 %                

        **[angle(tBodyAccJerkMean),gravityMean)]**   numeric         2947  0.00 %                

        **[angle(tBodyGyroMean,gravityMean)]**       numeric         2947  0.00 %                

        **[angle(tBodyGyroJerkMean,gravityMean)]**   numeric         2947  0.00 %                

        **[angle(X,gravityMean)]**                   numeric         2947  0.00 %                

        **[angle(Y,gravityMean)]**                   numeric         2947  0.00 %                

        **[angle(Z,gravityMean)]**                   numeric         2947  0.00 %                
-------------------------------------------------------------------------------------------------

### Interim Files

### testHAR / trainHAR / dataHAR

Result from binding columns of the testHAR and trainHAR datasets *(only the std() and mean() measurements are included in these files -- this data was removed from the xtest and ytest earlier in run_analysis.R -- see README.md for details)*

##### Dimensions:
---------------------------------
Feature                    Result
------------------------ --------
Number of observations      10299 *(7352 for trainHAR, 2947 for testHAR)*

Number of variables            81
---------------------------------

##### Summary table

--------------------------------------------------------------------------------------------
Label   Variable                                Class       # unique  Missing  Description  
                                                              values                        
------- --------------------------------------- --------- ---------- --------- -------------
        **[subjectID]**                         integer           30  0.00 %                

        **[activityCode]**                      integer            6  0.00 %                

        **[tBodyAcc-mean()-X]**                 numeric        10292  0.00 %                

        **[tBodyAcc-mean()-Y]**                 numeric        10299  0.00 %                

        **[tBodyAcc-mean()-Z]**                 numeric        10293  0.00 %                

        **[tBodyAcc-std()-X]**                  numeric        10295  0.00 %                

        **[tBodyAcc-std()-Y]**                  numeric        10297  0.00 %                

        **[tBodyAcc-std()-Z]**                  numeric        10297  0.00 %                

        **[tGravityAcc-mean()-X]**              numeric        10296  0.00 %                

        **[tGravityAcc-mean()-Y]**              numeric        10298  0.00 %                

        **[tGravityAcc-mean()-Z]**              numeric        10299  0.00 %                

        **[tGravityAcc-std()-X]**               numeric        10288  0.00 %                

        **[tGravityAcc-std()-Y]**               numeric        10293  0.00 %                

        **[tGravityAcc-std()-Z]**               numeric        10296  0.00 %                

        **[tBodyAccJerk-mean()-X]**             numeric        10299  0.00 %                

        **[tBodyAccJerk-mean()-Y]**             numeric        10299  0.00 %                

        **[tBodyAccJerk-mean()-Z]**             numeric        10299  0.00 %                

        **[tBodyAccJerk-std()-X]**              numeric        10290  0.00 %                

        **[tBodyAccJerk-std()-Y]**              numeric        10296  0.00 %                

        **[tBodyAccJerk-std()-Z]**              numeric        10293  0.00 %                

        **[tBodyGyro-mean()-X]**                numeric        10298  0.00 %                

        **[tBodyGyro-mean()-Y]**                numeric        10299  0.00 %                

        **[tBodyGyro-mean()-Z]**                numeric        10297  0.00 %                

        **[tBodyGyro-std()-X]**                 numeric        10292  0.00 %                

        **[tBodyGyro-std()-Y]**                 numeric        10296  0.00 %                

        **[tBodyGyro-std()-Z]**                 numeric        10296  0.00 %                

        **[tBodyGyroJerk-mean()-X]**            numeric        10295  0.00 %                

        **[tBodyGyroJerk-mean()-Y]**            numeric        10299  0.00 %                

        **[tBodyGyroJerk-mean()-Z]**            numeric        10298  0.00 %                

        **[tBodyGyroJerk-std()-X]**             numeric        10292  0.00 %                

        **[tBodyGyroJerk-std()-Y]**             numeric        10295  0.00 %                

        **[tBodyGyroJerk-std()-Z]**             numeric        10291  0.00 %                

        **[tBodyAccMag-mean()]**                numeric        10296  0.00 %                

        **[tBodyAccMag-std()]**                 numeric        10294  0.00 %                

        **[tGravityAccMag-mean()]**             numeric        10296  0.00 %                

        **[tGravityAccMag-std()]**              numeric        10294  0.00 %                

        **[tBodyAccJerkMag-mean()]**            numeric        10292  0.00 %                

        **[tBodyAccJerkMag-std()]**             numeric        10294  0.00 %                

        **[tBodyGyroMag-mean()]**               numeric        10298  0.00 %                

        **[tBodyGyroMag-std()]**                numeric        10298  0.00 %                

        **[tBodyGyroJerkMag-mean()]**           numeric        10293  0.00 %                

        **[tBodyGyroJerkMag-std()]**            numeric        10297  0.00 %                

        **[fBodyAcc-mean()-X]**                 numeric        10295  0.00 %                

        **[fBodyAcc-mean()-Y]**                 numeric        10292  0.00 %                

        **[fBodyAcc-mean()-Z]**                 numeric        10295  0.00 %                

        **[fBodyAcc-std()-X]**                  numeric        10294  0.00 %                

        **[fBodyAcc-std()-Y]**                  numeric        10297  0.00 %                

        **[fBodyAcc-std()-Z]**                  numeric        10296  0.00 %                

        **[fBodyAcc-meanFreq()-X]**             numeric        10299  0.00 %                

        **[fBodyAcc-meanFreq()-Y]**             numeric        10299  0.00 %                

        **[fBodyAcc-meanFreq()-Z]**             numeric        10299  0.00 %                

        **[fBodyAccJerk-mean()-X]**             numeric        10293  0.00 %                

        **[fBodyAccJerk-mean()-Y]**             numeric        10296  0.00 %                

        **[fBodyAccJerk-mean()-Z]**             numeric        10294  0.00 %                

        **[fBodyAccJerk-std()-X]**              numeric        10291  0.00 %                

        **[fBodyAccJerk-std()-Y]**              numeric        10294  0.00 %                

        **[fBodyAccJerk-std()-Z]**              numeric        10290  0.00 %                

        **[fBodyAccJerk-meanFreq()-X]**         numeric        10298  0.00 %                

        **[fBodyAccJerk-meanFreq()-Y]**         numeric        10299  0.00 %                

        **[fBodyAccJerk-meanFreq()-Z]**         numeric        10298  0.00 %                

        **[fBodyGyro-mean()-X]**                numeric        10297  0.00 %                

        **[fBodyGyro-mean()-Y]**                numeric        10296  0.00 %                

        **[fBodyGyro-mean()-Z]**                numeric        10297  0.00 %                

        **[fBodyGyro-std()-X]**                 numeric        10297  0.00 %                

        **[fBodyGyro-std()-Y]**                 numeric        10293  0.00 %                

        **[fBodyGyro-std()-Z]**                 numeric        10295  0.00 %                

        **[fBodyGyro-meanFreq()-X]**            numeric        10298  0.00 %                

        **[fBodyGyro-meanFreq()-Y]**            numeric        10299  0.00 %                

        **[fBodyGyro-meanFreq()-Z]**            numeric        10299  0.00 %                

        **[fBodyAccMag-mean()]**                numeric        10296  0.00 %                

        **[fBodyAccMag-std()]**                 numeric        10298  0.00 %                

        **[fBodyAccMag-meanFreq()]**            numeric        10299  0.00 %                

        **[fBodyBodyAccJerkMag-mean()]**        numeric        10290  0.00 %                

        **[fBodyBodyAccJerkMag-std()]**         numeric        10296  0.00 %                

        **[fBodyBodyAccJerkMag-meanFreq()]**    numeric        10299  0.00 %                

        **[fBodyBodyGyroMag-mean()]**           numeric        10297  0.00 %                

        **[fBodyBodyGyroMag-std()]**            numeric        10296  0.00 %                

        **[fBodyBodyGyroMag-meanFreq()]**       numeric        10299  0.00 %                

        **[fBodyBodyGyroJerkMag-mean()]**       numeric        10293  0.00 %                

        **[fBodyBodyGyroJerkMag-std()]**        numeric        10292  0.00 %                

        **[fBodyBodyGyroJerkMag-meanFreq()]**   numeric        10299  0.00 %                
--------------------------------------------------------------------------------------------

### meltHAR

##### Dimensions:
---------------------------------
Feature                    Result
------------------------ --------
Number of observations     813621

Number of variables             4
---------------------------------

#### Summary table

-------------------------------------------------------------------------
Label   Variable             Class       # unique  Missing  Description  
                                           values                        
------- -------------------- --------- ---------- --------- -------------
        **[subjectID]**      integer           30  0.00 %                

        **[activityCode]**   integer            6  0.00 %                

        **[variable]**       factor            79  0.00 %                

        **[value]**          numeric       783226  0.00 %                
-------------------------------------------------------------------------


##### tidyHARprep

This data set has the same layout as the final file **tidyHAR** the only differences are in the field names which were modified for final output. The change that were made are:

1. All fields that start with **[fBodyBody** where modified to **[fBody**, the fields affected are:

* **[fBodyBodyAccJerkMag-std()]**                        
* **[fBodyBodyAccJerkMag-meanFreq()]**                 
* **[fBodyBodyGyroMag-mean()]**                         
* **[fBodyBodyGyroMag-std()]**                         
* **[fBodyBodyGyroMag-meanFreq()]**                      
* **[fBodyBodyGyroJerkMag-mean()]**                     
* **[fBodyBodyGyroJerkMag-std()]**                    
* **[fBodyBodyGyroJerkMag-meanFreq()]**   

2. All data fields were modified to add the verbiage **Average-** at the beginning. *(see summary for tidyHAR below)*

### tidyHAR
The final clean data set

##### Dimensions:
---------------------------------
Feature                    Result
------------------------ --------
Number of observations        180

Number of variables            82
---------------------------------

##### Summary table:

-------------------------------------------------------------------------------------
Label   Variable                       Class         # unique  Missing  Description  
                                                       values                        
------- ------------------------------ ----------- ---------- --------- -------------
        **[subjectID]**                integer             30  0.00 %                

        **[activityCode]**             integer              6  0.00 %                

        **[activity]**                 character            6  0.00 %                

        **[Average-                    numeric            180  0.00 %                
        tBodyAcc-mean-X]**                                                           

        **[Average-                    numeric            180  0.00 %                
        tBodyAcc-mean-Y]**                                                           

        **[Average-                    numeric            180  0.00 %                
        tBodyAcc-mean-Z]**                                                           

        **[Average-                    numeric            180  0.00 %                
        tBodyAcc-std-X]**                                                            

        **[Average-                    numeric            180  0.00 %                
        tBodyAcc-std-Y]**                                                            

        **[Average-                    numeric            180  0.00 %                
        tBodyAcc-std-Z]**                                                            

        **[Average-                    numeric            180  0.00 %                
        tGravityAcc-mean-X]**                                                        

        **[Average-                    numeric            180  0.00 %                
        tGravityAcc-mean-Y]**                                                        

        **[Average-                    numeric            180  0.00 %                
        tGravityAcc-mean-Z]**                                                        

        **[Average-                    numeric            180  0.00 %                
        tGravityAcc-std-X]**                                                         

        **[Average-                    numeric            180  0.00 %                
        tGravityAcc-std-Y]**                                                         

        **[Average-                    numeric            180  0.00 %                
        tGravityAcc-std-Z]**                                                         

        **[Average-                    numeric            180  0.00 %                
        tBodyAccJerk-mean-X]**                                                       

        **[Average-                    numeric            180  0.00 %                
        tBodyAccJerk-mean-Y]**                                                       

        **[Average-                    numeric            180  0.00 %                
        tBodyAccJerk-mean-Z]**                                                       

        **[Average-                    numeric            180  0.00 %                
        tBodyAccJerk-std-X]**                                                        

        **[Average-                    numeric            180  0.00 %                
        tBodyAccJerk-std-Y]**                                                        

        **[Average-                    numeric            180  0.00 %                
        tBodyAccJerk-std-Z]**                                                        

        **[Average-                    numeric            180  0.00 %                
        tBodyGyro-mean-X]**                                                          

        **[Average-                    numeric            180  0.00 %                
        tBodyGyro-mean-Y]**                                                          

        **[Average-                    numeric            180  0.00 %                
        tBodyGyro-mean-Z]**                                                          

        **[Average-                    numeric            180  0.00 %                
        tBodyGyro-std-X]**                                                           

        **[Average-                    numeric            180  0.00 %                
        tBodyGyro-std-Y]**                                                           

        **[Average-                    numeric            180  0.00 %                
        tBodyGyro-std-Z]**                                                           

        **[Average-                    numeric            180  0.00 %                
        tBodyGyroJerk-mean-X]**                                                      

        **[Average-                    numeric            180  0.00 %                
        tBodyGyroJerk-mean-Y]**                                                      

        **[Average-                    numeric            180  0.00 %                
        tBodyGyroJerk-mean-Z]**                                                      

        **[Average-                    numeric            180  0.00 %                
        tBodyGyroJerk-std-X]**                                                       

        **[Average-                    numeric            180  0.00 %                
        tBodyGyroJerk-std-Y]**                                                       

        **[Average-                    numeric            180  0.00 %                
        tBodyGyroJerk-std-Z]**                                                       

        **[Average-                    numeric            180  0.00 %                
        tBodyAccMag-mean]**                                                          

        **[Average-                    numeric            180  0.00 %                
        tBodyAccMag-std]**                                                           

        **[Average-                    numeric            180  0.00 %                
        tGravityAccMag-mean]**                                                       

        **[Average-                    numeric            180  0.00 %                
        tGravityAccMag-std]**                                                        

        **[Average-                    numeric            180  0.00 %                
        tBodyAccJerkMag-mean]**                                                      

        **[Average-                    numeric            180  0.00 %                
        tBodyAccJerkMag-std]**                                                       

        **[Average-                    numeric            180  0.00 %                
        tBodyGyroMag-mean]**                                                         

        **[Average-                    numeric            180  0.00 %                
        tBodyGyroMag-std]**                                                          

        **[Average-                    numeric            180  0.00 %                
        tBodyGyroJerkMag-mean]**                                                     

        **[Average-                    numeric            180  0.00 %                
        tBodyGyroJerkMag-std]**                                                      

        **[Average-                    numeric            180  0.00 %                
        fBodyAcc-mean-X]**                                                           

        **[Average-                    numeric            180  0.00 %                
        fBodyAcc-mean-Y]**                                                           

        **[Average-                    numeric            180  0.00 %                
        fBodyAcc-mean-Z]**                                                           

        **[Average-                    numeric            180  0.00 %                
        fBodyAcc-std-X]**                                                            

        **[Average-                    numeric            180  0.00 %                
        fBodyAcc-std-Y]**                                                            

        **[Average-                    numeric            180  0.00 %                
        fBodyAcc-std-Z]**                                                            

        **[Average-                    numeric            180  0.00 %                
        fBodyAcc-meanFreq-X]**                                                       

        **[Average-                    numeric            180  0.00 %                
        fBodyAcc-meanFreq-Y]**                                                       

        **[Average-                    numeric            180  0.00 %                
        fBodyAcc-meanFreq-Z]**                                                       

        **[Average-                    numeric            180  0.00 %                
        fBodyAccJerk-mean-X]**                                                       

        **[Average-                    numeric            180  0.00 %                
        fBodyAccJerk-mean-Y]**                                                       

        **[Average-                    numeric            180  0.00 %                
        fBodyAccJerk-mean-Z]**                                                       

        **[Average-                    numeric            180  0.00 %                
        fBodyAccJerk-std-X]**                                                        

        **[Average-                    numeric            180  0.00 %                
        fBodyAccJerk-std-Y]**                                                        

        **[Average-                    numeric            180  0.00 %                
        fBodyAccJerk-std-Z]**                                                        

        **[Average-                    numeric            180  0.00 %                
        fBodyAccJerk-meanFreq-X]**                                                   

        **[Average-                    numeric            180  0.00 %                
        fBodyAccJerk-meanFreq-Y]**                                                   

        **[Average-                    numeric            180  0.00 %                
        fBodyAccJerk-meanFreq-Z]**                                                   

        **[Average-                    numeric            180  0.00 %                
        fBodyGyro-mean-X]**                                                          

        **[Average-                    numeric            180  0.00 %                
        fBodyGyro-mean-Y]**                                                          

        **[Average-                    numeric            180  0.00 %                
        fBodyGyro-mean-Z]**                                                          

        **[Average-                    numeric            180  0.00 %                
        fBodyGyro-std-X]**                                                           

        **[Average-                    numeric            180  0.00 %                
        fBodyGyro-std-Y]**                                                           

        **[Average-                    numeric            180  0.00 %                
        fBodyGyro-std-Z]**                                                           

        **[Average-                    numeric            180  0.00 %                
        fBodyGyro-meanFreq-X]**                                                      

        **[Average-                    numeric            180  0.00 %                
        fBodyGyro-meanFreq-Y]**                                                      

        **[Average-                    numeric            180  0.00 %                
        fBodyGyro-meanFreq-Z]**                                                      

        **[Average-                    numeric            180  0.00 %                
        fBodyAccMag-mean]**                                                          

        **[Average-                    numeric            180  0.00 %                
        fBodyAccMag-std]**                                                           

        **[Average-                    numeric            180  0.00 %                
        fBodyAccMag-meanFreq]**                                                      

        **[Average-                    numeric            180  0.00 %                
        fBodyAccJerkMag-mean]**                                                      

        **[Average-                    numeric            180  0.00 %                
        fBodyAccJerkMag-std]**                                                       

        **[Average-                    numeric            180  0.00 %                
        fBodyAccJerkMag-meanFreq]**                                                  

        **[Average-                    numeric            180  0.00 %                
        fBodyGyroMag-mean]**                                                         

        **[Average-                    numeric            180  0.00 %                
        fBodyGyroMag-std]**                                                          

        **[Average-                    numeric            180  0.00 %                
        fBodyGyroMag-meanFreq]**                                                     

        **[Average-                    numeric            180  0.00 %                
        fBodyGyroJerkMag-mean]**                                                     

        **[Average-                    numeric            180  0.00 %                
        fBodyGyroJerkMag-std]**                                                      

        **[Average-                    numeric            180  0.00 %                
        fBodyGyroJerkMag-meanFreq]**                                                 
-------------------------------------------------------------------------------------


### Acknowledgments

* makeCodebook from the package dataMaid was used to create part of this CodeBook
* [1] Davide Anguita, Alessandro Ghio, Luca Oneto, Xavier Parra and Jorge L. Reyes-Ortiz. Human Activity Recognition on Smartphones using a Multiclass Hardware-Friendly Support Vector Machine. International Workshop of Ambient Assisted Living (IWAAL 2012). Vitoria-Gasteiz, Spain. Dec 2012
