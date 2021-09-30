# 7 Python Built-in Functions You Should Know

Video Link: [https://youtu.be/2_xfAoJFWBY]()

In this video, we will look at seven different Python Built-in functions that will help you write more pythonic code.

- [`all()` and `any()`](#all-any)
- [`enumerate()`](#enumerate)
- [`zip()`](#zip)
- [`dir()`](#dir)
- [`eval()`](#eval)
- [`map()`](#map)
- [`filter()`](#filter)


## Python `all()` and `any()`

Code For `any()`

```python
boolean_list = [True,True]
print(all(boolean_list))
```

**Output**

```
True
```

Change second element to False.

```python
boolean_list = [True,False]
print(all(boolean_list))
```

**Output**

```
False
```
---

Code for `all()`

```python
boolean_list = [True,False]
print(any(boolean_list))
```

**Output**

```
True
```

Program to check if a list has all odd numbers

```python
numbers = [1,3,5,7,9]
all_odd = all([n%2 for n in numbers])
print(all_odd)
```

**Output**

```
True
```

---

## Python `enumerate()`

First Program

```python
name_list = ['Mary', 'Anna', 'Alexandra']
marks_list = [70, 45, 96]

counter = 0
for student in name_list:
    if student == "Anna":
        print(marks_list[counter])
        break
    counter += 1
```

**Output**

```
45
```

Same program using `enumerate()`

```python
name_list = ['Mary', 'Anna', 'Alexandra']
marks_list = [70, 45, 96]

for counter, student in enumerate(name_list):
    if student == "Anna":
        print(marks_list[counter])
        break
```

**Output**

```
45
```

---

## Python `zip()`

Group the corresponding elements of two lists.

```python
number_list = [1, 2, 3]
str_list = ['one', 'two', 'three']

result = zip(number_list, str_list)
print(list(result))
```

**Output**

```
[(1, 'one'), (2, 'two'), (3, 'three')]
```

Use `zip()` instead of `enumerate()` in earlier code

```python
name_list = ['Mary', 'Anna', 'Alexandra']
marks_list = [70, 45, 96]

for student, marks in zip(name_list, marks_list):
    if student == "Anna":
        print(marks)
        break
```

**Output**

```
45
```

---

## PythoN `dir()`

Returns all the attributes and methods present inside list

```python
numbers_list = [1, 2]
print(dir(numbers_list))
```

**Output**

```
['__add__', '__class__', '__contains__', '__delattr__', '__delitem__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__getitem__', '__gt__', '__hash__', '__iadd__', '__imul__', '__init__', '__init_subclass__', '__iter__', '__le__', '__len__', '__lt__', '__mul__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__reversed__', '__rmul__', '__setattr__', '__setitem__', '__sizeof__', '__str__', '__subclasshook__', 'append', 'clear', 'copy', 'count', 'extend', 'index', 'insert', 'pop', 'remove', 'reverse', 'sort']
```

List out all definition of math module

```python
import math

print(dir(math))
```

**Output**

```
['__doc__', '__loader__', '__name__', '__package__', '__spec__', 'acos', 'acosh', 'asin', 'asinh', 'atan', 'atan2', 'atanh', 'ceil', 'comb', 'copysign', 'cos', 'cosh', 'degrees', 'dist', 'e', 'erf', 'erfc', 'exp', 'expm1', 'fabs', 'factorial', 'floor', 'fmod', 'frexp', 'fsum', 'gamma', 'gcd', 'hypot', 'inf', 'isclose', 'isfinite', 'isinf', 'isnan', 'isqrt', 'ldexp', 'lgamma', 'log', 'log10', 'log1p', 'log2', 'modf', 'nan', 'perm', 'pi', 'pow', 'prod', 'radians', 'remainder', 'sin', 'sinh', 'sqrt', 'tan', 'tanh', 'tau', 'trunc']
```

---

## Python `eval()`

Runs the string passed as python expression

```python
x = 1
print(eval('x + 1'))
```

**Output**

```
2
```

Create command line calculator

```python
while True:
    print(eval(input(">>> ")))
```

**Output**

```
4 + 5
9
```

---

## Python `map()`

Create a new list with squared numbers from the original list

```python
numbers = [1, 2, 3, 4, 5]

squared_nums = []

square = lambda n: n**2

for num in numbers:
    squared_nums.append(square(num))

print(squared_nums)
```

**Output**

```
[1, 4, 9, 16, 25]
```

Solve the same problem using `map()`

```python
numbers = [1, 2, 3, 4, 5]

squared_nums = map(lambda n: n ** 2, numbers)
print(list(squared_nums))
```

**Output**

```
[1, 4, 9, 16, 25]
```

---

## Python `filter()`

Filter out even numbers from the list using `filter()`

```python
numbers = [234, 3245 ,639, 550, 654]

even_numbers = list(filter(lambda n: n % 2 ==0, numbers))
print(even_numbers)
```

**Output**

```
[234, 550, 654]
```

---

### Things to Take Away from this video

- `all()` - returns `True` if all elements of an iterable are `True`
- `any()` - returns `True` if any element of the iterable is `True`
- `enumerate()` - adds counter to an iterable and returns it
- `zip()` - aggregrates elements of multiple iterables into tuples
- `dir()` - returns all attributes and methods of an object
- `eval()` - runs the string passed to it as a python expression
- `map()` - applies a given function to each element of an iterable
- `filter()` -  filters out only the element for which the function returns `True`