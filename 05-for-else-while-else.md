# Python `for...else` and `while...else`

Video Link: [https://youtu.be/aoW_Y1MumN0](https://youtu.be/aoW_Y1MumN0)

In this video, we learned to use the `else` clause in `for` and `while` loops with the help of examples.

**Programs in the Video**

- [Python `for...else`](#python-forelse)
- [Python `while...else`](#python-whileelse)

---

## Python `for...else`

Suppose we want to check if an element is present in a given list.

For that, let's iterate through each element and check if it is equal to our value:

```python
languages = ['Python', 'JavaScript', 'C', 'C++', 'Java']

for language in languages:
    if language == "Java":
        print("Item found")
```

**Output**

```
Item found
```

Now, suppose we want to print `Item not found` if the item was not found in the list.

One way to do so is to use a flag and check it after the loop ends:

```python
languages = ['Python', 'JavaScript', 'C', 'C++', 'Java']

flag = False

for language in languages:
    if language == "Java":
        flag = True

if flag:
    print("Item found")
else:
    print("Item not found")
```

**Output**

```
Item found
```

Let's test using another keyword **"Rust"**:

```python
languages = ['Python', 'JavaScript', 'C', 'C++', 'Java']

flag = False

for language in languages:
    if language == "Rust":
        flag = True

if flag:
    print("Item found")
else:
    print("Item not found")
```

**Output**

```
Item not found
```

We can implement this exact functionality using `for...else`.

```python
languages = ['Python', 'JavaScript', 'C', 'C++', 'Java']

for language in languages:
    if language == "Java":
        print("Item found")
else:
    print("Item not found")
```

**Output**

```
Item found
Item not found
```

* First, we checked if every item was equal to `Java`,and since the last item is equal to `Java`, ***"Item found"*** was
  printed.
* The `else` clause of the `for` loop executes at the end, only if the loop completes normally. In this case the loop
  completed normally and **Item not Found** was printed at the end.

However, we can now use the `break` statement inside `if` to end the loop abruptly if the item was found:

```python
languages = ['Python', 'JavaScript', 'C', 'C++', 'Java']

for language in languages:
    if language == "Java":
        print("Item found")
        break
else:
    print("Item not found")
```

**Output**

```
Item found
```

Changing the keyword to **Rust**:

```python
languages = ['Python', 'JavaScript', 'C', 'C++', 'Java']

for language in languages:
    if language == "Rust":
        print("Item found")
        break
else:
    print("Item not found")
```

**Output**

```
Item not found
```

---

## Python `while...else`

The working of an `else` clause of a `while` loop is very similar to that of a `for` loop.

Let's write a program to check if a number is prime.

```python
num = int(input("Enter a number: "))

i = 2

while i < num:
    if num % i == 0:
        print(num, "is not a prime as it is", num // i, "times", i)
        break
    i += 1
else:
    print(num, "is a prime number")
```

**Output 1**

```
Enter a number: 34
34 is not a prime as it is 17 times 2
```

**Output 2**

```
Enter a number: 29
29 is a prime number
```