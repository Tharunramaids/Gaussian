# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
### Step1 
import the numpy module to use the build-in functions for calculation 
### Step2
 Prepare the loist from each linear equations and assign in np.array()
### Step3 
 using the np.linalg.solve().we can find the solutions
### Step4
 End the program

## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: Tharun R
RegisterNumber: 24005919
*/
import numpy as np
n=int(input())
matrix=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        matrix[i][j]=int(input())
for i in range(n):
    for j in range(i+1,n):
        ratio=matrix[j][i]/matrix[i][i]
        for k in range(n+1):
            matrix[j][k]=matrix[j][k]-ratio*matrix[i][k]
#black substitution 
x[n-1]=matrix[n-1][n]/matrix[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=matrix[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-matrix[i][j]*x[j]
    x[i]=x[i]/matrix[i][i]
for i in range(n):
    print("X%d = %0.2f" %(i,x[i]),end=" ")
```

## Output:
![output](<Screenshot 2024-12-04 115411.png>)

## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

