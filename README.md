# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.Get the independent variable X and dependent variable Y.
<br>
2.Calculate the mean of the X -values and the mean of the Y -values.
<br>
3.Find the slope m of the line of best fit using the formula. 
![image](https://github.com/user-attachments/assets/1f45b537-a8d9-4559-8798-e2f451e9497e)
<br>
4.Compute the y -intercept of the line by using the formula:
![image](https://github.com/user-attachments/assets/de13ee75-ba6d-459b-acea-79657d3bd610)
<br>
5.Use the slope m and the y -intercept to form the equation of the line.
<br>
6.Obtain the straight line equation Y=mX+b and plot the scatterplot.
<br>
## Program:
```
import numpy as np 
import matplotlib.pyplot as plt
x = np.array([0,1,2,3,4,5,6,7,8,9])
y = np.array([1,3,2,5,7,8,8,9,10,12])
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
```
## Output:

![Screenshot 2025-05-21 080409](https://github.com/user-attachments/assets/74e39ed1-2056-49aa-9136-2e508f1efdc5)
![image](https://github.com/user-attachments/assets/566450ce-103f-4025-92c5-b1f59b2fa5a3)

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
