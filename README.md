# House Price Prediction

Internship project (Week 1) — building a regression model to predict house prices from property features like area, number of rooms, location-related amenities, and furnishing status, and figuring out which features matter most.

## Problem Statement

Real estate buyers and sellers often rely on guesswork or rough comparisons to estimate a property's fair value. This project builds a regression model that predicts house prices and identifies which features most strongly influence price, using a real-world housing dataset.

## Dataset

[Housing Prices Dataset](https://www.kaggle.com/datasets/yasserh/housing-prices-dataset) from Kaggle — 545 rows, 13 columns (price, area, bedrooms, bathrooms, stories, mainroad, guestroom, basement, hotwaterheating, airconditioning, parking, prefarea, furnishingstatus). No missing values or duplicate rows.

## Project Structure

```
HousePricePrediction_[YourName]/
├── analysis.ipynb        # full notebook with all 5 tasks
├── Housing.csv            # dataset used
├── summary.pdf             # 1-page written summary
└── charts/
    ├── price_distribution.png
    ├── correlation_heatmap.png
    └── actual_vs_predicted.png
```

## What's Inside the Notebook

- **Task 1 — Data Loading & Exploration:** loading the CSV, checking shape, identifying target vs. features, checking for missing values
- **Task 2 — Data Cleaning:** handling missing values, removing duplicates, one-hot encoding categorical columns
- **Task 3 — Model Building:** 80/20 train-test split, Linear Regression and Random Forest Regressor, evaluated with MAE, RMSE, and R²
- **Task 4 — Visualization:** price distribution histogram, correlation heatmap, actual vs. predicted price scatter plot
- **Task 5 — Insights & Summary:** written takeaways on the most influential features, model accuracy, surprises in the data, and a recommendation for a real estate business

## Results

| Model | MAE | RMSE | R² |
|---|---|---|---|
| Linear Regression | ~₹9.7L | ~₹13.2L | ~0.65 |
| Random Forest | ~₹10.2L | ~₹14.0L | ~0.61 |

Linear Regression slightly outperformed Random Forest here — likely because the dataset is small (545 rows), leaving Random Forest little room to find extra patterns worth using.

## Key Findings

- Area, bathrooms, and air conditioning are the features most strongly linked to price, with area being the biggest single driver
- Amenities like AC and being in a preferred area add a surprisingly large jump in price, comparable to adding an extra bedroom
- A simpler model (Linear Regression) held up better than a more complex one on this dataset size

## Tools Used

Python, Pandas, Scikit-learn, Matplotlib, Seaborn, Jupyter / Google Colab

## Author

[Your Name] — [College Name]
