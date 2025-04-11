## 🧰 Chapter 23: The Toolbox Expands 🔧  
*from Adventure in Python by Sergey Samoylov*

---

The Companion was humming, lights dancing in patterns.  
The Terminal projected something new:

> "Your tools grow.  
> You now wield the power of built-in functions."

The hero blinked. A row of strange symbols lit up:

`len()`, `sum()`, `max()`, `min()`, `sorted()`, `reversed()`

---

### 🛠 What Are Built-in Functions?

Python comes with a powerful **standard library**  
and many built-in functions ready to use  
— no import needed.

They work on strings, lists, numbers, and more.

---

### 📏 `len()`: Know the Size

```python
name: str = "Python"
print(len(name))  # 6
```

Works with strings, lists, tuples, etc.

---

### ➕ `sum()`: Add It Up

```python
numbers: list[int] = [1, 2, 3]
print(sum(numbers))  # 6
```

Adds all elements of a list.

---

### 🥇 `max()` and `min()`: Find the Extremes

```python
scores: list[int] = [7, 4, 9, 2]
print(max(scores))  # 9
print(min(scores))  # 2
```

---

### 📚 `sorted()`: Return a Sorted Copy

```python
words: list[str] = ["banana", "apple", "cherry"]
print(sorted(words))  # ['apple', 'banana', 'cherry']
```

The original list stays unchanged.

---

### 🔁 `reversed()`: Go Backwards

```python
letters: str = "abc"
for letter in reversed(letters):
    print(letter)
```

---

The Companion explained:

> "These functions don’t belong to any module.  
> They are *built in* —  
> like your instincts."

---

### 🧠 Challenge: A Handy Toolbox

Write a program that:

1. Asks the user to enter 5 numbers  
2. Stores them in a list  
3. Prints:
   - The sum
   - The smallest and largest numbers
   - The list in reverse

Use only built-in functions.

---

The hero smiled.

> “Every new tool makes me faster.  
> And wiser.”

The Terminal agreed.

> “And closer to freedom.”

---

Jump to [Chapter 24](Chapter_24.md) now!
