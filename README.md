# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Input the data points (X: study hours, Y: marks) and compute their means.

2.Calculate slope m using covariance and variance.

3.Compute intercept c=
Y
ˉ
−m
X
ˉ
.

4.Predict marks using Y=mX+c.

## Program:
```
import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression
from sklearn.metrics import mean_squared_error, r2_score
X = np.array([1, 2, 3, 4, 5]).reshape(-1, 1)  
Y = np.array([35, 40, 50, 55, 65])           
model = LinearRegression()
model.fit(X, Y)
print("Slope (m):", model.coef_[0])
print("Intercept (c):", model.intercept_)

Y_pred = model.predict(X)

hours = np.array([[6]])
predicted_marks = model.predict(hours)
print("Predicted marks for 6 hours of study:", predicted_marks[0])
mse = mean_squared_error(Y, Y_pred)
r2 = r2_score(Y, Y_pred)

print("Mean Squared Error:", mse)
print("R2 Score:", r2)
plt.scatter(X, Y, color='blue', label='Actual Data')
plt.plot(X, Y_pred, color='red', label='Regression Line')
plt.xlabel("Hours Studied")
plt.ylabel("Marks Scored")
plt.title("Simple Linear Regression Model")
plt.legend()
plt.show()
Developed by: Kavinaya V
RegisterNumber: 212225230133 

```

## Output:
<img width="1920" height="1080" alt="Screenshot (173)" src="https://github.com/user-attachments/assets/c90e28c4-6c3a-409c-bb9f-f406959b6ac7" />
<img width="1920" height="1080" alt="Screenshot (177)" src="https://github.com/user-attachments/assets/2592d546-b218-47ab-8dae-a9bbf7bed601" />



## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
