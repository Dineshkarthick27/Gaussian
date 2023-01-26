# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.
## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm


1. Import the requried libraries for a guassian elimination.

2. Get the user input.

3. Use the for loop for a range of n+1,n.

4. Apply the guassian elimination.

5. Use the for loop with condition statment.

6. Applyn the back substiution

7.Print the program.

## Program:
```pythone
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: Dinesh Karthick.K,J
RegisterNumber: 22005847

import numpy as np
import sys 
n=int(input()) #input
a=np.zeros((n,n+1))
#print(a)
x=np.zeros(n)
#to get the A matrix
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
    #print(a)
#apply gaussian elimination
for i in range(n):
    if a[i][j]==0.0:
        sys.exit('Divide by zero found')    
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k]=a[j][k]-ratio*a[i][k]
#back substitution
x[n-1]=a[n-1][n]/a[n-1][n-1] 
for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
#display soln
for i in range(n):
    print('X%d = %0.2f'%(i,x[i]),end=' ')
```


## Output:
![tfd](https://user-images.githubusercontent.com/120552008/214863460-1b53679c-a0e7-4cd4-ab2f-6f1653b2f1c3.png)

## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

