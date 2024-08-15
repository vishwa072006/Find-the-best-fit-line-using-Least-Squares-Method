# Implementation of Univariate Linear Regression
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
Developed by: k vishwa
RegisterNumber:  212223080061
*/
import numpy as np
import matplotlib.pyplot as plt
X=np.array(eval(input()))
Y=np.array(eval(input()))
X_mean=np.mean(X)
Y_mean=np.mean(Y)
num=0
den=0
for i in range(len(X)):
  num=num+(X[i]-X_mean)*(Y[i]-Y_mean)
  den=den+(X[i]-X_mean)**2
m=num/den
b=Y_mean-m*X_mean
print(m,b)
Y_predicted=m*X+b
print(Y_predicted)
plt.scatter(X,Y)
plt.plot(X,Y_predicted,color='red')
plt.show()


## Output:
![image](https://github.com/ShanmathiShanmugam/Find-the-best-fit-line-using-Least-Squares-Method/assets/121243595/08fc3862-9f7c-4fe7-849c-5be5775f2397)

## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
