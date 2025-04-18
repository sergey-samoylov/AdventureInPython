### 🧬 Глава 42: Общая ДНК — Псевдонимы в Python  
*from **Adventure in Python** by Sergey Samoylov*

---

Герой пытался отладить тонкую ошибку.  
Две переменные должны были хранить *разные* списки.  
Но при изменении одной... менялась и другая.

Он уставился в код:

```python
companions = ["Бит", "Байт"]
team = companions
team.append("Баг")
print(companions)  # ['Бит', 'Байт', 'Баг']
```

Почему?

---

🧠 **Осознание**:  
В Python переменные не содержат значения напрямую.  
Они *ссылаются* на объекты в памяти.

Когда мы пишем:

```python
team = companions
```

Мы не копируем список.  
Мы создаём **псевдоним** — второе имя для одного и того же объекта.

---

🧪 Герой начал экспериментировать:

```python
a = [1, 2]
b = a
a.append(3)
print(b)  # [1, 2, 3]
```

Он попытался защитить второй список, сделав копию:

```python
a = [1, 2]
b = a.copy()
a.append(3)
print(b)  # [1, 2]
```

Сработало.

---

> "Остерегайся теней с именами", — сказал Терминал.  
> "Они несут твои данные — и последствия."

---

### 🧩 Задание для читателя

У вас есть список показаний сенсора:

```python
readings = [0.95, 1.01, 0.99]
```

1. Создайте функцию, которая изменяет этот список (например, добавляет значение).
2. Посмотрите, что произойдёт, если передать список напрямую.
3. Затем напишите безопасную версию, которая делает копию списка внутри функции.

**Дополнительно**: Можете ли вы придумать ситуацию,  
в которой псевдоним может быть *полезен*?

---

*"Псевдоним — это не близнец, это твоя тень."*  
— Терминал

---

[Глава 43](Chapter_43.md)
