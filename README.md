# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
STEP 1. START

STEP 2. Get the independent variable X and dependent variable Y.

STEP 3. Calculate the mean of the X -values and the mean of the Y -values.

STEP 4. Find the slope m of the line of best fit using the formula. 

<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">

STEP 5. Compute the y -intercept of the line by using the formula:

<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">

STEP 6. Use the slope m and the y -intercept to form the equation of the line.

STEP 7. END.

## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by:Sharan G
RegisterNumber:  212223230203
*/

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

```

## Output:
# SLOPE AND Y-INTERCEPT:
![Screenshot 2024-08-23 055626](https://github.com/user-attachments/assets/67b55996-e676-4710-b6ca-61233034739d)

# Y PREDICTED:
![Screenshot 2024-08-23 055631](https://github.com/user-attachments/assets/4743b6ac-18d6-4c64-a62f-416b7ae3c9cc)

# GRAPH:
![Screenshot 2024-09-27 113144](https://github.com/user-attachments/assets/4c0ab17c-4fd9-4392-bbfc-c4f9d28ae7c6)




## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
