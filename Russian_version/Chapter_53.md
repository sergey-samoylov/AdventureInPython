### 🧱 Глава 53: Вход в класс (с docstring)

Программист шагнул через мерцающий портал.

Перед ним раскинулся новый, загадочный мир,  
где **чертежи воплощают сущности**,  
а логика приобретает форму через имена и уровни.

Символ, пульсирующий энергией, сиял в воздухе:

```python
class Hero:
    """Отважный герой с именем и уровнем в перспективе :-)."""
    pass
```

На первый взгляд — просто структура.  
Но на самом деле — это **источник силы**.

---

### 🧬 Что такое класс?

**Класс** — это чертёж для создания **объектов**.

Он позволяет вам описать **собственный тип данных**,  
такой же, как `str`, `int` или `list`, но сделанный вами.

Вы решаете:
- какие данные объект хранит (атрибуты)
- что он умеет делать (методы)

> Класс — это не вещь. Это *рецепт*, по которому можно создать множество вещей.

---

### 🔨 Создаём класс и объект

Давайте создадим героя:

```python
class Hero:
    """Класс, представляющий героя с именем и уровнем."""

    def __init__(self, name: str, level: int):
        """Инициализирует нового героя с именем и уровнем."""
        self.name = name
        self.level = level

    def speak(self) -> None:
        """Герой произносит своё имя и уровень."""
        print(f"I am {self.name}, level {self.level}!")
```

Теперь создадим **объект** (экземпляр класса):

```python
knight = Hero("Galahad", 3)
knight.speak()
# Вывод: I am Galahad, level 3!
```

---

### 🧩 Разбираем по частям

- `class Hero`: определяет новый шаблон — класс `Hero`
- `__init__`: специальный метод, который вызывается **при
  инициализации(создании) объекта**
- `self`: ссылка на конкретный объект, с которым мы работаем
- `self.name`, `self.level`: **атрибуты/свойства** — данные, хранящиеся внутри объекта
- `speak`: **метод** — функция, привязанная к объекту

---

### 🔁 Вы можете создавать сколько угодно героев

```python
rogue = Hero("Nyx", 5)
rogue.speak()
```

Каждый объект уникален, но построен по одному чертежу.

---

### 🧠 Зачем нужны классы?

Классы позволяют:
- Объединять данные и поведение
- Создавать упорядоченные и переиспользуемые структуры
- Справляться со сложностью больших программ

---

### 🎯 Задание для тебя

Создай класс `Spell`, в котором:

- Метод `__init__()` принимает `name: str` и `power: int`
- Метод `cast()` выводит, например:
  ```
  Casting Fireball! (Power: 50)
  ```

С docstring:

```python
class Spell:
    """Магическое заклинание с именем и силой."""

    def __init__(self, name: str, power: int):
        """Создаёт заклинание с указанным именем и силой."""
        self.name = name
        self.power = power

    def cast(self) -> None:
        """Произносит заклинание и показывает его эффект."""
        print(f"Casting {self.name}! (Power: {self.power})")
```

Попробуй:

```python
fireball = Spell("Fireball", 50)
fireball.cast()
```

---

Дальше — 🧙‍♂️ **[Глава 54](Chapter_54.md): Магия объектов — что такое self**

Продолжим?
