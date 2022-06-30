# Mercedes-Benz-Greener-Manufacturing-with-Machine-Learning
Car Testing Time Predictions using Machine Learning Model

# 1.Project overview:
* Problem Statement Scenario: 
Since the first automobile, the Benz Patent Motor Car in 1886, Mercedes-Benz has stood for important automotive innovations. These include the passenger safety cell with a crumple zone, the airbag, and intelligent assistance systems. Mercedes-Benz applies for nearly 2000 patents per year, making the brand the European leader among premium carmakers. Mercedes-Benz is the leader in the premium car industry. With a huge selection of features and options, customers can choose the customized Mercedes-Benz of their dreams.

To ensure the safety and reliability of every unique car configuration before they hit the road, the company’s engineers have developed a robust testing system. As one of the world’s biggest manufacturers of premium cars, safety and efficiency are paramount on Mercedes-Benz’s production lines. However, optimizing the speed of their testing system for many possible feature combinations is complex and time-consuming without a powerful algorithmic approach.

You are required to reduce the time that cars spend on the test bench. Others will work with a dataset representing different permutations of features in a Mercedes-Benz car to predict the time it takes to pass testing. Optimal algorithms will contribute to faster testing, resulting in lower carbon dioxide emissions without reducing Mercedes-Benz’s standards.

### 2.Mapping the problem to Machine Learning: 
The basic problem statement as described above is to create a machine learning model that will predict the accurate time a car spends on the test bench. The car configuration is nothing but selected various customization options available and the features for a particular car. Accurate models will help to reduce the total time spent on testing by allowing the vehicles with the same configurations to test successively.
* Data Overview:This dataset contains an anonymized set of variables, each representing a custom feature in a Mercedes car. The ground truth is labeled ‘y’ and       represents the time (in seconds) that the car took to pass testing for each variable.
* Dataset: train.csv — Contains the training set with 4209 rows (data points) and 378 columns (features) with labels. test.csv — Contains the test set with 4209 rows (data points) and 377 columns (features) with no labels.
* Machine Learning model: Type of Machine Learning Problem is Regression analysis(supervised machine learning) since we want to predict the testing time with a labelled dataset.
  
### 3.Exploratory Data Analysis(EDA):
* Analysis of train data reveals 368 binary features with 8 categorical variables, Dataset has no missing values, perfomred outlier treatment on target variable and removed columns with zero variance. Encoded categorical features using label encoder for machine learning model.
* Analysis of test data reveals 377 features with 8 categorical variables, dataset with no missing values, label encoded the categorical features and dropped the variables from test data as we have dropped them from train dataset.
* PCA(Principal Component Analysis): Since our dataset suffers from curse of dimensionaltiy applying PCA for dimensinality reduction seems an apt choice. Performed PCA on both train and test data.

### 4.Tools and technologies used:
* Python Version: 3.8.5
* Packages and Libraries used:- 
  * a. Visualization libraries : Matplotlib,Seaborn
  * b. Data Analysis,arrays,dimendion reduction: Numpy,Pandas, PCA
  * c. Scaling,Model building,accuracy metric check: Scikit learn   

### 5. Performance Metric:
* Machine learning model used: XGBoost regressor model with RandomizedSearchCV for hyper parameter tuning to find best parameters for better accuracy.
*  Validation R-Square: 0.36
