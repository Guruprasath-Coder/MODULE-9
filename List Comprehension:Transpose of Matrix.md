# 🧮 List Comprehension:Transpose of Matrix 

## 🎯 AIM:
To write a Python program to compute the **transpose** of a matrix using **list comprehension**.

---

## 🧠 ALGORITHM:

1. **Start**
2. Create variables `r` and `c` to represent the number of rows and columns of the matrix.
3. Get the values of `r` and `c` from the user.
4. Define a function `create(r, c)` to create the matrix by reading the elements from the user.
5. Use **list comprehension** to calculate the transpose of the matrix.
6. Print the transposed matrix.
7. **Stop**

---

## 💻 PROGRAM:
```python
# Function to create matrix
def create(r, c):
    matrix = []
    print("Enter the elements row-wise:")
    for i in range(r):
        row = []
        for j in range(c):
            val = int(input(f"Enter element [{i}][{j}]: "))
            row.append(val)
        matrix.append(row)
    return matrix


# Main program
r = int(input("Enter number of rows: "))
c = int(input("Enter number of columns: "))

matrix = create(r, c)

# Transpose using list comprehension
transpose = [[matrix[j][i] for j in range(r)] for i in range(c)]

print("\nOriginal Matrix:")
for row in matrix:
    print(row)

print("\nTranspose of Matrix:")
for row in transpose:
    print(row)


## OUTPUT:
Enter number of rows: 2
Enter number of columns: 3
Enter the elements row-wise:
Enter element [0][0]: 1
Enter element [0][1]: 2
Enter element [0][2]: 3
Enter element [1][0]: 4
Enter element [1][1]: 5
Enter element [1][2]: 6

Original Matrix:
[1, 2, 3]
[4, 5, 6]

Transpose of Matrix:
[1, 4]
[2, 5]
[3, 6]

## RESULT:
Thus, the Python program successfully computes the transpose of a matrix using list comprehension.
