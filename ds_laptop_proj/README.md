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
6. Productionisation

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
Various graphs and charts are created to better understand the dataset. Below are the highlights from graphs and interpretations.

* Looking at the correlation, number of ratings and number of reviews are highly correlated. These two variables have negative correlation with price. The scatter chart shows that higher-priced laptops get fewer reviews and ratings. Probably because they are sold less. 
<img src="https://github.com/suaydin17/ds_laptop_proj/assets/132287565/e8e34acc-64d9-446e-a04d-763743d4131f" width="300" /> 

* Relations between important variables and price are shown in below figures.
<p float="left">
  <img src="https://github.com/suaydin17/ds_laptop_proj/assets/132287565/36ffd112-c082-44fc-9fc1-10552d7c33a3" width="500" />
  <img src="https://github.com/suaydin17/ds_laptop_proj/assets/132287565/5e969b01-8c59-472f-8d9f-1ad27c443d8a" width="500" /> 
</p>
<p float="left">
  <img src="https://github.com/suaydin17/ds_laptop_proj/assets/132287565/a15c0433-7396-4851-8cb9-fa97270842fd" width="500" />
  <img src="https://github.com/suaydin17/ds_laptop_proj/assets/132287565/e0d6de60-63d8-4b78-a71b-ede675160e89" width="500" /> 
</p>
<p float="left">
  <img src="https://github.com/suaydin17/ds_laptop_proj/assets/132287565/dea2cf4a-c531-4a2b-b367-5de715918299" width="500" />
  <img src="https://github.com/suaydin17/ds_laptop_proj/assets/132287565/f39f54f0-497e-4b1c-b36a-bbf6d31ae13a" width="500" /> 
</p>
<p float="left">
  <img src="https://github.com/suaydin17/ds_laptop_proj/assets/132287565/0978160f-88c1-4fb1-9d09-e4c1231380b9" width="500" />
  <img src="https://github.com/suaydin17/ds_laptop_proj/assets/132287565/14feb88d-2d7a-4bee-bccd-9a368f46bbe6" width="500" /> 
</p>
<p float="left">
  <img src="https://github.com/suaydin17/ds_laptop_proj/assets/132287565/9f855b6d-a11c-4614-a1af-41f7bb479ea6" width="500" />
  <img src="https://github.com/suaydin17/ds_laptop_proj/assets/132287565/2ff83692-bc93-4204-b284-2bf63932204e" width="500" /> 
</p>

* Higher price laptops mostly get 3 or 4 stars.
<p float="left">
  <img src="https://github.com/suaydin17/ds_laptop_proj/assets/132287565/332c7667-a13d-4e60-aa7e-b7d572218b47" width="500" />
  <img src="https://github.com/suaydin17/ds_laptop_proj/assets/132287565/fa37d2ea-5bdb-4d4e-ae61-03ac0f9ebf72" width="500" /> 
</p>

* Distribution of brands and processor brands.
<p float="left">
  <img src="https://github.com/suaydin17/ds_laptop_proj/assets/132287565/3cd1d60e-b552-462b-9386-3023bd64bc37" width="500" />
  <img src="https://github.com/suaydin17/ds_laptop_proj/assets/132287565/cf5b630d-16ce-44bf-bf18-0e5ce703ed7b" width="500" /> 
</p>

* Various bar plot and pivot table interpretations.
<img src="https://github.com/suaydin17/ds_laptop_proj/assets/132287565/e8d5592a-0983-4e84-958d-12eb9b6b0857" width="500" />
<img src="https://github.com/suaydin17/ds_laptop_proj/assets/132287565/0fb54b7d-ef82-4aa0-8d80-ab446a365e85" width="500" /> 
<img src="https://github.com/suaydin17/ds_laptop_proj/assets/132287565/91a7fe30-0526-4a7f-9e6e-203cde63b3d8" width="500" /> 

<img src="https://github.com/suaydin17/ds_laptop_proj/assets/132287565/237ebf84-d4fe-40cd-b574-6711c854cf48" width="200" /> 

## Model Building
* Categorical variables are turned into dummy variables. 
* Dataset split into train and test sets. 
* Multiple linear regression model is created using statsmodels. Adj. R-squared value is 0.823, which means that approximately 83.6% of the variability in the dependent variable can be explained by the independent variables included in the model. Prob (F-statistic): This is the p-value associated with the F-statistic. A low p-value suggests that the observed F-statistic is unlikely to occur by chance, further supporting the statistical significance of the regression model. Standard Errors: These indicate the standard deviation of the estimated coefficients. Larger standard errors suggest greater uncertainty in the coefficient estimates. P>|t|: These p-values represent the probability that the corresponding coefficient is not significantly different from zero. Lower p-values (typically below a predetermined significance level, such as 0.05) suggest that the coefficient is statistically significant.
* Multiple linear regression model is created using sklearn. Inıtıal Linear Regression model gives the score of 0.7347. Better score is obtained after using cross validation. R-squared value of 0.7788 suggests that approximately 77.88% of the variance in the target variable (price) can be explained by the features used in the model.


## Results
Linear Regression, Lasso Regression, Decision Tree Regression and Random Forest Regression models are tried and compared. Random Forest Model gives the best score out of all four. So, it is used for prediction.

* **Linear Regression:** score: 0.778824, best parameters: {'normalize': False}

* **Lasso Regression:** score: 0.783527, best parameters: {'alpha': 1, 'max_iter': 1000, 'selection': 'r...}

* **Decision Tree Regression:** score: 0.623888, best parameters: {'criterion': 'mse', 'splitter': 'random'}

* **Random Forest Regression:** score: 0.819445, best parameters: {'criterion': 'mse', 'max_features': 'sqrt', '...}, mean absolute error: 136.68

## Productionisation
During this step, a Flask API endpoint that is hosted on a local webserver is developed. The API endpoint is designed to receive a request containing list of values from the laptop dataset. Upon receiving the request, the API processes the data and returns a predicted price based on the provided laptop information.

