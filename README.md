# special-methods
special methods allow your objects to behave like built-in types 
magic/dunder
---

## 1. `__init__` — Object Constructor

Used in almost every class in your file.

### What it does:

Runs automatically when you create an object.

### Examples in your file:

* `Student(name, age)`
* `Vector(x, y)`
* `BankAccount(balance)`
* `Playlist(songs)`

### Meaning:

It initializes object attributes.

```python
s = Student("Matthew", 30)
```

Here, `__init__` sets `name` and `age`.

---

## 2. `__str__` — User-Friendly String Representation

### What it does:

Controls what you see when you do `print(object)`.

### Examples:

* `Student: name`
* `(x, y)` for Vector
* number display in `Number`

### Meaning:

Makes objects readable for humans.

```python
print(Student("Mattew"))
```

Outputs something like:

```
Student: Mattew
```

---

## 3. `__repr__` — Developer-Friendly Representation

### What it does:

Returns a detailed/debug version of the object.

### Example:

```python
repr(Student("Daniella"))
```

### Difference from `__str__`:

* `__str__` → for users
* `__repr__` → for developers/debugging

---

## 4. `__add__` — Addition Operator (`+`)

### Used in:

`Vector` class

### What it does:

Defines how `+` works for objects.

```python
v1 + v2
```

### Meaning:

Adds corresponding values of two vectors.

---

## 5. `__sub__` — Subtraction Operator (`-`)

### Used in:

`Vector` class

### What it does:

Defines behavior of subtraction between objects.

```python
v1 - v2
```

---

## 6. `__mul__` — Multiplication Operator (`*`)

### Used in:

`Number` class

### What it does:

Defines how multiplication works for objects.

```python
n1 * n2
```

---

## 7. `__eq__` — Equality Comparison (`==`)

### Used in:

`Student` class (ID comparison)

### What it does:

Defines what makes two objects equal.

```python
s1 == s2
```

### Meaning:

Students are equal if their `student_id` matches.

---

## 8. `__len__` — Length Function (`len()`)

### Used in:

`Playlist`

### What it does:

Allows `len(object)` to work.

```python
len(p)
```

Returns number of songs.

---

## 9. `__getitem__` — Indexing (`obj[index]`)

### Used in:

`Grades`

### What it does:

Lets you access elements using brackets.

```python
g[0]
```

Returns first grade.

---

## 10. `__setitem__` — Assigning Values (`obj[index] = value`)

### Used in:

`Grades`

### What it does:

Lets you modify items using indexing.

```python
g[1] = 100
```

---

## 11. `__contains__` — Membership Test (`in`)

### Used in:

`Course`

### What it does:

Allows use of `in` keyword.

```python
"Joe" in c
```

Checks if student exists.

---

## 12. `__call__` — Makes Object Callable Like a Function

### Used in:

`Multiplier`

### What it does:

Lets an object behave like a function.

```python
double(10)
```

Returns:

```
20
```

---

## 13. `__iter__` — Makes Object Iterable

### Used in:

`Counter`

### What it does:

Allows looping over object:

```python
for num in Counter(5):
```

---

## 14. `__next__` — Iterator Step Function

### Works with `__iter__`

### What it does:

Returns next value in sequence.

Stops with `StopIteration`.

---

## 15. `__bool__` — Truth Value Testing

### Used in:

`BankAccount`

### What it does:

Controls how object behaves in conditions.

```python
if account:
```

Returns `True` if balance > 0.

---

## 16. `__del__` — Destructor

### Used in:

`FileHandler`, `Resource`

### What it does:

Runs when object is deleted or garbage collected.

Used for cleanup:

* closing files
* releasing resources

