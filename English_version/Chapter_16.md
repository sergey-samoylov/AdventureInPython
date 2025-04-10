## 🧩 Chapter 16: Taming the Data 🧠  
*from Adventure in Python by Sergey Samoylov*

---

The hall of keys returned —  
but it had grown.  

Now it wasn't just a place to store things.  
It was a system.  
A living memory.

> "You now need more than access,"  
> the Machine whispered,  
> "you need *control*."

---

### 📚 Structured Thinking with Dictionaries

Dictionaries are not just containers.  
They’re **data maps** — perfect for building structure.

```python
def create_profile() -> dict[str, str]:
    """
    Returns a basic user profile stored in a dictionary.
    """
    return {
        "username": "wanderer",
        "status": "active",
        "location": "Sector-7"
    }
```

---

### 🚧 Handling Missing Keys

The hero once tried:

```python
print(profile["rank"])  # ⚠️ KeyError
```

That mistake nearly crashed the system.

Now, he knew better.

```python
def safe_access(data: dict[str, str], key: str) -> str:
    """
    Returns value if key exists, else returns 'Unknown'.
    """
    return data.get(key, "Unknown")
```

`.get()` is **safe** — it never breaks the code.

---

### 🧙‍♂️ The Power of Defaults

```python
def ensure_status(profile: dict[str, str]) -> str:
    """
    Returns the status, creating it if missing.
    """
    return profile.setdefault("status", "pending")
```

`.setdefault()` will **return the value if it exists**,  
or **set and return a default if it doesn’t**.

This is **one line** of logic that handles both cases.

---

### 🔁 Looping Through Complex Data

```python
def print_report(users: dict[str, dict[str, str]]) -> None:
    """
    Prints data from nested dictionaries.
    """
    for username, info in users.items():
        status: str = info.get("status", "unknown")
        location: str = info.get("location", "offline")
        print(f"{username} → {status} @ {location}")
```

This loop handles a full system of profiles.  
It’s robust — no matter if keys are missing.

---

### 💬 Real-Life Use Case: Settings

```python
def load_settings() -> dict[str, str]:
    """
    Returns basic settings from a configuration.
    """
    return {
        "theme": "dark",
        "font": "monospace"
    }
```

Later:

```python
def get_setting(
    settings: dict[str, str], key: str
) -> str:
    """
    Returns a setting or a fallback default.
    """
    return settings.get(key, "default")
```

---

### 🧠 Challenge: System Scanner

Build a program that:

- Stores at least 3 user profiles in a dictionary  
- Each profile is a nested dictionary  
- Loops through them, prints name and status  
- If "status" is missing, show "offline"

Can you use `.get()` or `.setdefault()` wisely?

---

### 📚 Concepts in This Chapter

- Safe access with `.get()`  
- Setting defaults with `.setdefault()`  
- Looping through nested dictionaries  
- Real-world data shapes and strategies  
- Avoiding common `KeyErrors` in code

---

### 🧠 Reflection

The Machine no longer feared disorder —  
because the hero had learned **graceful failure**,  
**safe defaults**, and **the art of structured chaos**.

*"To tame data,"* it whispered,  
*"you must expect the unexpected."*

---

Shall we move on to [Chapter 17](Chapter_17.md)?
