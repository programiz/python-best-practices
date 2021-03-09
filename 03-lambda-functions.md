# Python `lambda` (anonymous) Functions

Video Link: [https://youtu.be/dX6lWSp7pP4](https://youtu.be/dX6lWSp7pP4)

In this video, we learned to create and use lambda functions in Python with the help of examples.

**Programs in the Video**

- [Create Lambda Functions](#create-lambda-functions)
- [Lambda functions as keys to `sort()`](#lambda-functions-as-keys-to-sort)

---

## Create Lambda Functions

Lambda functions are single-line functions defined without a name.

Let's first start with a simple function that takes in an argument and doubles it.

```python
def double(n):
    return n * 2


print(double(10))
```

**Output**

```
20
```

Wouldn't it be neat if we could write this one-liner function in a more condensed way?

Python lambda functions allow us to do exactly that.

```python
# def double(n):
#     return n * 2

double = lambda n: n * 2

print(double(10))
```

**Output**

```
20
```

The syntax of lambda function is:

```
lambda arguments: expression
```

Let's create one more lambda function to return the larger among two other numbers.

```python
larger = lambda a, b: a if a > b else b

print(larger(10, 47))
```

**Output**

```
47
```

---

## `lambda` functions as keys to `sort()`

Suppose we have a list like this:

```python
names = ['Alan', 'Gregory', 'Zlatan', 'Jonas', 'Tom', 'Augustine']
```

To sort this list alphabetically, we can use the list's `sort()` method.

```python
names = ['Alan', 'Gregory', 'Zlatan', 'Jonas', 'Tom', 'Augustine']

names.sort()
print(names)
```

**Output**

```
['Alan', 'Augustine', 'Gregory', 'Jonas', 'Tom', 'Zlatan']
```

Instead of this, suppose we want to sort the items of this list based on the length of the name.

We can do this by passing an optional `key` argument to the `sort()` method.

```python
names = ['Alan', 'Gregory', 'Zlatan', 'Jonas', 'Tom', 'Augustine']

names.sort(key=lambda x: len(x))
print(names)
```

**Output**

```
['Tom', 'Alan', 'Jonas', 'Zlatan', 'Gregory', 'Augustine']
```

> **Note:** Lambda functions are used more frequently with Python builtin functions like map(), filter() and reduce.
