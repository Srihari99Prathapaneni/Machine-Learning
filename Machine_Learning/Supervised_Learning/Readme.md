# Simple Linear Regression

- Steps followed for SLR:

1. Import required python libraries
    - Inspected various aspects of the DataFrame.

2. Visualising the Data
    - Plotted pairplot and heatmap to find the highest correlation amoung the variables.

3. Performing Simple Linear Regression
    - Splited dataframe into train and test datasets.
    - Linear model is build using statsmodel.
    - Verified some key statistics from summary.

4. Residual Analysis
    - Validated assumptions of the model.

5. Predictions on the Test dataset
    - Performed prediction on test dataset and calculated RMSE & R-Squared.
    - Finally visualized the fit on test dataset.

# Multiple Linear Regression

- Steps followed for MLR:

1. Import Required libraries
    - Inspeted various aspects of dataset.

2. Data visualization on dataset
    - Performed the data visualization on dataset to find correlation as pairplot and heatmap.

3. Data Cleaning
    - Converted Binary data into Numerical data.
    - Applied get_dummy function on the dummy variables.
    - Concatenated the original dataset with dummy dataset after removing unneccessary variables.

4.  Split dataset and Build MLR Model
    - Splited the data set into Train and Test datasets.
    - Performed the Rescaling on Train dataset.
    - Again splited X_train and y_train to build the model.
    - Used add_constant and OLS methods to build model by using statsmodel.
    - Verified the variables with help of summary().
    - Removed variables which are higher values of P-values (>0.05).

5.  VIF (Variance Inflation Factor)
    - calculated vif on trained data to remove features which ara having > 5.
    
6. Rebuild the model
    - Repeated the building model mulptiple times untill variables all are less than the permissible limit and i have done this process on one variable at time, because of impact of one variable on another will be possible.

7.  Prediction on Train dataset
    - Applied the prediction function on the Trained dataset.

8. Residual Analysis
    - Verified the assumption of linear regression that mean of normal distribution is zero.

9. Model Evaluation
    - Rescaled neccessary features of test dataset.
    - bifurcated test dataset into X_test and y_test.
    - Removed a few features as they are violates the VIF's and P-values permmisible limit.
    - Used add_constant on X_test and OLS method on X_test with Fit() method to fit the line on model.
    - Made prediction on the X_test model.
    - Finally plotted scatter plot on y_test and y_test_pred variables to understand Linear Regression of the model.

# Multiple Linear Regression (RFE - Recursive Feature Elimination)

- Steps followed for MLR using RFE

1. Steps 1 & 2 & 3 are same as multiple linear regression.

2. Split dataset and Build Model
    - Splited the data set into Train and Test datasets.
    - Performed the Rescaling on Train dataset.
    - Again splited X_train and y_train to build the model.
    - Built the model using LinearRegression and fit() methods.
    - Used RFE() method to to check features are in under permissible limit or not. here we applied the RFE on a few variables.
    - Removed varibles which violates the limits of P-value and VIF.
    - Now verified the summary() and identified the varibles which re violating the limits and removed.
    - Once again performed the VIF's on Remaing variable on train dataset and removed violatable features as one by one with reapeating the process.

3. Steps 7 & 8 & 9 are same as multiple linear regression.



# Logistic Regression

 - Steps followed for Logistic Regression:

1. Import Required Libraries
    - Imported pandas, numpy, matplotlib, seaborn, and statsmodels.
    - Loaded the dataset(s) and merged them into a single master dataframe.

2. Inspect the Dataset
    - Viewed the first few rows with .head().
    - Checked shape, summary statistics with .describe(), and data types with .info().
    - Identified categorical and numerical variables.

3. Data Cleaning
    - Converted binary categorical variables (Yes/No) into numerical (1/0).
    - Applied get_dummies() for multi-level categorical variables.
    - Concatenated dummy variables with the main dataset and dropped redundant columns.
    - Converted string-based numeric columns (like TotalCharges) into float using pd.to_numeric().
    - Handled missing values (removed rows with NaN in TotalCharges).

4. Train-Test Split
    - Defined X (independent variables) and y (dependent variable: Churn).
    - Split into training and testing sets using train_test_split() with 70:30 ratio.

5. Feature Scaling
    - Applied StandardScaler to continuous variables (tenure, MonthlyCharges, TotalCharges).
    - Ensured scaling was done only on training data, then applied the same transformation to test data.

6. Correlation Analysis
    - Visualized correlations with a heatmap.
    - Dropped highly correlated dummy variables to avoid multicollinearity.

7. Model Building
    - Built the initial logistic regression model using statsmodels.api.GLM() with Binomial family.
    - Checked model summary for coefficients, p-values, and pseudo R².
    - Removed variables with high p-values (>0.05).

8. Feature Selection (RFE)
    - Applied Recursive Feature Elimination (RFE) with LogisticRegression() to select top predictors.
    - Retained features marked as important by RFE.

9. Rebuild the Model
    - Rebuilt logistic regression with selected features.
    - Iteratively refined by checking p-values and removing insignificant variables.

10. Model Evaluation
    - Predicted probabilities on training and test sets.
    - Conducted residual analysis and checked assumptions.
    - Evaluated performance using confusion matrix, accuracy, precision, recall, and ROC-AUC.
    - Plotted ROC curve to visualize classification performance.