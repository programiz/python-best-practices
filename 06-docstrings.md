# Python docstrings

Video Link: [https://youtu.be/0YUdYk5E-w4](https://youtu.be/0YUdYk5E-w4)

Python docstrings provide a convenient way of associating documentation with Python modules, functions, classes, and
methods.

In this video, we learned to create docstrings and understood how and why they are used.

**Programs in the Video**

- [Python Multiline comments](#python-multiline-comments)
- [Python docstrings](#docstrings-in-python)
- [How to write good docstrings?](#how-to-write-good-docstrings)

---

## Python Multiline comments

We use either triple single quotes `'''` or triple double quotes `"""` to create multiline comments.

```python
"""Takes two parameters. 
    Returns sum.
"""


def add_numbers(a, b):
    return a + b


print(add_numbers(5, 10))
```

**Output**

```
15
```

Here, these lines:

```python
"""Takes two parameters. 
    Returns sum.
"""
```

are multiline comments as they are inside triple quotation marks. These lines are ignored by the Python interpreter.

Now we are ready to learn about docstrings.

---

## Docstrings in Python

Let's modify our previous program:

```python
def add_numbers(a, b):
    """ Takes two parameters.  
        Returns sum.
    """
    return a + b


print(add_numbers(5, 10))

```

Now, the comment code inside the function is a docstring. For a multiline comment to be a docstring, it must be the
first line of a function, classes, modules and so on.

> **Note**: If your code editor supports it, you can see docstrings by hovering over modules and functions.

We can also print the docstring from our program using the `__doc__` attribute:

```python
def add_numbers(a, b):
    """ Takes two parameters.  
        Returns sum.
    """
    return a + b


print(add_numbers(5, 10))
print(add_numbers.__doc__)

```

**Output**

```
15
 Takes two parameters.  
        Returns sum.
```

>**Note**: If the docstring is not defined, `__doc__` is `None`.

You can use the doc attribute to also print the docstring on in-built functions, modules and so on:

```python
import math

print(math.__doc__)
print(math.sqrt.__doc__)

```

**Output**

```
This module provides access to the mathematical functions
defined by the C standard.
Return the square root of x.
```

---

## How to write good docstrings?

Writing docstring is pretty easy, however, there are a few things we should keep in mind while creating docstrings.

- A docstring must be the first statement in a module, function or class. Otherwise, it's not considered a docstring.
- We cannot use regular comments that start with a hash to create a docstring.
- Docstring must not be descriptive, rather they must follow, "Do this, return that" structure.