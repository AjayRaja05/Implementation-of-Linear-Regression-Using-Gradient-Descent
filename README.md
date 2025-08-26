# Implementation-of-Linear-Regression-Using-Gradient-Descent

## AIM:
To write a program to predict the profit of a city using the linear regression model with gradient descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula.

   <img width="285" height="137" alt="image" src="https://github.com/user-attachments/assets/8da9e7a6-d9c1-470e-a750-ee09fa174a3e" />
4. Compute the y -intercept of the line by using the formula:

   <img width="192" height="43" alt="image" src="https://github.com/user-attachments/assets/662bfffd-bb91-46e7-af0e-55a3876fb2b8" />
5. Use the slope m and the y -intercept to form the equation of the line. 6. Obtain the straight line equation Y=mX+b and plot
 the scatterplot.



## Program:
```
/*
Program to implement the linear regression using gradient descent.
Developed by: AJAYRAJA RATHINAM T 
RegisterNumber: 212224240006

import numpy as np
import matplotlib.pyplot as plt
X=np.array(eval(input()))
Y=np.array(eval(input()))
X_mean=np.mean(X)
print(X_mean)
Y_mean=np.mean(Y)
print(Y_mean)
num=0
denum=0
for i in range(len(X)):
  num+=(X[i]-X_mean)*(Y[i]-Y_mean)
  denum+=(X[i]-X_mean)**2
m=num/denum
print(m)
b=Y_mean - m*X_mean
print(b)
Y_pred=m*X+b
print(Y_pred)
plt.scatter(X,Y,color='blue')
plt.plot(X,Y_pred,color='yellow')
plt.show()
 
*/
```

## Output:
<img width="993" height="635" alt="image" src="https://github.com/user-attachments/assets/f417dc89-9592-4193-b743-1d64b7718d5f" />



## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
