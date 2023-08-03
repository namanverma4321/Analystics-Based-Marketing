# Loyalty Program Data Analysis using Logistic Regression

This repository contains code for analyzing the data of a loyalty program run by ABC Supermarket. In this program, promotional kits were given to 10% of customers, and it was recorded whether they made a purchase or not using logistic regression.

## Data Description
The dataset used for this analysis contains the following columns:

- `DemAffl`: Demographic Affluence score
- `DemAge`: Demographic Age
- `DemClusterGroup`: Demographic Cluster Group
- `DemGender`: Demographic Gender
- `DemReg`: Demographic Region
- `DemTVReg`: Demographic TV Region
- `LoyalClass`: Loyalty Class
- `LoyalSpend`: Loyalty Spending
- `LoyalTime`: Loyalty Time
- `TargetBuy`: Target variable indicating whether the customer made a purchase (1) or not (0)

## Code Overview
The code is written in Python and is divided into the following sections:

1. Importing Libraries and Loading the Data: The necessary libraries are imported, and the dataset is loaded from the "Dataset_Train.xlsx" file.

2. Data Visualization: Various visualizations, such as bar charts and histograms, are created to gain insights into the data distribution and relationships between variables.

3. Data Preparation: Missing values in the dataset are handled by filling them with appropriate values, and categorical variables are converted to numeric using Label Encoding.

4. Checking for Multicollinearity: The Variance Inflation Factor (VIF) is calculated to check for multicollinearity between the independent variables.

5. Sampling Unbalanced Data: The dataset is balanced using Synthetic Minority Over-sampling Technique (SMOTE) to handle the class imbalance.

6. Model Building: Logistic Regression is used to build the classification model, and the model is saved using joblib for future use.

7. Model Evaluation: The model is evaluated using confusion matrix and accuracy score on the test data.

8. Exporting Model Output: Model predictions along with probabilities are written to an Excel file ("ModelOutput_Train.xlsx").

## Excel file Overview
After building the logistic regression model, the Excel file ("ModelOutput_Train.xlsx") provides additional insights and recommendations based on the model's predictions:

1. Decile Method: We use a decile method to divide the customers based on their predicted probabilities of making a purchase. This method creates ten groups or deciles of customers ranked by their probability scores.

2. Customer Ranking: The top 10% of customers are ranked as 1, the next 10% as 2, and so on for all customers.

3. Profit Optimization: We determine the probability threshold that maximizes profit.
   

