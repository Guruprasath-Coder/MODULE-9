# 🧮 SORTING ALGORITHMS: Insertion Sort Using a Class

This program demonstrates how to implement the **Insertion Sort algorithm** using a Python class. It allows the user to input a list of numbers, sorts them using the insertion sort technique, and displays the sorted list.

---

## 🎯 Aim

To develop a Python class with functions to:
- Create a list of integers
- Sort it using the **Insertion Sort** algorithm
- Display the sorted list

---

## 🧠 Algorithm

1. **Start the program**
2. **Define a class** `InsertionSorter`
3. Inside the class:
   - `create_list()`:
     - Read number of elements
     - Store them in a list
   - `insertion_sort()`:
     - Iterate from the second element to the end
     - Move elements greater than the key to one position ahead
     - Insert the key at the correct position
   - `print_list()`:
     - Print the sorted list
4. **Create an object** of the class
5. **Call** the methods in order: `create_list()`, `insertion_sort()`, and `print_list()`
6. **End the program**

---

## 💻 PROGRAM:
```
  class Numbers:
      def __init__(self, N=0):
          self.N = int(input())
      def create_list(self):
          self.L=[]
          for i in range(self.N):
              x=int(input())
              self.L.append(x)
      def sorting(self):
          for i in range(self.N):
              mi=i
              for j in range(i+1,self.N):
                  if self.L[j]<self.L[mi]:
                      mi=j
              (self.L[i],self.L[mi])=(self.L[mi],self.L[i])
      def print_List(self):
          for i in range(self.N):
              print(self.L[i])
```
## OUTPUT:

![image](https://github.com/user-attachments/assets/fe7e5e5a-3200-4fe9-b9ac-5f7e482b4eab)

## RESULT:
The Python class successfully implements the Insertion Sort algorithm, sorts the user-provided list, and displays the sorted output.
