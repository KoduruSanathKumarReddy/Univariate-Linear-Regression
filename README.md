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
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```
'''
Developed by : Koduru Sanath Kumar Reddy
Reference number:21000648
'''
import numpy as np
import matplotlib.pyplot as plt
x = np.array([8,2,11,6,5,4,12,9,6,1])
y = np.array([2,10,3,6,8,12,1,4,9,14])
plt.scatter(x,y)
plt.show()
xmean = np.mean(x)
ymean = np.mean(y)
num=0
den=0
for i in range(len(x)):
    num+=(x[i]-xmean)*(y[i]-ymean)
    den+= (x[i]-xmean)**2
m = num/den
b = ymean - m*xmean
print(m,b)
ypred = m*x+b
print(ypred)

plt.scatter(x,y,color='red')
plt.plot(x,ypred,color='green')
plt.show()
```
## output
![inp](main.png)
![plot1](1.png)
![plot2](2.png)
## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
