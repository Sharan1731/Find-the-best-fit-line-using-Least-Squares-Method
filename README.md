
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
STEP 1. Get the independent variable X and dependent variable Y.
STEP 2. Calculate the mean of the X -values and the mean of the Y -values.
STEP 3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
STEP 4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
STEP 5. Use the slope m and the y -intercept to form the equation of the line.
END. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: Sharan G
RegisterNumber:212223230203

import numpy as np
import matplotlib.pyplot as plt

#preprocessing input data

X=np.array(eval(input()))
Y=np.array(eval(input()))


#mean

X_mean=np.mean(X)
Y_mean=np.mean(Y)
num=0 #for slope
denom=0 #for slope


#to find sum of (xi-x') & (yi-y') & (xi-x')^2
for i in range(len(X)):
    num+=(X[i]-X_mean)*(Y[i]-Y_mean)
    denom+=(X[i]-X_mean)**2


#to find slope

m=num/denom
b=Y_mean-m*X_mean
print(m,b)

#to find predicted value
 
Y_predicted=m*X+b
print(Y_predicted)


#to plot graphplt.scatter(X,Y)

plt.plot(X,Y_predicted,color="red")
plt.show()

*/
```

## Output:
![Screenshot 2024-08-23 053212](https://github.com/user-attachments/assets/8de5a7a3-b452-45cb-b0f4-0b2877cba181)


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
