# DATA SCIENCE LAPTOP PRICE ESTIMATOR

## Project Overview
* Created a tool to precdict laptop prices.
* Kaggle Laptop Prices Dataset is used.
* Data is cleaned, exploratory data analysis is done.
* Optimized Linear, Lasso, Decision Tree and Random Forest Regressors using GridSearchCV to create the best model.
* Built a client facing API using flask.

# Table of Contents
1. Code and Resources Used
2. Data Cleaning
3. Exploratory Data Analysis (EDA)
4. Model Building
5.Results

# Code and Resources Used
This data science project was implemented using the following code and resources:

**Programming Language:** Python 3.9

**IDE/Editor:** PyCharm Community Edition

**Libraries and Packages:** pandas (version 1.3.0) numpy (version 1.21.0) matplotlib (version 3.4.2) seaborn (version 0.11.1) scikit-learn (version 0.24.2) statsmodels (version 0.12.2)

The project code utilizes various Python libraries for data cleaning, exploratory data analysis, and model building tasks. The versions of the libraries used during development are mentioned above.

You can find the complete code implementation, including data cleaning scripts, EDA notebooks, and model building files, in the GitHub repository.

# Data Cleaning
In this project, the following steps were performed to clean and preprocess the data:

* Checking the shape of the dataset. Providing an overview of dataset's dimensions, including the number of rows and columns.
* Removing duplicate rows. Duplicate rows, if any, were identified and removed from the dataset to ensure data integrity and avoid redundancy.
* Inspecting the dataset information, gaining insights into the data types of each column and identify any missing values or inconsistencies.
* To facilitate analysis, the prices were converted to USD by dividing the original price values by the current exchange rate.
* Histograms were created to visualize the distribution of three numerical variables in the dataset. The histograms revealed that the distributions were right-skewed, indicating the presence of outliers. Outliers are handled by filling with appropriate values.
* Checking descriptive statistics. Providing a summary of the numerical variables' descriptive statistics, including count, mean, standard deviation, minimum, quartiles, and maximum values.
* These data cleaning steps aimed to ensure the quality and consistency of the dataset and prepare it for subsequent exploratory data analysis (EDA) and model building phases.

# Exploratory Data Analysis (EDA)
Various graphs and charts are created to better understand the dataset. Below are the highlights from graphs and interpretations.

# Model Building
* Categorical variables are turned into dummy variables.
* Dataset split into train and test sets.
* Multiple linear regression model is created using statsmodels. Adj. R-squared value is 0.823, which means that approximately 83.6% of the variability in the dependent variable can be explained by the independent variables included in the model. Prob (F-statistic): This is the p-value associated with the F-statistic. A low p-value suggests that the observed F-statistic is unlikely to occur by chance, further supporting the statistical significance of the regression model. Standard Errors: These indicate the standard deviation of the estimated coefficients. Larger standard errors suggest greater uncertainty in the coefficient estimates. P>|t|: These p-values represent the probability that the corresponding coefficient is not significantly different from zero. Lower p-values (typically below a predetermined significance level, such as 0.05) suggest that the coefficient is statistically significant.

# Results
Present the results and performance metrics of your trained model. Include any visualizations, tables, or graphs that demonstrate the model's accuracy, precision, recall, or other relevant evaluation metrics. Discuss the significance of the results and how they align with your project objectives.
