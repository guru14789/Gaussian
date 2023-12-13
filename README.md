# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm

## STEP 1:
Import the numpy module to use the built-in functions for calculation
## STEP 2:
Get input from the user for the number of unknows as n
## STEP 3:
Making numpy array of n x n+1 size and initializing to zeroes for augmented matrix
## STEP 4:
Making numpy array of n size and initializing to zero for storing solution vector
## STEP 5:
Reading arguments matrix coefficients
## Step 6:
Applying Gauss elimination i.e., interchanging the rows and columns, multiplying them with a scalar, and adding the rows with a multiplied scalar
## STEP 7:
Applying back substitution
## STEP 8:
Displaying the solution
## STEP 9:
End of program

## Program:
```
Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: SREEKUMAR S
RegisterNumber: 23008070

import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())

for i in range(n):
    if a[i][i]==0.0:
       sys.exit("Divided bby zero detected!")
    
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        
        for k in range(n+1):
            a[j][k]=a[j][k]-ratio*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]

for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
for i in range(n):
    print("X%d = %0.2f" %(i,x[i]),end=' ')
```

## Output:
![gaussian 1](https://github.com/guru14789/Gaussian/assets/151705853/8a411f11-dbe4-486a-84e8-ccb65975eaf1)



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using Python programming.

