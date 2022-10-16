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
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: VASANTHAN
RegisterNumber: 212220220052 
*/
```

import files
import numpy as np
import matplotlib.pyplot as plt

#assign input

X=np.array([0,1,2,3,4,5,6,7,8,9])
Y=np.array([1,3,2,5,7,8,8,9,10,12])


#mean values of input

X_mean=np.mean(X)
print("X_mean =",X_mean)
Y_mean=np.mean(Y)
print("y_mean =",Y_mean)

num=0
denum=0

for i in range(len(X)):
  num+=(X[i]-X_mean)*(Y[i]-Y_mean)
  denum+=(X[i]-X_mean)**2

#find m
print("find m")
m=num/denum
print("m=",m)

#find b
print("find b")
b=(Y_mean)-(m*X_mean)
print("b =",b)

#find Y_pred
print("find Y_pred")
Y_pred=m*X+b
print("Y_pred =",Y_pred)

#plot graph

plt.scatter(X,Y,color='orange')
plt.plot(X,Y_pred,color='maroon')
print("Graph")
plt.show()


## Output:
![ss1](https://user-images.githubusercontent.com/115924983/196039058-6ad3ccff-0380-4372-ae33-16b16449f074.png)

![ss2](https://user-images.githubusercontent.com/115924983/196039071-9be90602-1cfc-4013-97e9-8702c61622a0.png)

![ss3](https://user-images.githubusercontent.com/115924983/196039082-39ab53dc-0b9b-4134-a9ac-b6675dd18a25.png)

![ss4](https://user-images.githubusercontent.com/115924983/196039087-855a9442-1180-4080-9f87-41f0c951d828.png)

![ss5](https://user-images.githubusercontent.com/115924983/196039092-699a1ae4-11f5-4de6-a66a-bebe3485addd.png)

![ss6](https://user-images.githubusercontent.com/115924983/196039096-d03b8455-ae66-4730-8419-f74368d579d2.png)

![ss7](https://user-images.githubusercontent.com/115924983/196039105-075c8e3f-8789-4ab3-9e7c-a6394b11c65c.png)

![ss8](https://user-images.githubusercontent.com/115924983/196039115-7aee9d04-2ead-4d11-8c82-e8535f59ae7f.png)

![ss9](https://user-images.githubusercontent.com/115924983/196039122-83369e9c-559a-4b54-9a39-c47f83fc4101.png)

![ss10](https://user-images.githubusercontent.com/115924983/196039131-4d33b2c0-754b-4e94-b382-cdfc51f745d5.png)

![ss11](https://user-images.githubusercontent.com/115924983/196039136-0be29987-135b-4fde-99c0-9fda524d5c37.png)

![ss12](https://user-images.githubusercontent.com/115924983/196039152-f8680a2f-e9d4-48ec-a971-b9d868ecdd16.png)


## Graph:
![ss13](https://user-images.githubusercontent.com/115924983/196039195-e505034d-e972-47ad-9221-84f33f4ed09d.png)



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
