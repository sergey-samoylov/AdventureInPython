## 🔧 Chapter 14: Functions Return 🔁  
*from Adventure in Python by Sergey Samoylov*

---

He remembered.

He remembered the time he had built functions —  
simple tools, quiet servants.

But now, the world had changed.  
It asked more than *commands*.  
It expected **answers**.

And so the hero learned:  
**functions can return values**.

---

### 🎁 The Gift of Return

Before, functions just **did something**.  
Now, they could **give something back**.

```python
def scan_area() -> str:
    """
    Simulates a scan and returns the result.
    """
    return "No threats detected."
```

Now he could **capture** the result:

```python
scan_result: str = scan_area()
print(scan_result)
```

He didn’t just **command** anymore.  
He could **receive**.

---

### 🧮 Return with Data

```python
def add_power(base: int, bonus: int) -> int:
    """
    Returns total power after adding bonus.
    """
    return base + bonus

new_power: int = add_power(10, 5)
print(f"Updated power: {new_power}")
```

This was no longer just storytelling —  
it was *calculation*, *logic*, *structure*.

The hero could now pass data in —  
and pull meaning out.

---

### 🔀 Branching with Return

```python
def access_granted(code: str) -> bool:
    """
    Checks if access code is correct.
    """
    return code == "delta-73"

if access_granted("delta-73"):
    print("Welcome back.")
else:
    print("Access denied.")
```

Functions had become like **sensors**.  
They detected, judged, responded.

---

### 🛠️ Practice: Build a Scanner

Write a function:

- It takes a `location: str`
- If the location is `"vault"` → return `"High security"`
- Else → return `"Clear"`

Then call the function and print the result.

---

### 🎯 Challenge: Data Flow Simulation

Create two functions:

1. `gather_info() -> str`: returns fake system info  
2. `analyze_info(info: str) -> str`: returns a result  
   like `"Threat detected"` or `"Safe"`

Chain them together:

```python
info = gather_info()
result = analyze_info(info)
print(result)
```

Try adding randomness for different outcomes.

---

### 📚 Concepts in This Chapter

- `return` keyword to pass data out of a function
- Using returned values in other code
- Returning different types (`str`, `int`, `bool`)
- Function chaining (output → input)

---

### 🧠 Reflection

*"To speak is to act,"* the voice whispered,  
*"But to return is to decide."*

With returning functions,  
his code could now evaluate, judge, and advise.

The hero had become not just a builder —  
but a **thinker** in code.

---

Continue learnig! [Chater 15](Chapter_15.md) awaits!
