# 8 Python Tips and Tircks You Might Not Know About

Video Link: [Put Link Here]()

In this video, we will look at eight Python programming tips and tricks you might not have known about. This will definitely help you write python codes in more efficient way.

- [Unpacking](#unpacking)
- [Negative Indexing](#negative-indexing)
- [Slicing](#slicing)
- [List, Set, Dictionary Comprehension](#list-set-dictionary-comprehension)
- [args and kwargs](#args-kwargs)
- [Set and Set Operations](#set-operations)
- [Chaining of Comparison Operators](#chaining-comparison-operators)
- [Ternary Operator](#ternary-opertor)

---
## Unpacking

Unpacking allows us to assign values of an iterable to a number of variables.

```python
a, b, c = (1, 2, 3)

print(a)
print(b)
print(c)
```

**Output**

```
1
2
3
```

**Swap Two Numbers using Unpacking**

```python
x = 66
y = 44

x, y = y, x

print('x =', x)
print('y =', y)
```

**Output**

```
x = 44
y = 66
```

---
## Negative Indexing

Python programming supports negative index values for iterable like lists, strings and tuples. The negative index gives us elements from the last.

```python
numbers = [5, 10, 15, 20, 25]

print(numbers[-1])

print(numbers[-3])
```

**Output**

```
25
15
```

---
## Slicing

Slicing allows us to create a new sequence from an existing sequence.

```Python
numbers = [5, 10, 15, 20, 25]

new_numbers = numbers[0:3]
print(new_numbers)
```

**Output**

```
[5, 10, 15]
```

**Remove the 0 from above code**

```Python
numbers = [5, 10, 15, 20, 25]

new_numbers = numbers[:3]
print(new_numbers)
```

**Output**

```
[5, 10, 15]
```

**Using step value**

```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8]
print(numbers[1:6:2])
```

**Output**

```
[2, 4, 6]
```

**Reverse a list using slicing**

```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8]

print(numbers[::-1])
```

**Output**

```
[8, 7, 6, 5, 4, 3, 2, 1]
```

---
## List, Set and Dictionary Comprehension

Comprehensions allow us to create lists, sets and dictionaries in a more elegant and Pythonic way using a single line expression.


Create List of first five powers of 2 using loop

```python
numbers = []

for i in range(1, 6):
  numbers.append(2**i)

print(numbers)
```

**Output**

```
[2, 4, 8, 16, 32]
```

**Same Program using List Comprehension**

```python
numbers = [2**i for i in range(1, 6)]

print(numbers)
```

**Output**

```
[2, 4, 8, 16, 32]
```

---
## *args and **kwargs

*args is used to accept a arbiratory number of arguments.

```python
def add(*args):
  total = 0
  for n in args:
    total += n
  return total

print(add())
print(add(1,2))
print(add(1,2,3,4,5))
```

**Output**

```
0
3
15
```

**kwargs is used to accept an arbitary number of key, value pairs.

```python
def printer(**kwargs):
  for x, y in kwargs.items():
    print(f'{x} - {y}')

printer(language='Python')
printer(name='Bill Gates', company='Microsoft')
```

**Output**

```
language - Python
name - Bill gates
company - Microsoft
```

---
## Set and Set Operations

Set in Python are like set in mathematics. A set cannot contain duplicate items and these items are not in any order.

**Set Difference**

```python
A = {10, 20, 20, 30, 40}
B = {30, 30, 40, 50, 60, 70}

print(A - B)
```

**Output**

```
{10, 20}
```

**Set Union**

```python
A = {10, 20, 20, 30, 40}
B = {30, 30, 40, 50, 60, 70}

print(A | B)
```

**Output**

```
{70, 40, 10, 50, 20, 60, 30}
```

**Set Intersection**

```python
A = {10, 20, 20, 30, 40}
B = {30, 30, 40, 50, 60, 70}

print(A & B)
```

**Output**

```
{40, 30}
```

---
## Chaining of Comparison Operators

Check if a person is greater than 18

```python
age = int(input("Enter age:"))

if age > 18 and age < 60:
  print("accepted")
else:
  print("rejected")
```

**Output**

```
Enter age: 30
accepted
```

**Using Operator Chaining**

```python
age = int(input("Enter age:"))

if 18 < age < 60:
  print("accepted")
else:
  print("rejected")
```

**Output**

```
Enter age:30
accepted
```

---
## Ternary Operator

Ternary Operator allows us to write if...else statements in a single expression.

Program to check if a number is odd or even

```python
number = int(input("Enter a number:"))

if number % 2:
  print("odd")
else:
  print("even")
```

**Output**

```
Enter a number: 8
even
```

**Using Ternary Operator**

```python
number = int(input("Enter a number:"))

parity = "odd" if number % 2 else "even"
print(parity)
```

**Output**

```
Enter a number: 8
even
```

---
