# Verve-Group-case-study

##### 1. Imagine that you were asked to use this dataset to build a classification model, with gender as the target. Look at the information we have given you and identify 3-5 potential problems you can see with the provided dataset that might make building a classification model difficult.

#### Problem 1. 
The first problem that might make building the classification model difficult is the imbalanced dataset. Because there are over twice as many males as females, the model is likely going to favour predicting users as being male.
#### Problem 2. 
There are many categories for the app and ad categories, many of which have few samples, <100. These may not be enough to allow the model to pick up on any potential trends corresponding to the individual categories.
#### Problem 3.
There are only 18 samples where the ad was clicked. With such a small number, it is possible that due to pure coincidence, a large proportion of one of the genders may have clicked on the ad. This can skew training results and lead to overfitting. 
#### Problem 4. 
The number of independent variables relevant to the prediction is only equal to 3: app category, ad category, and interaction with app. Given the overlap between males and females for each of these categories (i.e.: although females may be more likely to receive beauty ads than males, a significant number of males will receive them as well), there is not enough data for accurate predictions.
Note: If we are able to extract device model (Ex. iPhone 12, oneplus 7T.) information from device_name we can use it as a feature. But in this case device_name has lot of missing values around 60% so it is better not use this feature unless we have good filling strategi. 
#### Problem 5.
App category and add category have missing values. It is important to handle missing values before model training because some models can handle them (Ex. XGBoost), but some are not.
#### Problem 6.
Given the already mentioned issues, a dataset of only 3700 samples is probably too small to allow for training a reliable model. 
