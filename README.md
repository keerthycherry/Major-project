# Major-project
# Data-Preprocessing-Framework-For-Supervised-Machine-Learning

Data preprocessing is a process of preparing the raw data and making it suitable for a machine learning model. It is the first and crucial step while creating a machine learning model.When creating a machine learning project, it is not always a case that we come across the clean and formatted data. And while doing any operation with data, it is mandatory to clean it and put in a formatted way. So for this, we use data preprocessing task.A real-world data generally contains noises, missing values, and maybe in an unusable format which cannot be directly used for machine learning models. Data preprocessing is required tasks for cleaning the data and making it suitable for a machine learning model which also increases the accuracy and efficiency of a machine learning model.

# DataSet

Context: Predict next-day rain by training classification models on the target variable RainTomorrow.

Content: This dataset contains about 10 years of daily weather observations from many locations across Australia. RainTomorrow is the target variable to predict. It means -- did it rain the next day, Yes or No? This column is Yes if the rain for that day was 1mm or more.
There are 21 features in the data set. 
['Location','MinTemp','MaxTemp','Rainfall','Evaporation','Sunshine','WindGustDir','WindGustSpeed','WindDir9am','WindDir3pm','WindSpeed9am','WindSpeed3pm','Humidity9am','Humidity3pm','Pressure9am','Pressure3pm','Cloud9am','Cloud3pm','Temp9am','Temp3pm','RainToday‘,’RainTomorrow’]
There are 1,45,460 rows in the data set.


![image](https://user-images.githubusercontent.com/63137589/121795831-e5744c00-cc31-11eb-8262-7aa47c413725.png)


## Implementation

Jupyter Lab is used for implementation.

### Exploratory Data Analysis

EDA to understand the nature of the data and decide what data Pre-processing algorithms to be used. The techniques used in this stage include the following:
    To take a closer look at the data took help of “ .head()”function of pandas library which returns first five observations of the dataset. Similarly “.tail()” returns last five observations of the data set.
    Total number of rows and columns in the data set using “.shape”.
    The independent and dependent variables in the dataset are found and the .info( ) method is used to find the information about the data set such as  the data type and the number of non- null values in each feature.
 various summary statistics are found for each feature . The summary statistics include count, mean, standard deviation, minimum and maximum values and the quantiles of the data.
The cardinality and the unique values in each feature are calculated . The number of null values in each feature are calculated and their distribution s analyzed using a matrix and a heat map.


### Data Cleaning

Following tasks are performed in data cleaning : 
  .The number of missing values in each row of the data set are computed and the rows containing more than 50% missing values are dropped. 
Duplicate records are eliminated to avoid redundancy in the dataset.
The missing values in continuous features are substituted by mean.
The missing values in categorical features are substituted by mode.
The percentage of null values in the dataset are evaluated after handling missing data to crosscheck whether all the missing values are handled properly or not.
HANDLING NOISY DATA(outliers): 
Outliers are detected using Z-Score and has been removed.
These are the tasks performed in Data cleaning, later the cleaned dataset is displayed on desktop and this cleaned dataset is further used in preprocessing.

### Data Transformation

The following steps were implemented for data transformation:
 The encoding feature is chosen based on the cardinality of the feature. Cardinality is the number of unique values in each feature. Integer encoding was used to convert each categorical feature into numerical type.
 .round( ) method is used for all the floating type value features to rounded off to nearest  integers to avoid complexity.
 The data set is split into training and test data sets. The test dataset size is 33 percent and the training data set is 67 percent. Random Sampling is used for splitting the dataset.
 Feature selection is performed in order to select the best features that are more useful for predicting the target attribute. ANOVA f-test was used to find the scores for the features. According to the feature scores top 10 features were selected and the remaining are discarded.
 Random forest classifier was applied to determine the target feature for test data and the accuracy was evaluated.
 Logistic Regression is applied to determine the target feature for test data and the accuracy was evaluated.
 
# Conclusions
▪ The Pre-processed Set produced 85% accuracy to predict the target feature with random forest classifier 
▪ The pre-processed Data Set produced 84% accuracy to predict the target feature with Logistic Regression algorithm. 
▪ The data cleaning method used removed all the insignificant rows from the data set and was able to calculate the missing values in an   effective manner. 
▪ The data pre-processing strategy used to pre-process the Australian weather data. We used a combination of existing methods for data     cleaning which gave better results. 
▪ We also performed exploratory data analysis (EDA). The encoding technique is based on cardinality of particular categorical feature. 
▪ We used ANOVA F classification function for feature selection as it is used mainly when target attribute is for classification problems. This methodology and choice of algorithm has produced 85 percent of accuracy on the test data for random forest classification algorithm 
▪ The data pre-processing techniques used have a huge impact on the performance of a machine learning algorithm. Therefore, it is very crucial to choose the proper data pre-processing algorithms. 
▪ The proper choice can only be made by thoroughly understanding the nature of the data and the relationship between various features in the data set. 







