## 🔄 Chapter 48: Decorators Revisited — The Elegant Patterns
*from **Adventure in Python** by Sergey Samoylov*

---

The Hero thought he already understood decorators.  
But now, deeper in the system, he saw something strange:  
decorators stacked like armor, layered upon one another,  
each one transforming, protecting, enhancing.

> "Decorators are not just tools," whispered the Companion.  
> "They're *patterns of expression.*"

---

### 🧱 Refresher: What is a Decorator?

A decorator is a function that takes another function  
and returns a new one — usually adding behavior before or after.

You've seen this:

```python
def simple_decorator(func):
    def wrapper():
        print("Before function")
        func()
        print("After function")
    return wrapper

@simple_decorator
def say_hi():
    print("Hi!")

say_hi()
```

---

### 🧙‍♂️ Stacking Decorators

They can be layered — each decorator wrapping the next:

```python
def bold(func):
    def wrapper():
        print("<b>", end="")
        func()
        print("</b>", end="")
    return wrapper

def italic(func):
    def wrapper():
        print("<i>", end="")
        func()
        print("</i>", end="")
    return wrapper

@bold
@italic
def say_hello():
    print("Hello", end="")

say_hello()
# Output: <b><i>Hello</i></b>
```

Decorators apply *from bottom up* — `italic` first, then `bold`.

---

### 🔐 Decorating Functions with Arguments

To support decorated functions that accept parameters,  
your decorator’s inner function must accept `*args` and `**kwargs`.

```python
def debug(func):
    def wrapper(*args, **kwargs):
        print(f"Calling {func.__name__}")
        return func(*args, **kwargs)
    return wrapper

@debug
def multiply(x: int, y: int) -> int:
    return x * y

print(multiply(3, 4))
```

---

### 🧪 Task: Timing a Function

Write a decorator called `timed` that prints how long  
the decorated function takes to run.

```python
@timed
def slow_function():
    for _ in range(1000000):
        pass
```

🧠 Hint: Use `time.time()` before and after the call.

---

Decorators aren't just a trick — they're part of how Python itself works.  
They allow for clean, reusable transformations.

And now, the Hero begins to see them not as tools —  
but as elegant expressions of power.

Ready for more?

[Chapter 49](Chapter_49.md)
