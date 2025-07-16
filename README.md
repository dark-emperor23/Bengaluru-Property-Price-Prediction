#  Bengaluru House Price Prediction

This is a Machine Learning project to predict housing prices in Bengaluru based on various features like location, square footage (sqft), number of bathrooms, and number of bedrooms (BHK). The model is trained using real-world data and predicts the prices of property on various parameters.

##  Project Objective

- Clean and preprocess the Bengaluru housing dataset
- Perform exploratory data analysis (EDA)
- Train and evaluate multiple regression models
- Use GridSearchCV for model selection
- Build a prediction function

##  Files and Folders

1.Bengaluru_House_Data.csv - This dataset contains information such number of beddrooms,bathrooms,location of the properties and their prices
2.This model helps in prediction of data based on various parameters.

## Project Workflow
1️  Data Collection
    - Source: Kaggle (Bengaluru House Price Data)
    - Format: CSV

2️  Data Cleaning
    - Handle missing values
    - Remove outliers (e.g., price per square foot anomalies)
    - Convert string-based sqft values to numeric
    - Drop unnecessary columns like society, balcony (if irrelevant)

3️  Feature Engineering
    - Extract BHK from total_bedrooms
    - Create new feature: price_per_sqft
    - Reduce dimensionality of location by grouping rare locations into "other"
    - Encode categorical features (like location) using One-Hot Encoding

4️  Exploratory Data Analysis (EDA)
    - Visualize relationship between sqft, price, BHK, and location
    - Use scatter plots, histograms, and boxplots
    - Check multicollinearity and feature importance

5️  Model Building
    - Split data into train and test sets
    - Train multiple regression models:
        • Linear Regression
        • Lasso Regression
        • Decision Tree Regressor
    - Use GridSearchCV for hyperparameter tuning

6️  Model Evaluation
    - Evaluate models using cross-validation (R² score, MAE, RMSE)
    - Select the best model based on performance

7️  Model Deployment
    - Save the best model using Pickle
    - Create a prediction function (`predict_price(location, sqft, bath, bhk)`)
    - (Optional) Deploy with Flask/Streamlit for user input & prediction

8️  Web Interface (Optional)
    - Input: location, sqft, BHK, bath
    - Output: predicted price in lakhs
    - Hosted locally or on platforms like Heroku/Render

9  Documentation & Version Control
    - README.md for project explanation
    - requirements.txt for dependencies
    - Jupyter notebook for experiments
