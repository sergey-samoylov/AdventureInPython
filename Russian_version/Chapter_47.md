## 🧠 Глава 47: Эволюция замыканий
*from **Adventure in Python** by Sergey Samoylov*

---

Чем дальше путешествовал наш Герой, тем яснее становились закономерности в мире кода.  
Однажды утром, стоя на вершине холма из обломков скриптов и незавершённых модулей,  
он заметил нечто знакомое: замыкания.

— "Но я уже это видел", — удивился он.

Терминал зашипел:

**"Да. Но теперь ты их *понимаешь* и сможешь лучше использовать."**

---

### 🔁 Напоминание: что такое замыкание?

Замыкание — это функция, которая "помнит" переменные из своей внешней области видимости,  
даже если эта область уже завершена.

Краткое напоминание:

```python
def make_multiplier(factor: int):
    """Возвращает функцию, умножающую число на factor."""
    def multiplier(value: int) -> int:
        return value * factor
    return multiplier

double = make_multiplier(2)
print(double(5))  # 10
```

Функция `multiplier` сохраняет доступ к переменной `factor`, даже после завершения `make_multiplier`.

---

### 🧰 Практика 1: логгер с меткой

```python
def make_logger(tag: str):
    """Создаёт логгер с заданной меткой."""
    def log(message: str) -> None:
        print(f"[{tag}] {message}")
    return log

error_logger = make_logger("ERROR")
info_logger = make_logger("INFO")

error_logger("Что-то пошло не так")
info_logger("Система работает нормально")
```

💡 **Зачем это нужно**: так можно создавать специализированные функции с запомненным внутренним состоянием.

---

### 🧰 Практика 2: ограничение количества вызовов

```python
def limit_calls(max_calls: int):
    """Ограничивает количество вызовов функции."""
    call_count = 0

    def wrapper(func):
        def limited() -> None:
            nonlocal call_count
            if call_count < max_calls:
                call_count += 1
                func()
            else:
                print("Достигнут лимит вызовов.")
        return limited

    return wrapper

def greet() -> None:
    print("Привет!")

limited_greet = limit_calls(2)(greet)
limited_greet()
limited_greet()
limited_greet()  # Лимит достигнут
```

🎯 **Что это даёт**:  
мы отслеживаем состояние (`call_count`) без глобальных переменных — благодаря замыканию.

---

### ✍️ Задание для тебя

Напиши функцию `make_power_raiser(base: int)`,  
которая возвращает другую функцию.  
Эта вторая функция должна возводить число в переданную степень.

```python
square = make_power_raiser(2)
print(square(5))  # 25
```

➡️ Реализуй это решение с использованием замыкания!

---

[Глава 48](Chapter_48.md)
