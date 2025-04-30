# Sales Prediction - Machine Learning Project

## Project Overview
The goal of this project is to predict the daily sales for retail stores based on various features, including store type, promotional offers, rival store proximity, and historical sales data. The project uses both **Linear Regression** and **Random Forest Regressor** models to train on the dataset and evaluate their performance on test data.

## Dataset Description
The dataset consists of two CSV files: one for training data (`train.csv`) and one for store-specific information (`store.csv`). Below is a description of the relevant columns:

### Training Data (`train.csv`)
- **Store_id**: A unique identifier for each store.
- **RetailType**: The category or type of retail store (e.g., grocery, clothing, electronics).
- **Stock variety**: The range of products offered by the store (e.g., basic, extended, premium).
- **DistanceToRivalStore**: Distance from this store to its nearest rival store.
- **RivalOpeningMonth**: The month when a rival store opened in proximity.
- **RivalEntryYear**: The year when the rival store entered the market.
- **ContinuousBogo**: Whether a "Buy One Get One" (BOGO) offer is active (binary flag).
- **ContinuousBogoSinceWeek**: The number of weeks since the BOGO offer started.
- **ContinuousBogoSinceYear**: The year when the BOGO offer started.
- **ContinuousBogoMonths**: The duration in months for which the BOGO offer has been active.
- **DayOfWeek**: The day of the week when the sales data was recorded.
- **Date**: The date on which the sales data was collected.
- **Sales**: The total sales made by the store on that day.
- **NumberOfCustomers**: The number of customers who visited the store.
- **Is Open**: A binary flag indicating whether the store was open (1 for open, 0 for closed).
- **BOGO**: A flag indicating if BOGO offers were active on the given day.
- **Holiday**: A binary flag indicating if the day was a recognized holiday.

### Store Data (`store.csv`)
- Contains additional details about each store, such as location, type, and other relevant information that may affect sales.

## Project Tasks
1. **Data Loading**: Read and clean the dataset by merging the training data and store data on `Store_id`.
2. **Preprocessing**:
   - Handle missing values in columns like `DistanceToRivalStore` using median imputation.
   - Extract relevant date features (Year, Month, Day, WeekOfYear).
   - Remove unnecessary columns.
3. **Model Training**: 
   - Split the dataset into training and test sets (70% train, 30% test).
   - Train and evaluate both **Linear Regression** and **Random Forest Regressor** models.
4. **Feature Importance**: Use the Random Forest model to analyze feature importance and identify the most influential features for predicting sales.

## Installation and Requirements
To run this project, you need to have the following Python libraries installed:
- pandas
- numpy
- scikit-learn
- matplotlib

You can install them using pip:

```bash
pip install pandas numpy scikit-learn matplotlib
```
**Model Evaluation**:

Linear Regression:
RMSE (Root Mean Squared Error): [Insert RMSE value here]

RMSPE (Root Mean Squared Percentage Error): [Insert RMSPE value here]

R² Score: [Insert R² value here]

Random Forest Regressor:
RMSE: [Insert RMSE value here]

RMSPE: [Insert RMSPE value here]

R² Score: [Insert R² value here]

Feature Importance (Random Forest):
The Random Forest model identified the following features as most important for predicting sales:

[List most important features here]

**Conclusion**:

This project demonstrates the use of both Linear Regression and Random Forest to predict retail sales based on various factors such as store type, promotional offers, and competitor proximity. Random Forest performed better in terms of feature importance and model accuracy.
