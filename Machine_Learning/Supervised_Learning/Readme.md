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
    - finally visualized the fit on test dataset.

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
    - Splited the data set into Train and Test datasets
    - performed the Rescaling on Train dataset.
    - again splited X_train and y_train to build the model
    - Used add_constant and OLS methods to build model by using statsmodel
    - Verified the variables with help of summary()
    - removed variables which are higher values of P-values (>0.05)

5.  VIF (Variance Inflation Factor)
    - calculated vif on trained data to remove features which ara having > 5
    
6. Rebuild the model
    - repeated the building model mulptiple times untill variables all are less than the permissible limit and i have done this one vriable at time because of impact of one variable on other will be possible

7.  Prediction on Train dataset
    - applied the prediction function on the Trained dataset

8. Residual Analysis
    - verified the assumption of linear regression that mean of normal distribution is zero.

9. Model Evaluation
    - Rescaled neccessary features of test dataset
    - bifurcated test dataset into X_test and y_test.
    - Removed a few features as they are violates the VIF's and P-values permmisible limit.
    - Used add_constant on X_test and OLS method on X_test with Fit() method to fit the line on model.
    - Made prediction on the X_test model.
    - Finally plotted scatter plot on y_test and y_test_pred variables to understand Linear Regression of the model.

