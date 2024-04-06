# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. 
2. 
3. 
4. 

## Program:
'''Program to solve a matrix using Gaussian elimination without partial pivoting.

Developed by: R.sivakumar

RegisterNumber: 23013501

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
      
      for k in range (n+1):
      
          arr[j][k]=arr[j][k]-ratio*arr[i][k]
          
res[n-1]=arr[n-1][n]/arr[n-1][n-1]

for i in range(n-2,-1,-1):

     res[i]=arr[i][n]
     
     for j in range(i+1,n):
     
          res[i]=res[i]-arr[i][j]*res[j]
          
     res[i]=res[i]/arr[i][i]
     
for i in range(n):

    print("X%d = %0.2f" %(i,res[i]),end=" ")
    

## Output:
<img width="635" alt="Screenshot 2024-04-06 133852" src="https://github.com/SIVAmech123/Gaussian/assets/151629067/42856f5d-514f-4e3b-8a3f-8b8cc0d71743">
<img width="574" alt="Screenshot 2024-04-06 133908" src="https://github.com/SIVAmech123/Gaussian/assets/151629067/d55f8840-4894-4d5b-b5b8-5f9f6b874c6f">
<img width="545" alt="Screenshot 2024-04-06 133920" src="https://github.com/SIVAmech123/Gaussian/assets/151629067/600e914f-634f-47e0-8153-5fda407761f6">



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

