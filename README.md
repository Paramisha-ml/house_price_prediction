# House Price Prediction Using Linear Regression

This project demonstrates a beginner-friendly implementation of **Linear Regression** to predict house prices using simple numerical features like square footage, number of bedrooms, and bathrooms. It is built using the **Ames Housing Dataset** (from Kaggle) as part of a machine learning internship task.

##  Dataset
I used a kaggle datset in csv format:  https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data

##  Features Used
To simplify and clean the data, I perform the following operations:

| Original Columns              | New Name         | Description                             |
|-------------------------------|------------------|-----------------------------------------|
| `GrLivArea`                   | `square_footage` | Above ground living area in sq. ft.     |
| `BedroomAbvGr`                | `Bedrooms`       | Number of bedrooms above ground         |
| `FullBath` + 0.5 × `HalfBath` | `Bathrooms`      | Full and half bathrooms (half = 0.5)    |

The final dataset contains these columns:
- `Id`
- `square_footage`
- `Bathrooms`
- `Bedrooms`
- `SalePrice` (Target/Label)

##  Model Training
- I use **Linear Regression** from the `sklearn.linear_model` module.
- The dataset is split using `train_test_split`:
  - **80%** for training
  - **20%** for validation
- Model accuracy is evaluated using the **R² score** from `sklearn.metrics`.

## Accuracy
After training the model, it is validated on the hold-out 20% test set. The result is printed like this: Accuracy: 0.7xxx
This R² score shows how well the model fits and explains the variation in house prices.

##  Custom Prediction
You can test the model on your own custom data using:
```python
custom_data = pd.DataFrame({
    'square_footage': [1500, 2500],
    'Bathrooms': [2.5, 3.0],
    'Bedrooms': [3, 4]
})

## Libraries Used : Python, pandas, numpy & scikit-learn

## Summary
This project is a great example for beginners learning:
- Data preprocessing and cleaning
- Feature engineering
- Building and evaluating ML models
- Making real-time predictions





