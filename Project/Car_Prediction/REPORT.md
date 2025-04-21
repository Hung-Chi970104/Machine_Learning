# Goal: Predict the price of a used car based on its features using a machine learning pipeline.

📊 Dataset Overview:
Contains features such as Mileage, Age, Engine_Liters, Cylinders, Doors, Airbags, Turbo, and Leather_Interior.

- Target variable: Price
- Average car price: $18,556
- Regression task

## 🔧 Data Preprocessing:
Created custom feature ratios:

- Engine_Liters_per_Cylinders
- Doors_per_Airbags
- Applied log transform to skewed features: Mileage, Age, Engine_Liters
- Used SimpleImputer for missing values
- One-hot encoded categorical features

## 🧠 Model:
Built a full pipeline using RandomForestRegressor inside Pipeline with ColumnTransformer

Hyperparameter tuning using RandomizedSearchCV

## 📈 Model Performance:
- 10-fold Cross-Validated
  - RMSE: ~6,657
  - R^2: ~63%
- Relative Error: ~35% of average car price
- Feature importances show that log-transformed features and engine-per-cylinder were most influential

## Final Thought
With this RMSE and R^2, the model did a quite solid job, although not good enough for production, due to its stability and descent average distances from the true values

## Others' projects
- https://www.kaggle.com/code/sawdi777/car-price-full-regression#Project-Overview
