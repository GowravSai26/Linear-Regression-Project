# Task 3: Interview Questions and Answers

### 1. What assumptions does linear regression make?
Linear regression relies on several key assumptions to produce reliable results. These are often remembered by the acronym **LINE**:

* **Linearity:** The relationship between the independent variables and the dependent variable is linear.
* **Independence:** The observations are independent of each other (e.g., no autocorrelation).
* **Normality:** The residuals (the errors between actual and predicted values) are normally distributed.
* **Equal Variance (Homoscedasticity):** The residuals have a constant variance at every level of the independent variables.

---
### 2. How do you interpret the coefficients?
The coefficient of an independent variable represents the **change in the dependent variable for a one-unit increase** in that independent variable, assuming all other variables in the model are held constant.

**For example:** In a house price prediction model, if the coefficient for the 'square_feet' feature is 150, it means that for each additional square foot of space, the house price is predicted to increase by $150, all else being equal.

---
### 3. What is R² score and its significance?
The **R-squared (R²) score**, also known as the coefficient of determination, measures the proportion of the variance in the dependent variable that can be explained by the independent variables in the model.

**Its significance** is that it tells you how well your model fits the data. It ranges from 0 to 1. An R² of 0.80 means that 80% of the variation in the outcome can be explained by the model's inputs. A higher R² generally indicates a better fit.

---
### 4. When would you prefer MSE over MAE?
Both Mean Squared Error (MSE) and Mean Absolute Error (MAE) are used to evaluate regression models, but they have a key difference.

* **MAE (Mean Absolute Error):** Treats all errors equally.
* **MSE (Mean Squared Error):** Squares the errors before averaging them.

You would prefer **MSE** when you want to **heavily penalize large errors**. Because the errors are squared, a prediction that is far off the mark will contribute much more to the total error than a small miss. This is useful in situations where large mistakes are particularly undesirable.

---
### 5. How do you detect multicollinearity?
Multicollinearity occurs when independent variables in a regression model are highly correlated with each other. You can detect it using:

* **Correlation Matrix:** Create a heatmap of the correlations between all independent variables. A high correlation coefficient (e.g., > 0.8 or < -0.8) between two variables is a strong indicator.
* **Variance Inflation Factor (VIF):** VIF measures how much the variance of a coefficient is "inflated" because of its correlation with other variables. A common rule of thumb is that a VIF score greater than 5 or 10 indicates significant multicollinearity.

---
### 6. What is the difference between simple and multiple regression?
The difference is the number of independent variables used to predict the outcome.

* **Simple Linear Regression:** Uses **one** independent variable to predict a single dependent variable.
* **Multiple Linear Regression:** Uses **two or more** independent variables to predict a single dependent variable.

---
### 7. Can linear regression be used for classification?
**No, not effectively.** Linear regression is designed for **regression tasks** where the output is a continuous value (e.g., price, temperature). Classification tasks require a categorical output (e.g., Yes/No, Cat/Dog).

While you could try to apply a threshold to the output of a linear model, the results are unreliable because the output is not a probability and can fall outside the 0-1 range. The appropriate linear model for classification is **Logistic Regression**.

---
### 8. What happens if you violate regression assumptions?
Violating the core assumptions of linear regression can make your model's results unreliable and misleading.

* **If Linearity is violated:** Your model will be a poor fit and its predictions will be inaccurate.
* **If Independence is violated:** The confidence intervals and significance tests for the coefficients will be unreliable.
* **If Normality of residuals is violated:** The statistical tests on the coefficients become less trustworthy.
* **If Homoscedasticity is violated:** The coefficient estimates may be correct, but their standard errors will be wrong, leading to incorrect conclusions about the significance of the features.