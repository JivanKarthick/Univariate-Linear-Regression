# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![1](https://user-images.githubusercontent.com/121165867/214810891-6c76e30a-175c-4a59-86f5-fef10c62774a.png)

4.	Compute the y -intercept of the line by using the formula:
![2](https://user-images.githubusercontent.com/121165867/214810928-4013a9ba-8949-4062-bf02-0ef02d24ac90.png)
 
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```python
Program for Univariate linear regression using the least squares method.
Developed by:Jivan Karthec.B.S
RegisterNumber: 22004763
 
import numpy as np

# Preprocessing Input data

X = np.array(eval(input()))
Y = np.array(eval(input()))

# Building the model
# write your code here
X_mean=np.mean(X)
Y_mean=np.mean(Y)

num = 0
denom = 0

for i in range(len(X)):
    num += (X[i]-X_mean)*(Y[i]-Y_mean)
    denom += (X[i]-X_mean)**2
    
m = num/denom

c = Y_mean - m*X_mean
print (m, c)

#Predict the output
Y_mean = m*X+c
print (Y_mean)

import matplotlib.pyplot as plt
plt.scatter(X,Y)
plt.plot(X,Y_pred,color="purple")
plt.show()
```
## Output
![3](https://user-images.githubusercontent.com/121165867/214810999-4f3b97c4-9987-4150-81c1-af219a0074dd.png)

![4](https://user-images.githubusercontent.com/121165867/214811042-063d82d2-e6ff-477d-a7c7-7fbe7aa6dd33.png)


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
