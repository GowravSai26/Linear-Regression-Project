# Task 3: Linear Regression for House Price Prediction

## Project Objective
The objective of this task is to implement and understand both simple and multiple linear regression models for predicting house prices. This project uses the California Housing dataset and follows a structured workflow from data preparation to model evaluation and interpretation.

---

## Workflow and Models

The project was divided into two main parts to demonstrate different regression techniques.

### Part 1: Simple Linear Regression
A simple linear regression model was built to establish a baseline.

* **Goal:** Predict house prices using a single feature, Median Income (`MedInc`).
* **Process:** The data was split into training and testing sets. A linear regression model was then fitted to the training data.
* **Evaluation & Results:** The model was evaluated on the test set using Mean Absolute Error (MAE), Mean Squared Error (MSE), and R² score. The resulting regression line was plotted to visualize the relationship between median income and house price. The model's coefficient was interpreted to understand this relationship.

### Part 2: Multiple Linear Regression
To improve predictive accuracy, a multiple linear regression model was built using all available features.

* **Goal:** Predict house prices using all features in the dataset.
* **Process:** Similar to the simple model, the data was split, and the model was fitted to the training data.
* **Evaluation & Results:** The model was evaluated using the same metrics (MAE, MSE, R²). The results showed a significant improvement in the R² score compared to the simple model, indicating better predictive power. The coefficients for each feature were examined to understand their individual impact on the predicted house price.

---

## Key Conclusion

The multiple linear regression model provided a more accurate prediction of house prices than the simple linear regression model. This highlights the importance of using multiple relevant features to capture the complexity of a prediction task.

---

## Tools and Libraries Used

* **Pandas**
* **Scikit-learn**
* **Matplotlib**
* NumPy
* Seaborn

---

## How to Run

1.  Clone the repository to your local machine.
2.  Create and activate a Python virtual environment.
3.  Install the required dependencies from the `requirements.txt` file:
    ```bash
    pip install -r requirements.txt
    ```
4.  Open and run the Jupyter Notebook (`.ipynb` file) in a compatible editor like VS Code.