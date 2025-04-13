🧰 **Chapter 46: The Power of Decorators**
*from **Adventure in Python** by Sergey Samoylov*

---

Beyond the valley of closures,  
the Programmer wandered into a strange field  
where functions wrapped other functions —  
changing them, empowering them,  
without touching their core.

> “This is advanced magic,” the Companion said,  
> “used by masters to add behavior without changing code.”

And the word carved in the air was:

**@decorator**

---

### 🎁 What is a Decorator?

A **decorator** is a function that takes another function  
and returns a new one with *enhanced behavior*.

It’s a beautiful example of how Python treats functions as first-class citizens.

---

### ⚙️ Basic Structure

```python

def my_decorator(func):
    def wrapper():
        print("Before the function runs.")
        func()
        print("After the function runs.")
    return wrapper
```

You can now use it like this:

```python
@my_decorator
def say_hello() -> None:
    print("Hello!")

say_hello()
```

Output:
```
Before the function runs.
Hello!
After the function runs.
```

The `@my_decorator` is just a shortcut for:

```python
say_hello = my_decorator(say_hello)
```

---

### 🧙 Why Use Decorators?

Decorators let you:

- Add **logging**, **timing**, or **validation**
- **Modify** inputs or outputs
- Reuse code across many functions without repetition

---

### 🧪 Another Example: Timing Decorator

```python
import time

def timing(func: Callable) -> Callable:
    def wrapper() -> None:
        start = time.time()
        func()
        end = time.time()
        print(f"Execution time: {end - start:.2f}s")
    return wrapper
```

Use it:

```python
@timing
def long_task() -> None:
    time.sleep(1)

long_task()
```

---

### 🧩 Challenge

Write a decorator called `repeat_three_times`  
that runs the decorated function **three times** in a row.

Example:

```python
@repeat_three_times
def laugh() -> None:
    print("Haha!")

laugh()
```

Expected output:
```
Haha!
Haha!
Haha!
```

---

The hero looked at the code — compact, magical,  
and yet readable. He felt like a wizard now.

> “With decorators,” whispered the Companion,  
> “you change behavior with grace.  
> Without ever touching the source.”

---

Ready to wrap your brain around the next spell?

[Chapter 47](Chapter_47.md)
