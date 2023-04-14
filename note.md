# Data Structures 

The Data Structures course focuses on expanding our basic python skills and learning how to represent data better. These skills are crucial for all programmers as they make their leap from beginner to intermediate programmers.

## Matrices & List Comprehension 

A Matrix is a representation of numbers, symbols, expressions in 2 dimensional array. In python data structures can be made allowing us to have values in rows and columns, we can do this by making a list inside of a list.

![image](https://user-images.githubusercontent.com/129182651/232047400-071bb508-ff4f-433b-838e-a8b4a4b7b6e3.png)

There is no data structure called a "Matrix" instead we have to follow a set of rules when making a list inside of a list they are as followd.

* All rows must have the same number of values

* All columns must have the same number of values 

* All items in the 2D list must have the same data types

* SInce indexing always starts at 0, row 1 is technically located at matrix[0]

### Example of Matrix 

```python

Matrix_A = [ 
    [1,2,3,4],
    [5,6,7,8]
]

print('Row 1: %s' % matrix_a[0]) 
print('value at row 2 column 2: %s' % matrix_a[1][1])

```

## List Comprehension In Python 3 

List comprehension is concise method to create a list

We use this technique when:

* Te list is a result of some operations applied to all its items, 

* Its made from another form of iterable data 

* The list is a memeber of another form of iterable data that satifies a certain condition

### List Example 1:

Old Method: 

```python

squares = []
for i in range(10):
    squares.append(i ** 2)

print('Our result: %s' % squares)
```
New method: 
```python 
squares = [i**2 for i in range(10)]

print('Our new result: %s' % squares)
```
### List Example of 3:

```python 

vec = [[1,2,3], [4,5,6], [7,8,9]]

result = [value for row in vec for value in row]
print('Vec as a single list of values: %s' % result)
```
It is important to note that the order of your clauses matter

# Lesson 2: Map and Filter

## The Map Function
