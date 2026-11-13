# California Housing Price Prediction

A Machine Learning regression project that predicts median house values in California using the California Housing dataset from Scikit-learn.

The project explores multiple regression algorithms, compares their performance, and evaluates how well they generalize to unseen data.

## Project Overview

The objective of this project is to build a regression model that predicts median house values based on various housing and geographical features.

The project covers the complete basic machine learning workflow, from data exploration and preprocessing to model training, evaluation, and comparison.

## Dataset

- **Dataset:** California Housing Dataset
- **Source:** Scikit-learn
- **Total observations:** 20,640
- **Features:** 8
- **Target:** Median house value

### Features

| Feature | Description |
|---|---|
| MedInc | Median income in the block group |
| HouseAge | Median house age |
| AveRooms | Average number of rooms |
| AveBedrms | Average number of bedrooms |
| Population | Block group population |
| AveOccup | Average household occupancy |
| Latitude | Geographical latitude |
| Longitude | Geographical longitude |

The target variable represents median house value in units of $100,000 and is capped at 5.0.

## Technologies and Libraries

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab

## Project Workflow

1. **Data Loading:** Loaded the California Housing dataset and converted it into a Pandas DataFrame.
2. **Exploratory Data Analysis:** Examined dataset structure, statistical summaries, missing values, duplicates, and feature distributions.
3. **Data Preparation:** Separated features and target variable and split the dataset into training and testing sets using an 80:20 ratio.
4. **Model Training:** Implemented and trained four regression algorithms.
5. **Model Evaluation:** Evaluated models using MAE, MSE, RMSE, and R² Score.
6. **Model Comparison:** Visualized and compared the performance of all four models.
7. **Feature Importance:** Examined the contribution of individual features to Random Forest predictions.
8. **Cross-Validation:** Used 5-fold cross-validation to assess model performance across different training folds.

## Models Implemented

- Linear Regression
- Polynomial Regression (Degree 2)
- Ridge Regression (L2 Regularization)
- Random Forest Regression

## Model Performance

The following results were obtained during experimentation:

| Model | R² Score | MAE |
|---|---:|---:|
| Linear Regression | 0.5758 | 0.5332 |
| Polynomial Regression | 0.6457 | 0.4670 |
| Ridge Regression | 0.6666 | 0.4880 |
| Random Forest | **0.8051** | **0.3275** |

### Best Performing Model: Random Forest

Random Forest achieved the best results among the models tested:

- **R² Score:** 0.8051
- **MAE:** 0.3275
- **RMSE:** 0.5053
- **5-Fold Cross-Validation Mean R²:** 0.8041

The feature importance analysis identified median income (MedInc) as the most influential feature, followed by average occupancy (AveOccup).

## Key Learnings

Through this project, I gained practical experience with:

- Exploratory Data Analysis and data visualization.
- Training and evaluating regression models.
- Feature engineering using polynomial features.
- Feature scaling using StandardScaler.
- L2 regularization with Ridge Regression.
- Understanding overfitting and the bias-variance trade-off.
- K-Fold Cross-Validation.
- Feature importance analysis in ensemble models.
- Comparing machine learning models using evaluation metrics.

## Limitations

- The dataset is a historical educational dataset and may not represent current housing market conditions.
- The target variable is capped at $500,000.
- Random Forest showed a noticeable gap between training and testing performance, indicating overfitting.
- Model selection involved repeated comparisons on the test set, so the reported test metrics should be treated as experimental rather than a fully independent final evaluation.

## Conclusion

This project provided hands-on experience with the fundamental concepts of supervised machine learning and regression.

Among the four algorithms evaluated, Random Forest Regression achieved the strongest experimental results, demonstrating the effectiveness of ensemble learning for capturing complex relationships in structured datasets.
