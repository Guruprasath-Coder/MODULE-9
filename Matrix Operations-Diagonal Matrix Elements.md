# Matrix Operations-Diagonal Matrix Elements Printer 🧮

This Python program reads a matrix of any size from the user and prints **only the diagonal elements**, leaving other elements blank in the output.

## 📌 Aim

To write a Python program that prints only the diagonal elements of a given matrix.

## 🧠 Algorithm

1. Read the number of rows and columns from the user.
2. Initialize an empty matrix of size `rows × columns`.
3. Populate the matrix with user input.
4. Display the full matrix.
5. Iterate through the matrix and:
   - If `i == j`, print the element (main diagonal).
   - Else, print a blank space.
6. Print a newline after each row.

## 🖥️ Program
```python
# Function to create a matrix
def create_matrix(rows, cols):
    matrix = []
    print("Enter the elements row-wise:")
    for i in range(rows):
        row = []
        for j in range(cols):
            val = int(input(f"Enter element [{i}][{j}]: "))
            row.append(val)
        matrix.append(row)
    return matrix


# Read size of matrix
rows = int(input("Enter number of rows: "))
cols = int(input("Enter number of columns: "))

# Create matrix
matrix = create_matrix(rows, cols)

print("\nOriginal Matrix:")
for row in matrix:
    print(row)

print("\nDiagonal Elements of the Matrix:")
for i in range(rows):
    for j in range(cols):
        if i == j:
            print(matrix[i][j], end=" ")
        else:
            print(" ", end=" ")
    print()  # New line after each row


### Output:
Enter number of rows: 3
Enter number of columns: 3
Enter the elements row-wise:
Enter element [0][0]: 1
Enter element [0][1]: 2
Enter element [0][2]: 3
Enter element [1][0]: 4
Enter element [1][1]: 5
Enter element [1][2]: 6
Enter element [2][0]: 7
Enter element [2][1]: 8
Enter element [2][2]: 9

Original Matrix:
[1, 2, 3]
[4, 5, 6]
[7, 8, 9]

Diagonal Elements of the Matrix:
1      
   5   
      9

## Result
Thus, the Python program successfully prints only the diagonal elements of a given matrix.
