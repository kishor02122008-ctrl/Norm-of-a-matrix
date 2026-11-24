# Norm of a matrix
## Aim
To write a program to find the 1-norm, 2-norm and infinity norm of the matrix and display the result in two decimal places.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
	1. Get the input matrix using np.array()   
    2. Find the 2-norm of the matrix using np.linalg.norm()
	3. Print the norm of the matrix in two decimal places.
## Program:
```Python
# Register No: Kishor.M
# Developed By: 26018383
# 1-Norm of a Matrix
import ast

matrix = ast.literal_eval(input())
a = len(matrix)
b = len(matrix[0])

norm = 0

for j in range(b):
    total = 0
    for i in range(a):
        total = total + abs(matrix[i][j])
        
    if total > norm:
        norm = total
        
print("{:.2f}".format(norm))



# 2-Norm of a Matrix
import ast, math

A = ast.literal_eval(input())
n = len(A[0])
v = [1.0] * n

for _ in range(1000):
    w = [sum(A[k][i]*A[k][j]*v[j] for k in range(len(A)) for j in range(n)) for i in range(n)]
    s = math.sqrt(sum(x*x for x in w))
    v = [x/s for x in w]
    
r = math.sqrt(sum(sum(A[k][i]*v[i] for i in range(n))**2 for k in range(len(A))))
print(f"{r:.2f}")



# Infinity Norm of a Matrix
import ast
A = ast.literal_eval(input())
result = max(sum(abs(x) for x in row) for row in A)
print(f"{result:.2f}")




```
## Output:
### 1-Norm of a Matrix
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/69bf9c31-71ed-420a-8459-0be49a4ed538" />


### 2-Norm of a Matrix
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/fe360509-e747-44a0-b1be-bd7a2b1a06bc" />


### Infinity Norm of a Matrix
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/cfcdf2af-50a1-42f9-9fb5-2eb1f9c82982" />


## Result
Thus the program for 1-norm, 2-norm and Infinity norm of a matrix are written and verified.
