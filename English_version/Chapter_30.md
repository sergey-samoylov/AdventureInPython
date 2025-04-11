### ✂️ Chapter 30: Filter What Matters 🪪  
*from *Adventure in Python* by Sergey Samoylov*

---

The hero now walked through a strange canyon.  
Its walls echoed unspoken thoughts.  
Some were loud, others faint.  
Some were true, others fake.

> “Not everything that enters your mind belongs there,”  
> said the Companion.

> “You must learn to filter out the noise.”

---

### 🧰 Topic: The `filter()` function

While `map()` **transforms** every item,  
`filter()` **selects** only those that match a condition.

---

### 🔧 Syntax:

```python
filter(function, iterable)
```

It returns an **iterator** with only truthy elements.

You usually wrap it in `list()`.

---

### 🔬 Example:

```python
def is_even(x: int) -> bool:
    return x % 2 == 0

numbers: list[int] = [1, 2, 3, 4, 5, 6]
even: list[int] = list(filter(is_even, numbers))

print(even)
```

✅ Output:
```python
[2, 4, 6]
```

---

### ⚡ With `lambda`:

```python
words: list[str] = ["", "apple", "", "banana"]
non_empty: list[str] = list(filter(lambda w: w, words))

print(non_empty)
```

✅ Output:
```python
['apple', 'banana']
```

---

### 🧪 Task: Filter Short Words

Given:

```python
words = ["a", "hi", "code", "python", "to"]
```

Filter out all words that are **less than 3 letters long**.

Expected result:

```python
["code", "python"]
```

---
[Chapter 31](Chapter_31.md)
