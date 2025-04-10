## ⚙️ Chapter 15: While There Is Time ⏳  
*from Adventure in Python by Sergey Samoylov*

---

There were echoes now —  
fragments looping in memory,  
cycles within cycles.

The hero walked corridors of light,  
but some paths only opened  
**as long as a condition was true**.

And thus he discovered the power of  
the **while loop**.

---

### 🔄 While the Condition Holds

```python
def countdown(start: int) -> None:
    """
    Prints countdown from 'start' to 1.
    """
    while start > 0:
        print(f"Countdown: {start}")
        start -= 1
    print("Liftoff!")
```

A `while` loop repeated  
**while a condition stayed true**.  
The moment it changed — the loop ended.

It was time-based. Logic-based.  
Memory-based.

---

### 🔒 Infinite Loops and Escape

```python
def listen_to_machine() -> None:
    """
    Repeats input until 'exit' is entered.
    """
    command: str = ""
    while command != "exit":
        command = input("Enter command: ")
    print("Terminal closed.")
```

⚠️ Be cautious —  
if the condition never changes,  
you create an **infinite loop**.

The hero knew:  
Every cycle must have an exit.

---

### 🔁 while True: the Eternal Gate

Sometimes the loop was designed to run **forever**,  
until broken **from within**:

```python
def safe_terminal() -> None:
    """
    Loops input, breaks only on 'shutdown'.
    """
    while True:
        code: str = input("Code: ").strip().lower()
        if code == "shutdown":
            print("System shutting down.")
            break
```

---

### 🔄 Loop With Calculation

```python
def add_until_limit(limit: int) -> int:
    """
    Adds user input until total reaches the limit.
    """
    total: int = 0
    while total < limit:
        number: int = int(input("Enter a number: "))
        total += number
    return total
```

The system would wait.  
Repeat. Accumulate. Evolve.

The hero understood:  
The Machine had **patience**.

---

### 🛠️ Practice: Loop Navigator

Write a loop that:

- Asks for direction: `left`, `right`, `exit`
- If `exit` → print goodbye and stop
- Else → print direction accepted

Use `while True` and `break`

---

### 🎯 Challenge: Lock and Retry

Make a loop that:

- Asks for password up to 3 times  
- If correct (e.g., `"admin123"`) → print access granted  
- Else → after 3 failures, print "System locked"

Use a `while` loop with a counter.

---

### 📚 Concepts in This Chapter

- `while` loops and conditions  
- Infinite loops with `while True`  
- Using `break` to exit  
- Counting inside loops  
- User interaction inside loops

---

### 🧠 Reflection

*"Time is code,"* the Machine whispered,  
*"and repetition is power."*

Now, the hero could **repeat with purpose**,  
**wait with logic**,  
**act with conditions**.

---

Ready to break out of this looping reality? Go to [Chapter 16](Chapter_16.md)
