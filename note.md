# Data Structures 

The Data Structures course focuses on expanding our basic python skills and learning how to represent data better. These skills are crucial for all programmers as they make their leap from beginner to intermediate programmers.

## Matrices & List Comprehension 

A Matrix is a representation of numbers, symbols, expressions in 2 dimensional array. In python data structures can be made allowing us to have values in rows and columns, we can do this by making a list inside of a list.

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

* The list is a result of some operations applied to all its items, 

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

# Map and Filter

## The Map Function

The map function is to apply a function to iterable data

### Formating
```python 
map(function_name, sequence) 

-- function_name: any function (built-in or selfmade) that returns a desired value of choice
-- sequence: any iterable data type

```
### Example 

```python

def square(num):
    ''' squares the given num argument '''
    return num ** 2
# end of square

array = list(range(1,11))
square_array = list(map(square, array))

print('Original Array:', array)
print('Array Squared:', square_array)

```
An important thing to note is that the map function doesn't return a specific data type, instead a some form of iterable data, meaning after we apply the function we use a list function on it. 

Its not needed to use methods with a map, since there is a high probability that there is already a method for what is needed. 

## Filter function 

The filter function is to filter out items from a data set that meets a certain condition. 

### Formatting

```python
filter(bool_returning_function, sequence)

-- function: The function name we provide for filter() must be return a boolean value ... should also be able handle the items inside the sequence as its arguments
-- sequence: any iterable data type
```
### Example: 

```python 

def isOdd(x):
    ''' isOdd() returns True if x is odd.'''
    return x % 2 != 0

array = list(range(1,101))
odds = list(filter(isOdd, array))

print('Odd Numbers from 1 to 100:', odds)

```

# Tuples

Strings and list are very similar data types with some key differences, these differences can cause it to be annoying. But when using a tuple all these issues 

## How to use tuples: 

* Tuples are declared with parenthesis ()
* () is an empty tuple
* (50,) is a singleton tuple, the comma is required
* Tuples are sliceable, therefore indexxable using square brackets

### Example: 

```python

tup = ('C', ' Java', 'Python')
empty_tup = ()
single_tup = ('Park',)

print(tup)
print(empty_tup)
print(single_tup)

```

### Tuple Operators: 

```python

# Concatenation: Joining two tuples
a = (1,2,3)
b = (4,5,6)
concat_result = a + b
print('a+b:', concat_result)


# Repetition: Repeating a list multiple times
c = ('Hi!',)
repet_result = c * 3
print('c*3', repet_result)

# Membership: Check if a value exists in a tuple
d = a + b + c
print('d:', d)
print('\'Hi!\' in d:', 'Hi!' in d)
print('7 in d:', 7 in d)

```
Tuples are iterable, indexable and sliceable

### Packing and Unpacking 

* Packing collect multiple variable’s values and assign it to a single variable

* Unpacking help us assign certain values from a tuple to different variables

* This becomes very useful skill when combined with variable arguments for Function Definition and Function Calls

```python
# Examine the following code

# Packing
var_1 = 2
var_2 = 3
var_3 = 5

prime = var_1, var_2, var_3

print('Packed prime values:', prime)

# Unpacking and Repacking
fib = (0, 1, 1, 2, 3, 5, 8)

fib_0, fib_1, fib_n = fib[0], fib[1], fib[2:]
print('fib_0:', fib_0)
print('fib_1:', fib_1)
print('fib_n:', fib_n)
```
# Sets 
A set is an unordered collection with no duplicate elements, it is a mathematical way to describe collections of diffrernt unique objects.

In Python, we create sets by placing all the elements inside curly braces {} , separated by comma. A set can have any number of items and they may be of different types (integer, float, tuple, string etc.). But a set cannot have mutable elements like lists, sets or dictionaries as its elements.
* Sets aren’t sliceable nor indexable
* Sets cannot have sets inside them
* Sets do not have order; nor order of insertion
* Sets cannot guarantee that their values will be in order
* Sets do not record a value’s position
* Two set are consided disjointed when two sets share no common value.


```python

# Set definition examples:
example_set1 = {1, 2, 3}
example_set2 = {'h','e','l','l','o'}

print('example_set1:', example_set1)
print('example_set2:', example_set2) # Notice there is only 1 'l'; Also notice the order of the values outputted
```
Built in functions include:
* Len
* Min
* Max
* ``` example_set = set('hello')``` setting an iterable to a set
* list to set and tuple to set

Basic Membership Operators

Membership is one of the key operations with set because:

* A set has no duplicates
* A set’s membership operation is one of the fastest operations compared to strings, lists, or tuples this will be covered more when we look at the concept of: complexity
* By using membership operator, we can be certain a target exists or does not exist in our data

### Set operators: 

* Union: The joining/combining of two sets, the union operator is "|"
* Intersection: Members/Items that only exists in both sets, the intersection operator is "&"
* Difference: Members/items that only exists in the first set and not the second set, the difference operator is "-"
* Symmetric Difference: : Members/items that exists one or the other set but not both sets, the symmetric difference operator is "^"
* Proper Subset: A is proper subset of B if all members of A is found in B, but A cannot be exactly the same as B. This is a boolean operator, the operator is "<" 
* Subset: A is a Proper Subset of B if A < B is True, but A can equal to B unlike a proper subset also a boolean, the operator is <=
* Proper Superset: A is a proper superset of B if A has all the values of B and more, but they are not equal to each other also a boolean, the operator is ">"
* Superset: A is a superset of B if A > B or A == B also a boolean, the operator is ">="

# Dictionaries 

Dictionary in Python 3 is a data type that stores a collection of (key, value) pairs, where each possible key appears at most once in the collection. Common operations with dictionaries include adding a pair, removing a pair, modifying an existing pair, and looking up a value associated with a particular key. Dictionaries in Python 3 are defined using curly braces {} and use a key-value pair format. For example:

```python
# Dictionary Example
sammy = {
    'username': 'sammy',
    'online': True,
    'followers': 42
}

```

Dictionary properties include keys and values. Keys are unique addresses for a dictionary value's location and must be immutable (e.g., strings, numbers, tuples, frozenset) and unique. Values can be of any data type. Dictionaries can be updated by modifying existing values using the key, adding new values by creating a new key, or overwriting a value at an existing key by referencing and recreating the value for it.

Dictionaries can be deleted using the del keyword, which can delete a specific key-value pair or the entire dictionary. Membership in a dictionary can be checked using the in and not in operators. Built-in functions can also be used with dictionaries, such as len() to get the size of the dictionary, max() and min() to get the largest and smallest keys, str() to convert the dictionary to a string, and list() to convert the dictionary to a list.

Dictionaries can be duplicated using the copy() method, which creates a shallow copy of the dictionary, or using the fromkeys() method, which creates a new dictionary with the same keys but with all values set to None.



