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

# 📊 Multiple Linear Regression (Python)

A simple Python program to perform **Multiple Linear Regression** with **two independent variables**, calculated manually using the **Least Squares Method** — no external libraries required.

---

## 💡 Description
This project finds the regression coefficients (**B₀**, **B₁**, **B₂**) for the equation:

\[
Y = B_0 + B_1X_1 + B_2X_2
\]

and predicts the value of **Y** for given **X₁** and **X₂**.

---

## 🧮 Example Data
```python
X1 = [3, 4, 5, 6, 2]
X2 = [8, 5, 7, 3, 1]
Y  = [-3.7, 3.5, 2.5, 11.5, 5.7]

