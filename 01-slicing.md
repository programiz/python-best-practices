# Python Slicing of Lists and Strings

Video Link: [https://youtu.be/A5N_-kMbv1o](https://youtu.be/A5N_-kMbv1o)

In this video, we learned about slicing of lists and strings that allows us to build new lists from an existing list or string.

**Programs in the Video**

- [List Indexing](#list-indexing)
- [Slicing of a List](#slicing-of-a-list)
- [Using step in Slicing](#using-step-in-slicing)
- [Reversing a List Using slicing](#reversing-a-list-using-slicing)
- [Changing Multiple List Items](#changing-multiple-list-items)

---

## List Indexing

A list is a sequence of items in an order.

To access an individual item from a list, we use index that starts from `0`.

```python
numbers = [5, 10, 15, 20, 25]

print(numbers[0])

print(numbers[3])
```

**Output**
```
5
20
```

Python also supports negative indexing for lists. Using a negative index gives us items from the last.

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

## Slicing of a List

Slicing allows us to create a new list from an existing list.

```python
numbers = [5, 10, 15, 20, 25]

new_numbers = numbers[0:3]
print(new_numbers)
```

**Output**
```
[5, 10, 15]
```

This creates a new list from start upto but not including the fourth item (Item with index of `3`).

As you can see, the start index is inclusive and the end index is exclusive.

We can also use negative indexes in slicing notation.

```python
numbers = [5, 10, 15, 20, 25]

new_numbers = numbers[0:3]
print(new_numbers)

new_numbers = numbers[2:4]
print(new_numbers)

new_numbers = numbers[-4: -1]
print(new_numbers)
```

**Output**
```
[5, 10, 15]
[15, 20]
[10, 15, 20]
```

In a slice notation, we can skip the start and end index.

- If we skip the start index, then slicing starts from `0`(the first element). 
- If we skip the last index, the slicing ends at the last element. 


```python
numbers = [5, 10, 15, 20, 25]

new_numbers = numbers[:3]
print(new_numbers)

new_numbers = numbers[2:]
print(new_numbers)
```

**Output**
```
[5, 10, 15]
[15, 20, 25]
```

---

## Using step in Slicing

The complete slicing notation syntax is:

```
list[start, end, step]
```

```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8]

print(numbers[1: 6: 2])

print(numbers[1: 6: 3])
```

**Output**

```
[2, 4, 6]
[2, 5]
```

---

## Reversing a List Using slicing

There is a cool way to reverse a list using the slicing notation.

Since we want to reverse a list, lets go through the list from start to end by using empty start and end index.

```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8]
print(numbers[:])
```

Then, let's use `-1` as step which creates a list starting from the last item up to the first item in a backward direction.

```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8]
print(numbers[::-1])
```

**Output**
```
[8, 7, 6, 5, 4, 3, 2, 1]
```

---

## Changing Multiple List Items
We can also use the slicing notation to change multiple items of a list at once.

```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8]

numbers[:3] = [-1, -2, -3]
print(numbers)
```

**Output**
```
[-1, -2, -3, 4, 5, 6, 7, 8]
```

The first three items have been replaced.

---

The slicing also works in a similar way for other compound data types that use indexes such as strings and tuples.
