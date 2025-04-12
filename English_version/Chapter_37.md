### 📤 Chapter 37: Sending Messages — Arguments and Parameters 📬  
*from **Adventure in Python** by Sergey Samoylov*

---

In a twilight canyon of logic and memory,  
the Hero found a glowing console.

The Companion whispered:

> “You’ve built tools.  
> Now… how will they receive instructions?”

A message flickered into the void:

```python
send_message("Hello, world!")
```

The Hero tilted his head.

> “That’s... a function call.  
> But where does the message go?”

---

### 🧠 Concept: Parameters vs. Arguments

Let’s clear this up:

- **Parameter**: the name inside the function definition  
- **Argument**: the actual value you send when calling it

Think of it like this:

```python
def greet(name: str) -> None:
    """Say hello to someone."""
    print(f"Hello, {name}!")
```

- `name` is the **parameter**  
- `"Ada"` is the **argument** in this call:

```python
greet("Ada")
```

---

### 📦 Why It Matters

Functions become **reusable** and **flexible**  
when they accept different inputs.

```python
greet("Linus")
greet("Grace")
```

One function, many uses.

---

### 🧪 You Can Pass…

✅ Strings  
✅ Numbers  
✅ Lists  
✅ Even other functions!

Example:

```python
def double(x: int) -> int:
    return x * 2

def apply(func, value: int) -> int:
    return func(value)

print(apply(double, 10))  # 20
```

> A function… passed into another function?  
> The Hero’s eyes widened.

---

### 🧠 Default Parameters

You can make parameters optional:

```python
def greet(name: str = "stranger") -> None:
    print(f"Welcome, {name}!")
```

```python
greet()             # Welcome, stranger!
greet("Turing")     # Welcome, Turing!
```

---

### 🔥 Keyword Arguments

You can name arguments explicitly:

```python
def full_name(first: str, last: str) -> str:
    return f"{first} {last}"

print(full_name(last="Curie", first="Marie"))
```

---

### ⚙️ Function with Many Arguments

You can even accept **any number** of arguments:

```python
def sum_all(*numbers: int) -> int:
    return sum(numbers)

print(sum_all(1, 2, 3, 4))  # 10
```

> The asterisk `*` collects all values into a tuple.

---

### ✨ The Hero’s Realization

He was no longer writing one-use tools.  
He was building **interfaces**.

He understood:

> “To command a function is to speak its language.”

---

### 🎯 Challenge: Multi-function Messenger

Write a function:

```python
def repeat_message(
    message: str, times: int = 1
) -> None:
    """Repeat a message multiple times."""
    ...
```

Make it work like:

```python
repeat_message("Rise!", 3)
# Rise!
# Rise!
# Rise!
```

Try it with different inputs.  
Then pass it to another function as an argument.

You’re not just coding—  
you’re **communicating** with machines.

---

Ready for [Chapter 38](Chapter_38.md)?
