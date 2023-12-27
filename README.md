# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm
```
Step1 :
Import the numpy module to use the built-in functions for calculation.
Step 2:
Type the program to be executed.
Step 3:
Using the built-in function, we can find the solutions.
Step 4:
Print the value and end the program
```
## Program:
```
Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: Piritharaman R
RegisterNumber: 23013537
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
for i in range(n-1,-1,-1):
    res[i]=arr[i][n]
    for j in range(i+1,n):
        res[i]=res[i]-arr[i][j]*res[j]
    res[i]=res[i]/arr[i][i]
for i in range(n):
    print("X%d = %0.2f" %(i,res[i]),end=" ")
```

## Output:
![image](https://github.com/ramanpiritha/Gaussian/assets/147084116/a018d444-9c01-4fd0-a373-e24b8096c9f3)



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

