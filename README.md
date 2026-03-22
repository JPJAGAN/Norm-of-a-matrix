# NAME: JAGAN J P
# REG.NO: 212224230099
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
# Register No: 212224230099
# Developed By: JAGAN J P
# 1-Norm of a Matrix
import ast

A = ast.literal_eval(input())
cols = len(A[0])
max_sum = 0

for j in range(cols):
    col_sum = 0
    for i in range(len(A)):
        col_sum += abs(A[i][j])
    if col_sum > max_sum:
        max_sum = col_sum

print(f"{max_sum:.2f}")

# 2-Norm of a Matrix
import ast
import math

A = ast.literal_eval(input())

m = len(A)
n = len(A[0])

B = [[0]*n for _ in range(n)]
for i in range(n):
    for j in range(n):
        for k in range(m):
            B[i][j] += A[k][i]*A[k][j]

x = [1]*n

for _ in range(20):
    y = [0]*n
    for i in range(n):
        for j in range(n):
            y[i] += B[i][j]*x[j]
    norm = math.sqrt(sum(i*i for i in y))
    x = [i/norm for i in y]

num = 0
den = 0
for i in range(n):
    t = 0
    for j in range(n):
        t += B[i][j]*x[j]
    num += x[i]*t
    den += x[i]*x[i]

lam = num/den
print(f"{math.sqrt(lam):.2f}")

# Infinity Norm of a Matrix
import ast

A = ast.literal_eval(input())
max_sum = 0

for row in A:
    s = sum(abs(i) for i in row)
    if s > max_sum:
        max_sum = s

print(f"{max_sum:.2f}")

```
## Output:
### 1-Norm of a Matrix
<img width="453" height="411" alt="image" src="https://github.com/user-attachments/assets/3d3892eb-e71d-480e-8cf7-466fc1c7cb66" />

###
<img width="429" height="61" alt="image" src="https://github.com/user-attachments/assets/6fca1ad3-20a3-4038-bdad-b0aef3b0a888" />

### 2-Norm of a Matrix
<img width="475" height="862" alt="image" src="https://github.com/user-attachments/assets/6c0962c1-be0f-4a86-9a97-dcf96a25545b" />

###
<img width="396" height="70" alt="image" src="https://github.com/user-attachments/assets/ff53897f-cca6-4384-8c85-5c1125c783ed" />

###
<img width="338" height="57" alt="image" src="https://github.com/user-attachments/assets/fae254cf-01e1-4bb0-91a3-ca90abc92380" />

### Infinity Norm of a Matrix
<img width="455" height="321" alt="image" src="https://github.com/user-attachments/assets/40a5c2e7-b78a-4890-99c3-ce0ed5013511" />

###
<img width="380" height="70" alt="image" src="https://github.com/user-attachments/assets/272200f6-c4b9-4f75-8c83-fb83b2a1e5ae" />

## Result
Thus the program for 1-norm, 2-norm and Infinity norm of a matrix are written and verified.
