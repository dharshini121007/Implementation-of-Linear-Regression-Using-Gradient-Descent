# Implementation-of-Linear-Regression-Using-Gradient-Descent

## AIM:
To write a program to predict the profit of a city using the linear regression model with gradient descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Read the input dataset and initialize the slope (m) and intercept (b) as zero values, then choose a suitable learning rate and iteration count.
2.Calculate the predicted output values using the current equation of the line for all given data points.
3.Find the difference between the predicted values and the actual target values to determine the error.
4.Update the slope and intercept repeatedly using the gradient descent method so the error decreases in every iteration.
5.After the training process is completed, print the final slope and intercept values and plot the best fit regression line with the original data points.
## Program:
```
/*
Program to implement the linear regression using gradient descent.
Developed by:DHARSHINI.M
RegisterNumber:212225220025 
*/
import numpy as np
import matplotlib.pyplot as plt
X = np.array([1, 2, 3, 4, 5])
Y = np.array([2, 3, 5, 5, 6])
m = 0
c = 0        
L = 0.01     
epochs = 1000  
n = float(len(X))  
for i in range(epochs):
    Y_pred = m * X + c  
    D_m = (-2/n) * sum(X * (Y - Y_pred))  
    D_c = (-2/n) * sum(Y - Y_pred)        
    m = m - L * D_m   
    c = c - L * D_c  
print(f"Final slope (m): {m}")
print(f"Final intercept (c): {c}")
Y_pred = m * X + c
plt.scatter(X, Y, color="red", label="Data Points")
plt.plot(X, Y_pred, color="blue", label="Best Fit Line")
plt.xlabel("X")
plt.ylabel("Y")
plt.legend()
plt.title("Linear Regression using Gradient Descent")
plt.show()
```

## Output:



<img width="952" height="637" alt="image" src="https://github.com/user-attachments/assets/53bfe273-d8ba-4746-ae36-23a132c66db6" />




## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
