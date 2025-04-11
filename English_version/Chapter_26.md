### 🗳️ Chapter 26: Unpacking Values — With Grace 🗃️

*from **Adventure in Python** by Sergey Samoylov*

---

The Companion pointed at a new door that had no handle — just five sockets in a row.  
The message blinked above it:

> “I only open when values are placed properly.”  

No magic, no riddle, just Python.

Inside the terminal, the hero saw a clue:

```python
coordinates = (10, 20, 30)
x, y, z = coordinates
```

And just like that, the door clicked.

---

### 🧰 Topic: Value Unpacking in Python

Python allows you to unpack a collection (like a tuple or list)  
into separate variables. This makes code cleaner and often more readable.

```python
dimensions = (1920, 1080)
width, height = dimensions
print(f"Width: {width}")
print(f"Height: {height}")
```

Unpacking works with any iterable, as long as the number of  
elements on the right matches the variables on the left.

If you don’t want all values, use underscore `_` as a throwaway:

```python
_, _, important = (0, 0, 42)
print(f"Only one matters: {important}")
```

You can even unpack nested structures, or use the `*` operator  
for flexible assignment:

```python
first, *middle, last = [1, 2, 3, 4, 5]
print(f"Middle part: {middle}")
```

This makes unpacking powerful for pattern recognition in data.

---

### 🧪 Task: Face the Portal

You're given this tuple:

```python
portal_code = (101, 202, 303, 404, 505)
```

Unpack the first and last digits into two variables —  
`first_digit` and `last_digit`. Ignore the rest.

Then print this phrase:

```
The portal reacts to 101 and 505!
```

---

[Chapter 27](Chapter_27.md)
