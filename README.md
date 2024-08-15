# Crab Data Analysis and Age Prediction

## Overview

This project focuses on analyzing and predicting the age of crabs based on various physical attributes. The analysis involves data visualization, feature engineering, and the use of multiple regression models, including linear regression, Lasso, HuberRegressor, Ridge, and ElasticNet. The final model is a stacked regressor that combines the predictions of these models to provide the best estimate of crab age.

## Project Structure

- **Data Visualization**: The project begins with an exploration of the data using various visualization techniques, such as histograms, scatter plots, and pair plots. These visualizations help in understanding the distribution of features like weight, length, and age, as well as the relationships between them.

- **Feature Engineering**: Several new features are engineered to enhance the predictive power of the models. These include ratios and logarithmic transformations of existing features, as well as the creation of a Body Condition Index (BCI) and binning of the Length feature.

- **Modeling**: The project employs a variety of regression models:
  - **Linear Regression**: A polynomial regression model with degree 2.
  - **Lasso Regression**: A polynomial regression model with degree 3, using Lasso regularization.
  - **Huber Regressor**: A robust regression model less sensitive to outliers.
  - **Ridge Regression**: A polynomial regression model with degree 2, using Ridge regularization.
  - **ElasticNet**: A regression model that combines Lasso and Ridge.

  These models are then combined in a **Stacking Regressor**, which uses a HuberRegressor as the final estimator. This approach aims to leverage the strengths of each individual model to improve prediction accuracy.

- **Prediction**: The model is trained and tested on the provided data, with the performance evaluated using the Mean Absolute Error (MAE). The final predictions on the test set are saved in a CSV file named `Exam.csv`.

## Files

- **train.csv**: The training dataset containing features and the target variable (Age).
- **test.csv**: The test dataset used for making predictions.
- **sample_submission.csv**: A sample submission file to format the final predictions.
- **Exam.csv**: The final submission file containing the predicted ages.

## Usage

1. **Install Dependencies**: Ensure you have the necessary Python libraries installed:
   ```bash
   pip install numpy pandas seaborn matplotlib scikit-learn
   ```

2. **Run the Notebook**: Execute the code in the provided Jupyter notebook or script to perform the analysis and generate predictions.

3. **View Results**: The predicted ages will be saved in `Exam.csv`, which can be submitted or further analyzed.

## Visualizations

The project includes the following visualizations:
- **Distribution of Weight**: Shows the distribution of crab weight across different sexes.
- **Relationship between Length and Age**: A scatter plot illustrating the correlation between the length of crabs and their age.
- **Distribution of Age**: A histogram of crab ages.
- **Age by Sex**: Violin and box plots showing the distribution of age across different sexes.
- **Pair Plot**: A pairwise plot of numerical features, colored by sex.

## Feature Engineering

The following new features were created:
- **Viscera Ratio**
- **Shell-to-body Ratio**
- **Meat Yield**
- **Length-to-Diameter Ratio**
- **Weight-to-VisceraWeight Ratio**
- **Weight-to-ShellWeight Ratio**
- **Weight-to-ShuckedWeight Ratio**
- **Length Bins**
- **Body Condition Index (BCI)**
- **Weight without Viscera**
- **Log Weight**

## Model Performance

The Mean Absolute Error (MAE) for the stacked model is calculated and displayed in the notebook. This metric provides insight into the average prediction error of the model.

## Conclusion

This project demonstrates a comprehensive approach to data analysis and predictive modeling, using a variety of regression techniques and feature engineering to accurately predict the age of crabs. The final model, a stacking regressor, provides robust predictions by combining the strengths of multiple models.

---
