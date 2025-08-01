# Airbnb Price Prediction (NYC)

This project builds a machine learning model to predict Airbnb listing prices in New York City.
It follows a full ML workflow: manual data preprocessing, exploratory data analysis, and training regression models to understand what factors affect listing prices.

---

## Dataset

- **Source:** Airbnb NYC listings (`airbnbListingsData.csv`)
- **Target variable:** `price`
- **Selected features:**
  - `room_type`
  - `neighbourhood_group_cleansed`
  - `number_of_reviews`
  - `reviews_per_month`
  - `host_is_superhost`
  - `host_listings_count`
  - `minimum_nights`
  - `availability_365`
  - `review_scores_rating`
  - `accommodates`

Text fields like `name`, `description`, and `host_about` were removed to keep the model simple and focused.

---

## Workflow

1. **Data exploration & cleaning**
   - Remove rows with missing target (`price`).
   - Remove extreme price outliers (1st and 99th percentiles).
   - Identify useful features.

2. **Data preprocessing**
   - Impute missing numeric features with mean.
   - Impute missing categorical features with the most frequent value.
   - One-hot encode categorical variables.
   - Scale numeric features to similar ranges.

3. **Modeling**
   - Train/test split (80/20).
   - Train two models:
     - Linear Regression
     - Random Forest Regressor
   - Evaluate using:
     - Mean Absolute Error (MAE)
     - Root Mean Squared Error (RMSE)
   - Plot actual vs. predicted prices to visualize performance.

---

## Results

- The Random Forest model performed better, with lower MAE and RMSE compared to Linear Regression.
- Scatter plots showed predictions generally aligned with actual prices, though some variance remained, especially for higher-priced listings.
- Using a combination of listing, host, and review features provided a solid baseline for predicting Airbnb prices.

---

## Conclusion

Manually preprocessing the data and training different models helps reveal which features most influence Airbnb prices.
Further improvements could include:
- Adding new features
- Tuning hyperparameters
- Trying advanced models like Gradient Boosting or XGBoost

This project demonstrates the end-to-end process of defining, building, and evaluating a predictive model on real-world data.

---
