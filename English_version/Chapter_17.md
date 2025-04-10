## 🧪 Chapter 17: Testing the System 🧫  
*from Adventure in Python by Sergey Samoylov*

---

The screen blinked.

A script failed.  
Then another.

> "Something’s… wrong,"  
> the hero whispered.

> "Is it the code —  
> or is it… me?"

---

### 🧪 What is Testing?

The Machine was growing.  
So was the hero’s code.

And with that growth came bugs.  
Invisible traps.  
Logic errors.  
Broken assumptions.

To fix them, he needed a weapon.

That weapon was **testing**.

---

### ✅ Manual Testing

The simplest way to test a function?

Just run it:

```python
def double(number: int) -> int:
    """
    Returns the input number multiplied by 2.
    """
    return number * 2

print(double(3))     # → 6
print(double(-1))    # → -2
```

If you get the right answer — great!  
If not — fix it.

But manual testing doesn’t scale.

---

### 🧪 Automated Testing

What if code tested itself?

```python
def test_double() -> None:
    """
    Runs simple tests for the double function.
    """
    assert double(2) == 4
    assert double(0) == 0
    assert double(-3) == -6
```

Each `assert` checks a condition.  
If it fails — Python throws an error.

This is **defensive programming**.  
You don’t trust the code.  
You *verify* it.

---

### 🔄 Running the Tests

```python
if __name__ == "__main__":
    test_double()
    print("All tests passed.")
```

By placing test calls in `__main__`,  
you keep test logic separate from the rest.

If anything breaks — you’ll know.

---

### 🧰 More Complex Example

```python
def is_even(number: int) -> bool:
    """
    Returns True if the number is even.
    """
    return number % 2 == 0


def test_is_even() -> None:
    """
    Tests is_even() with several values.
    """
    assert is_even(4) is True
    assert is_even(7) is False
    assert is_even(0) is True
```

One bug. One wrong expectation.  
And the machine *screams*.

---

### 🧠 Challenge: Write Your Own Test

Create a function called `is_palindrome(text: str) -> bool`  
It should return True if text reads the same backward.

Then, write at least **3 tests** for it  
using `assert`.

Can you make all tests pass?

---

### 📚 What We Learned

- What testing is and why it matters  
- Manual vs automated testing  
- Using `assert` to write simple test cases  
- Keeping tests isolated  
- Testing builds confidence — and saves time

---

### 🧠 Reflection

The Machine sighed — peacefully.

The hero had given it a gift:  
*Stability*.

> "Now," it whispered,  
> "we are harder to break."

---

Ready for the [next chapter](Chapter_18.md)?
