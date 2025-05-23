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
```

##Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: A S Siddarth
Registration No. 212224040316

import numpy as np
import matplotlib.pyplot as plt

#Least Square Method

#Preprocessing Input Data
X= np.array(eval(input("Input Values of X: ")))
print()
Y= np.array(eval(input("Input Variables of Y: ")))
print()

# Mean

X_mean=np.mean(X)

Y_mean=np.mean(Y)

num=0
denom=0

#to find sum of (xi-x') & (yi-y') & (xi-x')^2
for i in range(len(X)):
    num+=(X[i]-X_mean)*(Y[i]-Y_mean)
    denom+=(X[i]-X_mean)**2
    
#calculate slope

m=num/denom
print("Slope of the line is",m)
print()


#calculate intercept
b=Y_mean- m*X_mean

print("The value of slope and y intercept are:",m,"and",b)
print()

#Line Equation
y_predicted=m*X+b
print("The predicted values of Y are",y_predicted,end="")
print()

#to plot graph
plt.scatter(X,Y)
plt.plot(X,y_predicted,color='red')
plt.xlabel("X Values")
plt.ylabel("Y Values")
plt.show()


```

## Output:


![output_exp1](https://github.com/user-attachments/assets/ecab303c-a7a2-401c-8e1c-4cf0a21ae6c0)


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
