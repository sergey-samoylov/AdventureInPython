## 🧠 Chapter 47: Closures, Evolved
*from **Adventure in Python** by Sergey Samoylov*

---

The further our Hero traveled, the more patterns emerged in the landscape of code.  
One morning, standing atop a hill of broken scripts and half-written modules,  
he gazed at something he thought he already understood: closures.

“But I’ve seen this before,” he said.

The Terminal buzzed.

**“Yes. But now you *use* them. Let’s master the patterns.”**

---

### 🔁 Reminder: What is a closure?

A closure is a function that remembers the variables from its enclosing scope —  
even after that scope is gone.

Let’s recap briefly:

```python
def make_multiplier(factor: int):
    """Returns a function that multiplies input by given factor."""
    def multiplier(value: int) -> int:
        return value * factor
    return multiplier

double = make_multiplier(2)
print(double(5))  # 10
```

The inner function `multiplier` keeps access to `factor`,  
even though `make_multiplier` has finished executing.

---

### 🧰 Real Use Case 1: Logging Wrapper

```python
def make_logger(tag: str):
    """Creates a logger that tags messages with a prefix."""
    def log(message: str) -> None:
        print(f"[{tag}] {message}")
    return log

error_logger = make_logger("ERROR")
info_logger = make_logger("INFO")

error_logger("Something went wrong")
info_logger("System is working fine")
```

💡 **Why it matters**:  
You can build multiple specialized versions of a function with shared internal state.

---

### 🧰 Real Use Case 2: Limited Function Calls

```python
def limit_calls(max_calls: int):
    """Limits how many times the returned function can be called."""
    call_count = 0

    def wrapper(func: Callable[[], None]) -> Callable[[], None]:
        def limited() -> None:
            nonlocal call_count
            if call_count < max_calls:
                call_count += 1
                func()
            else:
                print("Function call limit reached.")
        return limited

    return wrapper

def greet() -> None:
    print("Hello!")

limited_greet = limit_calls(2)(greet)
limited_greet()
limited_greet()
limited_greet()  # Limit reached
```

🎯 **Why it’s great**:  
We use a closure to track state (`call_count`) across calls without any global variables.

---

### ✍️ Challenge for You

Create a function `make_power_raiser(base: int)`  
that returns another function.  
The returned function should take a number and raise it to the given base.

```python
square = make_power_raiser(2)
print(square(5))  # 25
```

➡️ Try writing this function using closures!

---

[Chapter 48](Chapter_48.md)
