#EXP. NO. 1: Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:

/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: NIRANJAN S
RegisterNumber:  24900209
~~~

import numpy as np
import matplotlib.pyplot as plt
x = np.array(eval(input()))
y = np.array(eval(input()))
plt.scatter(x,y)
plt.show()

xmean = np.mean(x)
ymean = np.mean(y)
num=0
den=0

for i in range(len(x)):
    num+=(x[i]-xmean)*(y[i]-ymean)
    den+=(x[i]-xmean)**2

m = num/den
b = ymean - m*xmean
print(m,b)

ypred = m*x+b
print(ypred)

plt.scatter(x,y,color='Red')
plt.plot(x,ypred,color='Blue')
plt.show()
~~~

## Output:
## Slope andd y intercept:
![360801346-ec7cdb04-e2c5-4981-a98f-226160c3eb41](https://github.com/user-attachments/assets/a1f61427-1e5e-43f1-b0ec-e900f093ac72)
## Y Intercept:
![360801442-589b2574-03d5-48e8-8459-acd8a5938197](https://github.com/user-attachments/assets/c01a851c-a008-4e4a-80a8-0afed417d8a4)
## Graph
![360801508-bc7bd28d-0caa-41c7-816a-6198d90317c9](https://github.com/user-attachments/assets/b7eadca5-a229-407e-a302-4450a2bc5d02)


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
