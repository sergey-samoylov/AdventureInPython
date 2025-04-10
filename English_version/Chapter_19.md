## 🔍 Chapter 19: Errors and Exceptions ⚠️  
*from Adventure in Python by Sergey Samoylov*

---

The Machine paused.  
A quiet blink in the terminal.  
Something had gone wrong.  
But the hero was calm.

He’d seen this before.

---

> "An error? No problem — try/except."

Yes. He *used* exceptions.  
Now it was time to **understand** them.

---

### ⚠️ What *Are* Exceptions?

Exceptions are **signals**.  
They tell the interpreter:  
> "Something went wrong.  
> We can't continue unless this is handled."

They are part of the program’s **control flow** —  
not just accidents.

What's the catch? Why [try/except again](why_try_except.md)?

---

### 🔁 The Difference Between Using and Knowing

The hero had caught exceptions before:  

```python
try:
    value = int(input("Enter a number: "))
except ValueError:
    print("Not a number!")
```

But what **exactly** was `ValueError`?  
What other errors are there?  
Can you catch more than one?  
Can you raise your own?

These are questions of a programmer,  
not just a survivor.

---

### 🧪 Let's Explore an Exception

```python
def divide(a: float, b: float) -> float:
    """
    Returns a divided by b.
    """
    return a / b
```

Used safely:

```python
try:
    result = divide(10, 0)
except ZeroDivisionError:
    print("Division by zero!")
```

Now you know: `ZeroDivisionError`  
is a built-in exception class.

---

### 🧰 Exception Types

Python has many exceptions:

- `ValueError`
- `IndexError`
- `KeyError`
- `TypeError`
- `FileNotFoundError`

You can catch them *individually*  
or use a base class like `Exception`.

---

### 🧼 Be Specific, Not Lazy

Avoid this:

```python
try:
    run_code()
except:
    pass
```

Why is it dangerous?

- You’ll hide bugs.
- You won’t know what failed.
- You can’t fix what you can’t see.

Be precise.

---

### 💬 Raising Your Own Exceptions

You can raise exceptions too:

```python
def check_age(age: int) -> None:
    """
    Raises an error if age is too low.
    """
    if age < 0:
        raise ValueError("Age cannot be negative.")
```

Now you *control the error flow*.

---

### 🧠 Challenge: Input with Limits

Write a function:

```python
def ask_number() -> int:
```

It should:

- Ask the user for a number
- Raise `ValueError` if the number is negative
- Catch and explain what went wrong

Run it several times.  
What happens with "ten"? With `-1`?

---

### 🧠 Reflection

> “I used to avoid errors,”  
> said the hero.  
> “Now I understand them.”

> “Good,” said the Machine.  
> “Because mastery  
> is not about preventing failure —  
> but *growing from it*.”

---

Ready for a jump? [Chapter 20](Chapter_20.md) waits for you!
