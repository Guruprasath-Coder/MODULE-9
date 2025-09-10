# # ➖ Matrix Operations-Matrix Subtraction in Python

## 🎯 AIM:
To write a Python program that reads two matrices from the user and performs matrix subtraction.

---

## 🧠 ALGORITHM:

1. **Start**
2. Create variables `r` and `c` for rows and columns
3. Get the values of `r` and `c` from the user
4. Define a function `create_matrix(n, m)` to:
   - Prompt user for each matrix element
   - Append each row to form a complete matrix
5. Call the `create_matrix()` function twice to read two matrices `A` and `B`
6. Define a loop to subtract the elements of matrix `B` from matrix `A`
7. Store the result in a new matrix `C`
8. Print the resulting matrix `C`
9. **Stop**

---

## 💻 PROGRAM:
```python
# Function to create matrix
def create_matrix(r, c, name):
    matrix = []
    print(f"\nEnter elements of Matrix {name}:")
    for i in range(r):
        row = []
        for j in range(c):
            val = int(input(f"Enter element [{i}][{j}] for Matrix {name}: "))
            row.append(val)
        matrix.append(row)
    return matrix


# Read rows and columns
r = int(input("Enter number of rows: "))
c = int(input("Enter number of columns: "))

# Create matrices A and B
A = create_matrix(r, c, "A")
B = create_matrix(r, c, "B")

# Subtract matrices (A - B)
C = [[A[i][j] - B[i][j] for j in range(c)] for i in range(r)]

# Display results
print("\nMatrix A:")
for row in A:
    print(row)

print("\nMatrix B:")
for row in B:
    print(row)

print("\nResult of A - B:")
for row in C:
    print(row)


## OUTPUT:
Enter number of rows: 2
Enter number of columns: 2

Enter elements of Matrix A:
Enter element [0][0] for Matrix A: 5
Enter element [0][1] for Matrix A: 6
Enter element [1][0] for Matrix A: 7
Enter element [1][1] for Matrix A: 8

Enter elements of Matrix B:
Enter element [0][0] for Matrix B: 1
Enter element [0][1] for Matrix B: 2
Enter element [1][0] for Matrix B: 3
Enter element [1][1] for Matrix B: 4

Matrix A:
[5, 6]
[7, 8]

Matrix B:
[1, 2]
[3, 4]

Result of A - B:
[4, 4]
[4, 4]

## RESULT:
Thus, the Python program successfully performs matrix subtraction of two user-defined matrices.
