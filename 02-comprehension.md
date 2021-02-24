# Python List, Set and Dictionary Comprehension

Video Link: [https://youtu.be/TGaKzl6p4nA](https://youtu.be/TGaKzl6p4nA)

In this video, we learned to use list, set, and dictionary comprehension in Python.

**Programs in the Video**

- [List Comprehension](#list-comprehension)
- [Conditionals in List Comprehension](#conditionals-in-list-comprehension)
- [Multiple Loops in List Comprehension](#multiple-loops-in-list-comprehension)
- [Set Comprehension](#set-comprehension)
- [Dictionary Comprehension](#dictionary-comprehension)

---

## List Comprehension

Before we learn about list comprehension, let's first understand why it is used.

Suppose we have to create a list of the first five powers of 2. For this, we would normally use a for loop and append every item to the list.

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

Wouldn't it be neat if we could do this same task in a single line?

List comprehension allows us to do exactly that.

```python
# numbers = []

# for i in range(1, 6):
#     numbers.append(2**i)

numbers = [2**i for i in range(1, 6)]

print(numbers)
```

**Output**
```
[2, 4, 8, 16, 32]
```

This comprehension says, "Create a `numbers` list with elements in the form `2**i` where `i` takes values from `1` to `5`."

---

## Conditionals in List Comprehension

List comprehensions can also have an optional `if` conditional along with a `for` loop.

```python
import math
numbers = [49, 64, 81, 100, 121]

new_list = [math.sqrt(n) for n in numbers]
```

**Output**
```
[7.0, 8.0, 9.0, 10.0, 11.0]
```

To get square roots of only the even numbers in the `numbers` list:

```python
import math
numbers = [49, 64, 81, 100, 121] 

new_list = [math.sqrt(n) for n in numbers if n % 2 == 0]
print(new_list)
```

**Output**
```
[8.0, 10.0]
```

---

## Multiple Loops in List Comprehension

We can have more than one for loop in list comprehension:

```python
team1 = ['Janet', 'Arya', 'Mary']
team2 = ['Evan', 'Jake', 'Randy']

new_list = [(x,y) for x in team1 for y in team2]
print(new_list)
```

**Output**

```
[('Janet', 'Evan'), ('Janet', 'Jake'), ('Janet', 'Randy'), ('Arya', 'Evan'), ('Arya', 'Jake'), ('Arya', 'Randy'), ('Mary', 'Evan'), ('Mary', 'Jake'), ('Mary', 'Randy')]
```

We can also write nested list comprehensions.
It means that we can use a list comprehension inside another list comprehension.

>**Note**: We generally write list comprehensions to simplify our code and make it easier to read,
>so you should avoid using list comprehensions inplace of complex and long nested for loops.

---

## Set Comprehension

We can also use set comprehensions in Python to create sets quickly and concisely.

Its syntax is similar to that of list comprehension but we use `{}` instead of `[]`.

```python
word = "programming"
alphabets = {x for x in word}

print(alphabets)
```

**Output**
```
{'o', 'r', 'm', 'a', 'i', 'g', 'p', 'n'}
```

---

## Dictionary Comprehension
Similar to list and set comprehension, dictionary comprehension is an elegant and concise way to create dictionaries in Python.

```python
numbers = [1, 2, 3, 4, 5]

# square_dict = dict()
# for num in numbers:
#     square_dict[num] = num**2
# print(square_dict)

square_dict = {num:num**2 for num in numbers}
print(square_dict)
```

**Output**
```
{1: 1, 2: 4, 3: 9, 4: 16, 5: 25}
```

Lets try one more example:

Suppose we have a dictionary that looks like this:

```python
old_price = {'milk': 1.02, 'coffee': 2.5, 'bread': 2.5}
```

We need to construct a new dictionary with new prices by increasing the price of items by 50% for those that are more than $2.

```python
old_price = {'milk': 1.02, 'coffee': 2.3, 'bread': 2.5}

new_price = {key: value*1.5 if value>2 else value for (key, value) in old_price.items()}
print(new_price)
```

**Output**
```
{'milk': 1.02, 'coffee': 3.4499999999999997, 'bread': 3.75}
```

The above code is equivalent to:

```python
old_price = {'milk': 1.02, 'coffee': 2.3, 'bread': 2.5}

new_price = dict()
for key, value in old_price.items():
    if value > 2:
        new_price[key] = value * 1.5
    else:
        new_price[key] = value

print(new_price)
```