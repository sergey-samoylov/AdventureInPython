## 📖 Chapter 3: The Debugger Beast 🦁

*from Adventure in Python by Sergey Samoylov*

---

His code was clean.  
His logic—flawless.  
His mind—calm.

But then, something broke.

The terminal spat red fire:

```
Traceback (most recent call last):
  File "main.py", line 8, in <module>
    greet(user)
NameError: name 'greet' is not defined
```

The system screamed.

Error.  
Traceback.  
Undefined.

And from the red mist of the terminal, it emerged:  
The **Debugger Beast**.

It did not bite directly.  
It lived in typos.  
In missed colons.  
In forgotten indentation.

It lived in *him*.

He must not fight it. He must **tame** it.

---

## 💡 Module 3: Loops, Exceptions & the Beast

---

> 🎯 Goal: Repeat, handle failures, survive bugs.

---

### 🔹 `while` Loop — Persistence in Logic

Loops repeat actions while a condition is `True`.

```python
def countdown(start_value: int) -> None:
    """
    Countdown from a given start_value.
    """
    while start_value > 0:
        print(f"Time left: {start_value}")
        start_value -= 1

    print("Launch complete!")


countdown(3)
```

---

### 🔹 `try / except` — Taming the Beast

When an error might occur, catch it with `try / except`.

```python
def safe_divide(dividend: int, divisor: int) -> float:
    """
    Divide two numbers safely.
    """
    try:
        result: float = dividend / divisor
        return result
    except ZeroDivisionError:
        print("Error: Cannot divide by zero.")
        return 0.0


print(safe_divide(10, 0))
```

---

### 🔹 Access Script: Controlled Entry

```python
def request_access() -> None:
    """
    Ask for a secret code with limited attempts.
    """
    access_code: str = "delta"
    attempts_left: int = 3

    while attempts_left > 0:
        user_code: str = input("Enter access code: ")

        if user_code == access_code:
            print("Access granted.")
            return
        elif user_code.strip() == "":
            print("Code cannot be empty.")
        else:
            attempts_left -= 1
            print(f"Wrong code. {attempts_left} tries left.")

    print("Access locked.")


request_access()
```

---

### 🧠 Your Challenge

- Create a login loop that:
  - Accepts only a specific code.
  - Handles blank input.
  - Exits after 3 failed tries.
  - Uses a function with clean logic.

---

> Errors are not the enemy.  
> **They are messages. Clues. Beasts.**  
> And beasts can be tamed.

---

Ready for [**Chapter 4: Virus and Encapsulation**](Chapter_04.md)?  
We’ll craft your first **class**—a digital entity with memory.
