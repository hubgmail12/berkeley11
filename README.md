# berkeley11

The purpose of this exercise is to help dealerships to identify what features customers value more.

This exercise has the following file structure

- Data Folder
    - vehicles,csv : This is the original dataset
    - cleanup_car.csv : This is the cleaned version of the original dataset

- images Folder:
    - This folder contains the images used within the original csv file

prompt_II-amin1-take6.ipynb notebook containing the code.


Approach:
- Data Explorer and clean up:

As the 1st step, we explored the data to better understand the quality of the dataset. This insection included:
- Determined Null fields
- Transformed features from object to int64
- Used mean to update null fields when possible
- Based on car type or other features, determined what some of the values should be replaced with in null fileds
- Once completd, then created a new CSV file called cleanup_car

- Modeling & Evalution:
- This was more complicated since I had to repeat this step multiple times. I originally used following models
    - Linear Regression
    - Ridge
    - LASSO
    - Forest

The Best Model for this exercise happened to be Forest, However, my laptop could not handle running Foest and it would crash ater 30 inutes.

The next best Model is Linear Regression.

I used kFold Cross Validation with Liner Rregreeion and Ridge ( including GridSearchCV with Ridge). The first 3 times, based on the data my modeling was overfitted.
To fix overfitting issues, I reduced number of features, until training and test MSE become in acceptable range.


I finally Ran the Model and reported the reslts in Jupyter notebook markdowns.

Please try this and remeber, there are few more approaches can be made if there is additional time:
- Alter the data set further by determining he correlations and choose your datset based on that
- Remove some of the features entirely insetad of using Mode / Mean method to populate as this could skew the results.

Please enjoy and if you need any help, do not hestiate to contact me.

