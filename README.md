## Baseball Salary Prediction

### Project Overview

This project aims to predict the **salary of professional baseball players** based on their performance statistics. By analyzing a dataset of player statistics for both the current season and their entire career, the goal is to develop a regression model that can accurately estimate a player's salary. This is a classic machine learning task that can provide insights into what factors are most valued in professional sports.

-----

### Technical Highlights

  * **Dataset**: A dataset named `Hitters.xls` is used, which contains baseball player statistics.
  * **Size**: 322 entries, 20 columns. The `Salary` column has 59 missing values.
  * **Key Features**:
      * **Current Season Stats**: `AtBat`, `Hits`, `HmRun`, `Runs`, `RBI`, `Walks`.
      * **Career Stats**: `CAtBat`, `CHits`, `CHmRun`, `CRuns`, `CRBI`, `CWalks`.
      * **Other**: `Years`, `League`, `Division`, `PutOuts`, `Assists`, `Errors`.
  * **Approach**:
      * **Data Cleaning**: Rows with missing values in the target `Salary` column were dropped. The remaining dataset was used for modeling.
      * **Exploratory Data Analysis**: The code checks basic statistics, null values, duplicates, and unique values for all columns.
      * **Label Encoding**: Applied to categorical columns (`League`, `Division`, `NewLeague`).
      * **Regression Task**: The target variable is `Salary`.
      * **Models Used**:
          * A suite of regression models were trained, including Ridge, XGBoost, Random Forest, AdaBoost, Gradient Boosting, Bagging, Decision Tree, SVR, and K-Nearest Neighbors (KNN).
  * **Best R² Score**:
      * **0.657** with Gradient Boosting Regressor.
      * **0.631** with Random Forest Regressor.
      * **0.605** with Bagging Regressor.
      * The moderate R² scores indicate that predicting salaries is a complex task with these features, but the ensemble models show the best predictive power.

-----

### Purpose and Applications

  * **Predict professional baseball player salaries** based on their performance.
  * Assist baseball teams and agents in salary arbitration and contract negotiations.
  * Provide insights into which on-field metrics are most correlated with a player's market value.
  * Serve as a foundational model for sports analytics and performance evaluation.

-----

### Installation

Clone the repository and download the dataset.

Install the necessary libraries:

```bash
pip install pandas numpy seaborn matplotlib scikit-learn xgboost
```

-----

### Collaboration

We welcome contributions to improve the project. You can help by:

  * Exploring more advanced methods for handling the missing `Salary` values, such as imputation, rather than just dropping the rows.
  * Performing comprehensive hyperparameter tuning and cross-validation for the top-performing regression models.
  * Investigating the impact of different feature engineering techniques, such as creating new features like `Batting Average` or `On-base Percentage`.
  * Adding explainability (e.g., SHAP or LIME) to understand which player statistics are the most significant drivers of salary.
