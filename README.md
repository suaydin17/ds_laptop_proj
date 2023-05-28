# DATA SCIENCE LAPTOP PRICE ESTIMATOR

## Project Overview
* Created a tool to precdict laptop prices.
* Kaggle Laptop Prices Dataset is used.
* Data is cleaned, exploratory data analysis is done.
* Optimized Linear, Lasso, Decision Tree and Random Forest Regressors using GridSearchCV to create the best model.
* Built a client facing API using flask.

## Table of Contents

1. Code and Resources Used
2. Data Cleaning
3. Exploratory Data Analysis (EDA)
4. Model Building
5. Results

## Code and Resources Used
This data science project was implemented using the following code and resources:

**Programming Language:** Python 3.9

**IDE/Editor:** PyCharm Community Edition

**Libraries and Packages:**
pandas (version 1.3.0)
numpy (version 1.21.0)
matplotlib (version 3.4.2)
seaborn (version 0.11.1)
scikit-learn (version 0.24.2)
statsmodels (version 0.12.2)

The project code utilizes various Python libraries for data cleaning, exploratory data analysis, and model building tasks. The versions of the libraries used during development are mentioned above.

You can find the complete code implementation, including data cleaning scripts, EDA notebooks, and model building files, in the GitHub repository.

## Data Cleaning
In this project, the following steps were performed to clean and preprocess the data:

* Checking the shape of the dataset. Providing an overview of dataset's dimensions, including the number of rows and columns.
* Removing duplicate rows. Duplicate rows, if any, were identified and removed from the dataset to ensure data integrity and avoid redundancy.
* Inspecting the dataset information, gaining insights into the data types of each column and identify any missing values or inconsistencies.
* To facilitate analysis, the prices were converted to USD by dividing the original price values by the current exchange rate.
* Histograms were created to visualize the distribution of three numerical variables in the dataset. The histograms revealed that the distributions were right-skewed, indicating the presence of outliers. Outliers are handled by filling with appropriate values.
* Checking descriptive statistics. Providing a summary of the numerical variables' descriptive statistics, including count, mean, standard deviation, minimum, quartiles, and maximum values.

These data cleaning steps aimed to ensure the quality and consistency of the dataset and prepare it for subsequent exploratory data analysis (EDA) and model building phases.

## Exploratory Data Analysis (EDA)
Provide an overview of the exploratory data analysis conducted on your dataset. Describe the visualizations, statistical analyses, or data exploration techniques used to gain insights into the data. Highlight any interesting patterns, correlations, or observations discovered during the EDA phase.

Model Building
Outline the process of building your machine learning model. Describe the algorithms, techniques, or frameworks used for training and evaluating the model. Include relevant code snippets or configuration details. If applicable, mention any hyperparameter tuning or model selection strategies employed.

Results
Present the results and performance metrics of your trained model. Include any visualizations, tables, or graphs that demonstrate the model's accuracy, precision, recall, or other relevant evaluation metrics. Discuss the significance of the results and how they align with your project objectives.


