# ARE BUILT-IN FUNCTIONS ACTUALLY METHODS OF SOME SUPER CLASS?

## For Example type() looks like one.

Let’s break it down:

---

### 🧠 **Built-in Functions vs. Methods of `type()`**

#### ✅ **Built-in Functions** (like `len()`, `sum()`, `max()`):

- These are **global functions** provided by Python.
- They're available without importing anything.
- Technically, they’re defined in the built-in namespace (`__builtins__`).
- They **work by calling internal methods** of objects — often via *special methods*.

For example:

```python
len("hello")  # Actually calls "hello".__len__()
```

So yes, `len()` **delegates to the object's** `__len__()` method — but `len()` itself is not a method of any type — it’s a **function** that *knows how to talk to different types*.

---

#### 📦 **Methods** of objects (like strings, lists, etc.):

These are **bound to the object’s type**, like:

```python
text: str = "hello"
text.upper()  # method of str
```

So, `.upper()` is a method of `str`, while `len(text)` is a function that asks `text` to tell its length via `__len__()`.

---

### 🔍 What About `type()`?

The `type()` function tells you the type of an object:

```python
type("hello")  # <class 'str'>
```

So `type()` is **also a built-in function**, not the container of others.

---

### ✅ Summary:

- `len()`, `sum()`, `max()` etc. are **built-in functions**, not methods.
- They internally call **special methods** like `__len__()`, `__add__()`, etc.
- The object’s `type()` tells which class defines those methods.
- But these functions are **not methods of `type()` itself**.


