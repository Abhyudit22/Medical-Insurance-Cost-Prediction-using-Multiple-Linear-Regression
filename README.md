# AI-ML Assignment 1 - Medical Insurance Cost Prediction

## Objective
The objective of this assignment is to develop a Multiple Linear Regression model to estimate the medical insurance charges of customers based on their personal and health-related information.

## Dataset Link
[Medical Cost Personal Insurance Dataset on Kaggle](https://www.kaggle.com/datasets/mirichoi0218/insurance)

*(Note: The dataset is not included in this repository due to licensing. Please download `insurance.csv` from Kaggle and place it in the project root directory before running the code).*

## Libraries Used
- **Pandas**: For data loading and manipulation.
- **NumPy**: For numerical computations.
- **Matplotlib & Seaborn**: For data visualization (scatter plots).
- **Scikit-Learn (sklearn)**: For model development (Linear Regression), data splitting, and performance evaluation.

## Methodology
1. **Data Understanding**: Loaded the dataset, displayed initial records, and categorized features into numerical and categorical types.
2. **Data Preprocessing**: Checked for missing values, applied one-hot encoding to categorical variables (`sex`, `smoker`, `region`), and split the dataset into 80% training and 20% testing sets.
3. **Model Development**: Built a Multiple Linear Regression model using the training data.
4. **Model Evaluation**: Evaluated the model's performance on the testing set using Mean Absolute Error (MAE), Mean Squared Error (MSE), and R² Score. Generated an Actual vs. Predicted scatter plot to visually assess the fit.

## Results
- **Mean Absolute Error (MAE)**: ~4181.19
- **Mean Squared Error (MSE)**: ~33596915.85
- **R² Score**: ~0.7836
*(Actual values may vary slightly based on random state during data split).*

## Conclusion
**Key findings:** The Multiple Linear Regression model provides a reasonable baseline for predicting medical insurance charges, achieving an R² score of around 0.78. The model performs well for the majority of individuals with average charges but exhibits higher errors when predicting extreme high-cost outliers.

**Factors affecting insurance charges:** Features such as being a smoker, age, and BMI are the most significant drivers of higher insurance costs.

**Limitation of Linear Regression for this problem:** One major limitation of Linear Regression is its assumption of a strictly linear and additive relationship between the features and the target variable. In reality, the interaction between features (e.g., the compounded effect of smoking combined with a high BMI) often has a non-linear effect on medical charges, which a basic linear model fails to capture effectively.
