### 🌀 Chapter 50: Into the Spiral — Recursion
*from **Adventure in Python** by Sergey Samoylov*

---

He entered a hallway with mirrored walls — endless reflections of himself reaching into darkness.  
Each step forward echoed backward. Every problem he solved… revealed a smaller version of itself.

He touched the wall. The reflection spoke:

> "To escape the loop, you must understand the spiral."

---

### 🧠 The Concept

**Recursion** is when a function calls itself.  
But not blindly — it does so with a clear *exit strategy*.

It’s like breaking a problem down into simpler, smaller versions  
of itself — until the smallest version is so simple, it just returns a value.

---

### 🧪 Example: The Countdown

```python
def countdown(number: int) -> None:
    """Prints a countdown from number to 0."""
    if number <= 0:
        print("Boom!")
    else:
        print(number)
        countdown(number - 1)
```

Try this:

```python
countdown(5)
```

It prints:

```
5
4
3
2
1
Boom!
```

Each time, it reduces the problem size — until the base case (`number <= 0`) ends the chain.

---

### 🧩 A Recursive Puzzle: Factorial

```python
def factorial(number: int) -> int:
    """Calculates factorial using recursion."""
    if number == 0:
        return 1
    return number * factorial(number - 1)
```

Factorial is defined as:

```text
5! = 5 × 4 × 3 × 2 × 1 = 120
```

So:

```python
print(factorial(5))  # Output: 120
```

Each call depends on the result of the smaller one.

---

### ⚠️ Watch Out!

Recursion can go *too deep* if you forget the exit condition.

```python
def infinite_loop():
    infinite_loop()
```

This will eventually raise:

```text
RecursionError: maximum recursion depth exceeded
```

Always include a **base case** — the point where the function *stops* calling itself.

---

### 🛠 Task for the Brave

Write a recursive function called `reverse_string(text: str) -> str`  
that returns the reversed version of the input string.

📌 For example:

```python
reverse_string("hero")  # should return "oreh"
```

---

### 💬 Reflection

The hallway was gone.  
But he had learned to think like a spiral — each problem folding inward until it resolved itself.

> "In recursion, as in life," he whispered,  
> "sometimes you solve the whole by mastering the part."

---
[Chapter 51](Chapter_51.md)
