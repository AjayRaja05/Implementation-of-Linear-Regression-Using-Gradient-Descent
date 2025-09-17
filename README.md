# Implementation-of-Linear-Regression-Using-Gradient-Descent

## AIM:
To write a program to predict the profit of a city using the linear regression model with gradient descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

1.Import the required library and read the dataframe.

2.Write a function computeCost to generate the cost function.

3.Perform iterations og gradient steps with learning rate.

4.Plot the Cost function using Gradient Descent and generate the required graph.




## Program:
```
Program to implement the linear regression using gradient descent.
Developed by: AJAYRAJA RATHINAM T 
RegisterNumber: 212224240006
```
```
import numpy as np
import matplotlib.pyplot as plt

# Generate synthetic data (you can replace this with your own)
np.random.seed(0)
X = 2 * np.random.rand(100, 1)
y = 4 + 3 * X + np.random.randn(100, 1)  # y = 4 + 3x + noise

# Convert to 1D for simplicity
X = X.flatten()
y = y.flatten()

# Initialize parameters
m = 0  # slope
b = 0  # intercept

# Hyperparameters
learning_rate = 0.01
epochs = 1000
n = len(X)

# Gradient Descent
for i in range(epochs):
    y_pred = m * X + b
    error = y_pred - y

    # Compute gradients
    dm = (2/n) * np.dot(error, X)
    db = (2/n) * np.sum(error)

    # Update parameters
    m -= learning_rate * dm
    b -= learning_rate * db

    # Optional: print cost every 100 iterations
    if i % 100 == 0:
        cost = np.mean(error ** 2)
        print(f"Epoch {i}: Cost = {cost:.4f}, m = {m:.4f}, b = {b:.4f}")

# Final parameters
print(f"\nFinal Model: y = {m:.2f}x + {b:.2f}")

# Plot the data and the regression line
plt.scatter(X, y, color='blue', label='Data points')
plt.plot(X, m * X + b, color='red', label='Regression line')
plt.xlabel("X")
plt.ylabel("y")
plt.title("Linear Regression using Gradient Descent")
plt.legend()
plt.grid(True)
plt.show()
```

## Output:

<img width="676" height="794" alt="image" src="https://github.com/user-attachments/assets/c4f0a632-720d-4335-9da2-c438b6b812dd" />





## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
