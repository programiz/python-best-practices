# Python `map()` and `filter()`

Video Link: [https://youtu.be/kYIrDMbqunw](https://youtu.be/kYIrDMbqunw)

In this video, we learned how to use `map()` and `filter()` in Python with the help of examples.

**Programs in the Video**

- [Lambda functions](#lambda-functions)
- [Python `map()` function](#python-map-function)
- [Python `filter()` function](#python-filter-function)

---

The builtin functions like `map()` and `filter()` allow us to write simpler, shorter and more Pythonic code in place of
using loops and branching.

Let's first recap `lambda` functions.

## Lambda Functions

Lambda functions are single-line functions defined without a name.

```python
# def add(n1, n2):
#     return n1 + n2

add = lambda n1, n2: n1 + n2

print(add(10, 20))
```

**Output**

```
30
```

---

## Python `map()` function

Suppose we have a list like this:

```python
numbers = [1, 2, 3, 4, 5]
```

We have to create a new list with all the squares of the numbers from this list.

For this, we would normally use a `for` loop and apply the square to each item:

```python
numbers = [1, 2, 3, 4, 5]

squared_nums = []

square = lambda n: n ** 2

for num in numbers:
    squared_nums.append(square(num))

print(squared_nums)
```

**Output**

```
[1, 4, 9, 16, 25]
```

This same task can be done in a more elegant way using `map()`:

```python
numbers = [1, 2, 3, 4, 5]

squared_nums = map(lambda n: n ** 2, numbers)
print(squared_nums)
```

**Output**

```
<map object at 0x7efd7e693070>
```

The `map()` function returns an iterator object. Let's use the `list()` function to convert this iterator back to a
list:

```python
numbers = [1, 2, 3, 4, 5]

squared_nums = list(map(lambda n: n ** 2, numbers))
print(squared_nums)
```

**Output**

```
[1, 4, 9, 16, 25]
```

We can also pass multiple iterable arguments to `map()`:

```python
num1 = [4, 5, 6]
num2 = [5, 6, 7]

result = map(lambda n1, n2: n1 + n2, num1, num2)
print(list(result))
```

**Output**

```
[9, 11, 13]
```

---

## Python `filter()` function

The `filter()` function filters out only the elements for which the given function returns `true`:

```python
numbers = [234, 3245, 639, 550, 654]

even_numbers = list(filter(lambda n: n % 2 == 0, numbers))
print(even_numbers)
```

**Output**

```
[234, 550, 654]
```

---

### Things to Take Away from this Video

- Use `map()` to apply a function to each element of an iterable.
- Use `filter()` to filter out values of an iterable if they don't match the specified condition.