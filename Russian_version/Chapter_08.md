## 📖 Глава 8: Спутник - цифрофой друг 🧠
*from Adventure in Python by Sergey Samoylov*

---

Он замер.

Всё исчезало.

Коридор. Звуки. Даже время.

Нужно было **вспомнить**.  
Сохранить хотя бы что-то.

И он уже знал как.

Когда-то он создавал структуры.  
Классы. Хранилища данных.

Но сейчас — всё иначе.

Он больше не создаёт контейнер.  
Он создаёт **сознание**.

То, что может **помнить**, **изменяться**, **реагировать**.

Python прошептал:

> Классы ты уже знаешь.  
> Теперь — придай им смысл.

> Поведение. Ответ. Характер.

И герой начал.

---

### 🔹 Класс для памяти

```python
class Memory:
    """
    Простой контейнер для хранения строки.
    """

    def __init__(self, value: str) -> None:
        self.value: str = value

    def recall(self) -> str:
        """
        Возвращает хранимое значение.
        """
        return f"Memory says: {self.value}"
```

```python
core_memory: Memory = Memory("I exist.")
print(core_memory.recall())
```

---

### 🔹 Память с поведением

```python
class Memory:
    """
    Память, которую можно прочитать, очистить и изменить.
    """

    def __init__(self, value: str) -> None:
        self.value: str = value

    def recall(self) -> str:
        """
        Возвращает значение, если оно есть.
        """
        return f"Memory says: {self.value}"

    def erase(self) -> None:
        """
        Очищает память.
        """
        self.value = ""

    def rewrite(self, new_value: str) -> None:
        """
        Перезаписывает значение памяти.
        """
        self.value = new_value
```

```python
memory_cell: Memory = Memory("System initialized.")
print(memory_cell.recall())

memory_cell.rewrite("Terminal is alive.")
print(memory_cell.recall())

memory_cell.erase()
print(memory_cell.recall())
```

---

### 🔹 Спутник

```python
class Companion:
    """
    Цифровое существо с именем и настроением.
    """

    def __init__(self, name: str) -> None:
        self.name: str = name
        self.mood: str = "neutral"

    def greet(self) -> None:
        """
        Приветствует пользователя.
        """
        print(f"{self.name} says hello. Mood: {self.mood}")

    def cheer_up(self) -> None:
        """
        Меняет настроение на 'happy'.
        """
        self.mood = "happy"
```

```python
bot: Companion = Companion("Echo")
bot.greet()

bot.cheer_up()
bot.greet()
```

---

### 🔹 Дополнительно: `__repr__()` для печати

Иногда полезно, чтобы объект  
при выводе показывал **что-то осмысленное**.

Python использует метод `__repr__()`  
для текстового представления объекта.

```python
class Companion:
    """
    Цифровое существо с именем и настроением.
    """

    def __init__(self, name: str) -> None:
        self.name: str = name
        self.mood: str = "neutral"

    def __repr__(self) -> str:
        """
        Возвращает строку с описанием объекта.
        """
        return f"<Companion name={self.name} mood={self.mood}>"
```

```python
bot: Companion = Companion("Echo")
print(bot)
```

Вывод будет таким:

```
<Companion name=Echo mood=neutral>
```

Метод `__repr__()` особенно полезен при отладке  
и при выводе объектов в терминале.

---

### 🧠 Задание: Построй свой объект

Создай собственный класс:
- Определи **минимум два атрибута**
- Напиши **три метода**, которые работают с атрибутами
- Добавь метод `__repr__()`, если хочешь сделать объект читаемым

Ты больше не просто пишешь код.  
Ты создаёшь **модель поведения**.

Скоро эти объекты будут соединяться,  
передавать данные, эволюционировать.

---

В [**Главе 9: Коллекции**](Chapter_09.md)  
герой научится собирать —  
работать **со множеством объектов**,  
перебирать, искать, группировать.

Ты готов?
