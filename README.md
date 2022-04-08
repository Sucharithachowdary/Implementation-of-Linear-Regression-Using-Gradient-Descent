# Implementation-of-Linear-Regression-Using-Gradient-Descent

## AIM:
To write a program to implement the linear regression using gradient descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```

Program to implement the linear regression using gradient descent.

Developed by: Sucharithachowdary
RegisterNumber: 212221240021


import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
data=pd.read_csv("/content/student_scores - student_scores.csv")
data.head()
data.isnull().sum()
x=data.Hours
x.head()
y=data.Scores
y.head()
n=len(x)
m=0
c=0
l=0.001
loss=[]
for i in range(10000):
    ypred=m*x+c
    MSE=(1/n)*sum((ypred-y)*2)
    dm=(2/n)*sum(x*(ypred-y))
    dc=(2/n)*sum(ypred-y)
    c=c-l*dc
    m=m-l*dm
    loss.append(MSE)
    #print(m,c)
    ypred=m*x+c
plt.scatter(x,y,color="blue")
plt.plot(x,ypred)
plt.xlabel("study hours")
plt.ylabel("scores")
plt.title("study hour vs scores")
plt.plot(loss)
plt.xlabel("iteration")
plt.ylabel("loss")
    

```

## Output:
![linear regression using gradient descent](suchi.png)


## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
