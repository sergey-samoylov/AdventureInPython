🧠 **Chapter 45: The Function Inside the Function – Closures**

*from *Adventure in Python* by Sergey Samoylov*

---

The digital sky shimmered in shades of copper and cobalt.  
Our hero, walking the lines of recursive trees and logic gates,  
noticed something odd — a function, floating freely, but somehow  
still holding on to a piece of memory.  
Not global memory. Not local memory.  
**Something... in between.**

He approached.

Inside this floating code structure, a value whispered from the past.  
It remembered something. Something enclosed.

> “This,” said the Companion, “is called a *closure*.”

### 🔍 What Is a Closure?

A **closure** is a function defined inside another function  
that remembers the variables from the outer function  
even after that outer function has finished executing.

Let’s look at this in code:

```python
def make_multiplier(factor: int) -> Callable[[int], int]:
    """Returns a function that multiplies by the given factor."""
    def multiplier(number: int) -> int:
        return number * factor
    return multiplier
```

Now use it:

```python
times_three = make_multiplier(3)
print(times_three(10))  # 30
```

Even though `make_multiplier` is finished, `factor` is remembered.

---

### 🧪 Another Example: A Logger Factory

```python
def logger(prefix: str) -> Callable[[str], None]:
    """Creates a logging function with a given prefix."""
    def log(message: str) -> None:
        print(f"{prefix}: {message}")
    return log
```

And now:

```python
error_log = logger("ERROR")
error_log("Something went wrong.")  # ERROR: Something went wrong.
```

---

### 💡 How It Works

Closures *capture* variables from the surrounding context.  
They are especially useful when:

- Creating **factories** of functions.
- Maintaining **state** across multiple calls.
- Avoiding **global variables**.

A closure behaves like it has private memory.

---

### 🧩 Your Challenge

Create a `counter()` function that returns an inner function.  
Each time you call the inner function, it should increment and  
return the count.

Expected behavior:

```python
count = counter()
print(count())  # 1
print(count())  # 2
print(count())  # 3
```

Avoid using `global`! Closures only. 😎

---

The hero, now armed with this strange memory-bearing power,  
felt stronger. He could craft behavior that lived beyond time,  
functions that outlasted the scope of their creation.

> “With closures,” whispered the Companion, “you don’t just code.  
> You *enchant* behavior.”

---

[Chapter 46](Chapter_46.md)
