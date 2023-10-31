# rossmann
Business Challenge: Developing a Sales Prediction Model. A sales prediction model for the following six weeks will be developed in order to predict how much money each store of the company will have available to spend on their renovation.



**Table of contents**
- Rossmann Sales Prediction
  - About Sales Prediction
  - About Rossmann
  - Business Problem
  - Imports
    - Libraries  
    - Settings
    - Functions    
    - Dataset  
  - Data Description   
    - Data dimensions   
    - Columns   
    - Data types    
    - Describing data
    - Checking NaN
  - Data Exploration and Preprocessing
    - Renaming columns
    - Datetime variable
    - Filling out NaN values on date-related columns
    - Changing data types
    - Dropping Unecessary Data
    - Reasonable Changes
  - Hypotheses
    - Stores Hypotheses
    - Products Hypotheses
    - Frequency and Time Hypotheses 
    - Final Hypotheses
  - Feature Engineering 
    - Features Creation
  - Exploratory Data Analysis
    - Describing the dataset
    - Sales Histogram
    - Hypothesis Testing
        - **H1:** Stores with higher assortment level are supposed to sell more.
        - **H2:** Stores with higher number of nearby competitors are supposed to sell less.
        - **H3:** Stores with competitors for a longer period of time sell more.
        - **H4:** Stores that keep promotions for longer periods are supposed to sell more.
        - **H5:** Stores that participate in more consecutive promotions are supposed to sell more.
        - **H6:** Regular days sell less than holidays on average. 
        - **H7:** Stores are supposed to sell more before the 15th day of each month.
        - **H8:** Stores are supposed to sell less during the weekend on average.
        - **H9:** Stores are supposed to sell less during school holidays.
    - Final List of Hypotheses
    - Numerical Attributes
    - Categorical attributes
    - Summary statistics
  - Data Preparation
    - Train-test split
      - Split by date  
    - Filling NaN
    - Rescaling
    - Encoding
    - Transformations
    - Dropping Features
    - Best Features from Boruta
    - Final Dataset
  - Machine Learning Modeling
    - Average Model (baseline model)
    - Linear Regression
      - Linear Regression - Cross Validation
    - Lasso Regression
      - Lasso Regression - Cross Validation
    - Random Forest Regressor
      - Random Forest Regressor - Cross Validation
    - XGBoost Regressor
      - XGBoost Regressor - Cross Validation
    - LightGBM Regressor
      - LightGBM Regressor - Cross Validation
    - Comparing Models
  - Hyperparameter Tuning
    - Random Search
    - Final Model
  - Business Performance
    - Financial Performance
    - Total Performance
  - Conclusion and Recommendations




