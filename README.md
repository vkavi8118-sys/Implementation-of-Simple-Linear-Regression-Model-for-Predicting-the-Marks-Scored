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

X = np.array(list(map(float, input().split())))
Y = np.array(list(map(float, input().split())))

Xmean = np.mean(X)
Ymean = np.mean(Y)

num = np.sum((X - Xmean)*(Y - Ymean))
den = np.sum((X - Xmean)**2)

m = num / den
c = Ymean - m * Xmean

print("Slope (m):", m)
print("Intercept (c):", c)

Y_pred = m * X + c
print("Predicted Marks:", Y_pred)

x_new = float(input("Enter study hours to predict marks: "))
y_new = m * x_new + c
print("Predicted marks for given input:", y_new)

sorted_indices = np.argsort(X)

plt.scatter(X, Y)
plt.plot(X[sorted_indices], Y_pred[sorted_indices], color="red")
plt.xlabel("Study Hours")
plt.ylabel("Marks Scored")
plt.title("Simple Linear Regression")
plt.show()

Developed by: Kavinaya V
RegisterNumber: 212225230133 

```

## Output:
<img width="818" height="680" alt="Screenshot 2026-04-24 144058" src="https://github.com/user-attachments/assets/b25fea1f-187e-429e-bd44-9fec48fd0005" />
<img width="874" height="372" alt="Screenshot 2026-04-24 144114" src="https://github.com/user-attachments/assets/ca320910-d17d-48c2-8940-0e560d58d067" />
<img width="873" height="701" alt="Screenshot 2026-04-24 144125" src="https://github.com/user-attachments/assets/b7dbb88a-9c58-4ff4-a9af-12b56715593d" />


## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
