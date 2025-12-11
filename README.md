#  Ordinary Least Squares (OLS) Linear Regression — From Scratch

This project demonstrates how to implement **Ordinary Least Squares (OLS)** linear regression **without using any external libraries** like NumPy or pandas.  
It’s a simple and educational example of how linear regression works under the hood.

---

##  Features
- Calculates **slope (m)** and **intercept (b)** manually  
- Uses basic Python operations only  
- Predicts `y` values for given `x` inputs  
- Clean and minimal code — great for learning regression fundamentals  

---

##  Formula

The best-fit line is given by:

\[
y = m x + b
\]

\[
x_mean = sum(x)/len(x)
\]


\[
y_mean = sum(y)/len(y)
\]


Where:

\[
m = \frac{\sum (x_i - x_mean)(y_i - y_mean)}{\sum (x_i - x_mean)^2}
\]


\[
b = y_mean - m*x_mean
\]

---
#  Multiple Linear Regression

This project demonstrates **Multiple Linear Regression implemented manually in Python**, without using any external libraries like NumPy or scikit-learn.  
It helps understand the **mathematical logic** behind regression and how the **coefficients are derived step by step** — for both types of models:

- **Regression through the Origin**
- **Regression through the Centroid (Normal Regression)**

---

##  Concept Summary

- **Goal:** Predict the dependent variable `Y` using two independent variables, `X1` and `X2`.  
- **Method:** Uses the *least squares method* to minimize the sum of squared errors between actual and predicted values.  
- **Outputs:** Regression coefficients `B0`, `B1`, and `B2`, and the final regression equation.  
- **Types Covered:**
  1. **Through Centroid (Normal Regression)** → includes intercept term `B0`
  2. **Through Origin (No Intercept)** → forces regression to start at (0,0,0)

---

## 1. Regression **Through Centroid** (Normal Regression)

### Model:
\[
Y = B_0 + B_1X_1 + B_2X_2
\]

### Formulas:
\[
B_1 = \frac{Σ(X_2 - \bar{X_2})^2Σ(X_1 - \bar{X_1})(Y - \bar{Y}) - Σ(X_1 - \bar{X_1})(X_2 - \bar{X_2})Σ(X_2 - \bar{X_2})(Y - \bar{Y})}{Σ(X_1 - \bar{X_1})^2Σ(X_2 - \bar{X_2})^2 - [Σ(X_1 - \bar{X_1})(X_2 - \bar{X_2})]^2}
\]

\[
B_2 = \frac{Σ(X_1 - \bar{X_1})^2Σ(X_2 - \bar{X_2})(Y - \bar{Y}) - Σ(X_1 - \bar{X_1})(X_2 - \bar{X_2})Σ(X_1 - \bar{X_1})(Y - \bar{Y})}{Σ(X_1 - \bar{X_1})^2Σ(X_2 - \bar{X_2})^2 - [Σ(X_1 - \bar{X_1})(X_2 - \bar{X_2})]^2}
\]

\[
B_0 = \bar{Y} - B_1\bar{X_1} - B_2\bar{X_2}
\]

 **This is the standard regression model** — the regression plane passes through the **centroid** (mean point)  
\((\bar{X_1}, \bar{X_2}, \bar{Y})\).

---

## 2. Regression **Through Origin**

### Model:
\[
Y = B_1X_1 + B_2X_2
\]

### Formulas:
\[
B_1 = \frac{ΣX_2^2ΣX_1Y - ΣX_1X_2ΣX_2Y}{ΣX_1^2ΣX_2^2 - (ΣX_1X_2)^2}
\]

\[
B_2 = \frac{ΣX_1^2ΣX_2Y - ΣX_1X_2ΣX_1Y}{ΣX_1^2ΣX_2^2 - (ΣX_1X_2)^2}
\]

 **Used only when** you are told that the regression line/plane passes **through the origin**,  
i.e., \(Y = 0\) when \(X_1 = X_2 = 0\).  
This version has **no intercept** (`B0 = 0`).

#### When we say a regression passes through the origin, it means the line or plane goes through the point (0, 0, 0), so all the mean are 0. 

---

# Batch Gradient Descent for Linear Regression

Simple from-scratch implementation of **batch gradient descent** to fit a linear model \( y = B_0 + B_1 \cdot x \) using mean squared error.

## Features
-  Computes predictions, loss, and gradients manually  
-  Averages gradients by `n` (standard MSE convention)
-  Prints B0 (intercept), B1 (slope), and loss each iteration
-  Interactive input for data, initial parameters, learning rate

## Mathematical Background

**Cost function**: \( J(B_0, B_1) = \frac{1}{2n} \sum_{i=1}^{n} (y_{\text{pred},i} - y_i)^2 \)

**Gradient updates**:

