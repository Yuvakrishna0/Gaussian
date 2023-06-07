# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. get the input from the user
2. assign a variable for storing the result
3. write a code to solve the matrix
4. display the result

## Program:
```
'''Program to solve a matrix using Gaussian elimination with partial pivoting.
Developed by: yuva krishna k
RegisterNumber: 212222110056
'''
import numpy as np
n=int(input())
arr=np.zeros((n,n+1))
res=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        arr[i][j]=int(input())
for i in range(n):
    for j in range(i+1,n):
        ratio=arr[j][i]/arr[i][i]
        for k in range(n+1):
            arr[j][k]=arr[j][k]-ratio*arr[i][k]
res[n-1]=arr[n-1][n]/arr[n-1][n-1]
for i in range(n-2,-1,-1):
    res[i]=arr[i][n]
    for j in range(i+1,n):
        res[i]=res[i]-arr[i][j]*res[j]
    res[i]=res[i]/arr[i][i]
for i in range(n):
    print("X%d = %0.2f" %(i,res[i]),end=" ")
    
```

## Output:

![Screenshot (81)](https://github.com/Yuvakrishna0/Gaussian/assets/117915037/ce6b0b2e-ef2c-48cb-865f-c9db6d80e7ed)

## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

