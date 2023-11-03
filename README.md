# Rossmann Sales Prediction

## 1. About Sales Prediction

In the world of retail, accurate sales prediction is key for companies like Rossmann. Sales prediction is the practice of leveraging historical data and data-driven methodologies to anticipate future sales trends, enabling businesses to make informed decisions on inventory management, marketing strategies, and resource allocation. 

## 2. About Rossmann
Rossmann, a prominent European drug store and retail chain, plays a vital role in the daily lives of countless customers across multiple countries. With a vast array of products, from cosmetics and personal care items to household essentials, Rossmann has become a go-to destination for shoppers seeking quality goods at competitive prices. 

In this data science project, I delve into the challenge of forecasting Rossmann store revenues, a task with significant implications for the company's operations and decision-making. By leveraging data-driven insights and predictive models, I aim to uncover patterns and trends that can help Rossmann optimize its business strategies and improve its performance.

## 3. Business Problem

**Business Challenge: Developing a Sales Prediction Model**

A sales prediction model for the following six weeks will be developed in order to predict how much money each store of the company will have available to spend on their renovation.

_Although the data and the company are real, the business problem is fictitious._

## 4. Data Overview

The original dataset of this project is available at [Kaggle](https://www.kaggle.com/competitions/rossmann-store-sales/data) containing data from multiple years and over a million rows. Despite this, it was decided to only use data from 2015 for this project for computational efficiency during machine learning modeling.

The main variables are described as follows:

<div align="center">

| Column name | Description |
|---|---|
| `store` | Each store has its unique ID. |
| `day_of_week` | Day of the week on which the sale was made.  |
| `date` | The exact date on which the sale was made. |
| `sales` | Whether a sale was made or not. |
| `promo` | Indicates whether the store is on promotion or not. |
| `state_holiday` | Indicates which state holiday is it or if it is none. |
| `school_holiday` | Indicates whether it is a school holiday or not. |
| `store_type` | Informs what type of store it is. |
| `assortment` | Informs the level of assortment the store has. |
| `comp_distance` | Distance in meters to the nearest competition. |
| `comp_open_since_month/year` | Indicates when the nearest competitor opened in month/year. |
| `promo2` | Indicates if the store is running a consecutive promotion. |
| `promo2_since_week/year` | Indicates how long the store has been participating in the consecutive promotion in month/year. |
| `is_promo` | Indicates whether the store is on a promotional month or not. |

</div>

## 5. Solution Plan

- **What is the problem:** the stores of the company need a renovation as a part of Rossmann's rebranding, but how much money each one of them will have available?
- **Data Description:** after importing the necessary data, conducting a brief Data Description is crucial to understand where are we heading into. This step consists in Data dimensions, how many columns on the dataset, what are the Data types, Describing data and Checking NaN.
- **Data Exploration and Preprocessing:** in this step, a Preprocessing of the dataset is run, for example Renaming columns to snake case style and making them more clear, changing the Datetime variables, Filling out NaN values on date-related columns, Changing data types to int or float, Dropping Unecessary Data for the project and other Reasonable Changes.
- **Hypotheses:** this step of the project was created to formulate thoughts about the data and its potential relationships to guide the data exploration and analysis. Several hypotheses are conduced for Stores, Products, Frequency and Time Hypotheses and the Final Hypotheses. This Final list is compiled based on the variables are available in the dataset, considering what can realistically be examined.
- **Feature Engineering:** Features Creation, Time variables and rows selection for conducing EDA.
- **Exploratory Data Analysis:** at this step, the Final list of Hypotheses are tested, describing them visually through **histograms, boxplots, bar plots, heatmaps** and so. Beyond that, a little summary on Numerical and Categorical attributes.
- **Data Preparation:** considering that we have to predict the sales for the following six-weeks, the Train-test split needs to be split by date. Other sub-steps of Data Preparation are **Filling NaN, Rescaling, Encoding and Transformations**. Later, Dropping Features that were needed to EDA but won't be necessary to Machine Learning modeling. Further, running Boruta we can select the best features for the Final Dataset.
- **Machine Learning Modeling**: in this section, the first approach is to define a Baseline Model to guide other models performances, which will be conducted through an Average Model. Then the other models are run at single performance and in Cross Validation, such as **Linear Regression**, **Lasso Regression**, **Random Forest Regressor**, **XGBoost Regressor** and **LightGBM Regressor**. For each one of them the metrics **Mean Absolute Error (MAE)**, **Mean Absolute Percentage Error (MAPE)**, **Root Mean Squared Error (RMSE)** and **Coefficient of Determination (R2)** will be calculated. Comparing the models with their metrics performances is the last part of this section.

<div align="center">
  
| Model                     | MAE     | MAPE  | RMSE    | R2  |
|---------------------------|---------|-------|---------|-----|
| LGBM Regressor            | 890.65  | 0.14  | 1268.28 | 0.83|
| Random Forest Regressor   | 954.60  | 0.15  | 1372.42 | 0.80|
| XGBoost Regressor         | 1031.40 | 0.17  | 1422.48 | 0.78|
| Average Model (Baseline)  | 1386.12 | 0.22  | 1836.36 | 0.64|
| Lasso Regression          | 2086.74 | 0.37  | 2740.73 | 0.20|
| Linear Regression         | 2088.71 | 0.37  | 2742.11 | 0.19|

</div>

- **Hyperparameter Tuning:** in this step, we run a Random Search on the parameters of the best model from the previous section to obtain the Final Model and predict the stores sales for the following six months.

<div align="center">

| Model                     | MAE     | MAPE  | RMSE    | R2  |
|---------------------------|---------|-------|---------|-----|
| LGBM Regressor            | 885.55  | 0.14  | 1272.60 | 0.83|

</div>

- **Business Performance** in this step, the main objective is to show the Financial Performance of the choosen Model and what it means in monetary values.

<div align="center">

| Scenario        | Values           |
|-----------------|------------------|
| Prediction      | $295,581,222.65  |
| Worst Scenario  | $287,416,916.76  |
| Best Scenario   | $303,745,528.54  |

</div>

## 6. Conclusion and Recommendations
In conclusion, this Data Science project has successfully delivered a Sales Prediction Model in order to optimize resource allocation for Rossmann store renovations. 

Through a complete Exploratory Data Analysis, the company gained valuable insights into the factors influencing sales, providing a solid foundation for decision-making.

However, it's worth noting that the project's potential could be further maximized with a larger dataset. While it's focused on the year 2015 for computational efficiency, the complete dataset contains over 1 million rows, significantly more than the 236k rows of data used in this analysis. This could have had significant implications for the under-performance of cross-validation.

Throughout the project, various Machine Learning models were evaluated, but future efforts could explore alternative methodologies. For example, forecasting the number of customers and incorporating this data into the model could be a promising avenue for further research. 

As Rossmann continues to evolve,the insights gained here offer a robust foundation for informed decision-making and future data-driven projects.




