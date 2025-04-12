### 📚 Chapter 33: *args and Flexible Functions 🌀  
*from *Adventure in Python* by Sergey Samoylov*

---

The path led deeper into the forest of functions.  
There, the hero saw one function calling many names.

> “Not all functions ask for one thing,”  
> said the Companion.  
> “Some take many, as many as needed.”

---

### 📚 Topic: `*args` — Flexible Arguments

What if you don’t know how many arguments  
will be passed to your function?

Use `*args` to catch them all — as a tuple.

---

### 🔧 Example:

```python
def add_all(*numbers: int) -> int:
    """Returns the sum of all numbers"""
    return sum(numbers)

print(add_all(1, 2, 3))         # 6
print(add_all(10, 20, 30, 40))  # 100
```

The `*` gathers all extra positional arguments  
into one tuple called `numbers`.

---

### 🧪 You Can Still Use Normal Arguments:

```python
def greet_all(greeting: str, *names: str) -> None:
    """Greets each name with a greeting"""
    for name in names:
        print(f"{greeting}, {name}!")
```

Call like this:

```python
greet_all("Hello", "Alice", "Bob", "Cleo")
```

---

### 🧪 Task: Multiply Them All

Write a function `multiply_all()`  
that uses `*args` and returns  
the result of multiplying all the numbers.

```python
multiply_all(2, 3, 4) → 24
multiply_all(5) → 5
multiply_all() → 1
```

Hint: Start with a variable `result = 1`  
and loop through the numbers multiplying them.

---

[Chapter 34](Chapter_34.md)
