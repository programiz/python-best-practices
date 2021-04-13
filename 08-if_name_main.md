# Python if __name__ == "__main__"

Video Link: [https://youtu.be/rFPakswX8XA](https://youtu.be/rFPakswX8XA)

In this video, we learned about the special `__name__` attribute of a Python file that can be used to run the file
dynamically in different contexts.

**Programs in the Video**

- [What is `__name__` in Python?](#what-is-__name__-in-python)
- [Running a Python File as a Script](#running-a-python-file-as-a-script)
- [Running a Python File as a Module](#running-a-python-file-as-a-module)
- [Using if conditional with `__name__`](#using-if-conditional-with-__name__)

---

## What is `__name__` in Python?

The `__name__` variable is a special pre-defined variable that represents the name of a Python file.

It has different values depending on how we execute the Python file.

---

## Running a Python File as a Script

When we run the file normally as a script, the value of the `__name__` variable is equal to `__main__`.

Let me create a file named **first.py**.

```python
print(__name__)
```

Let's run this file from the terminal as a script.

```shell
python first.py
```

**Output**

```
__main__
```

> **Note**: When we run a Python file as a script, the value of the `__name__` variable for that file is always `__main__`.

---

## Running a Python File as a Module

When we run a Python file by importing it as a module inside another file, the value of the dunder name variable is
equal to the actual name of the Python file.

Let's create another file named **second.py** in the same directory:

```python
import first
```

Let's run this code:

```shell
python second.py
```

**Output**

```
first
```

> **Note**: In the context of running a Python file as a module, the name of the module itself is assigned to `__name__`.
---

## Using if conditional with `__name__`

Suppose we have a file called **helloworld.py** with the following contents:

```python
def greet():
    print("Hello, World!")
```

Suppose we want to run the `greet()` function directly while running **helloworld.py** as a script, that is when running
it from the terminal.

For this, we can use the `if` statement, and the `__name__` variable.

```python
def greet():
    print("Hello, World!")

if __name__ == "__main__":
    greet()
```

Let's run this file:

```shell
python helloworld.py
```

**Output**
```
Hello, World!
```

Now, let's create a new file called **greetings.py**

```python
import helloworld
```

Let's run **greetings.py** file:

```shell
python greetings.py
```

This time nothing gets printed. It means that the `greet()` function was not executed directly.

In this case, only the contents outside the `if` of **helloworld.py** gets executed and imported.

However, we can still call it manually:

```python
import helloworld

helloworld.greet()
```

**Output**

```
Hello, World!
```

This is a very useful feature as it allows you to run the same file differently in different scenarios.

You are sure to encounter if `__name__ == "__main__":` a lot while coding in Python.

