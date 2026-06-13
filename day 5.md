# Day 5 — Readability, Documentation & Refactoring

Clean code is easier to read, test, and maintain. This guide covers three related practices and the Cursor prompts that help apply them.

---

## 1. Refactoring

Refactoring improves structure without changing behavior. Focus on **meaningful names**, **small functions**, and **removing duplication**.

### 1.1 Meaningful Names

**Before**

```python
def calc(a, b, c):
    x = a * b
    y = x - c
    return y
```

**After**

```python
def calculate_discounted_price(price, quantity, discount):
    """
    Calculate final price after discount.

    Args:
        price (float): Price of one item.
        quantity (int): Number of items.
        discount (float): Discount amount.

    Returns:
        float: Final payable amount.
    """
    total_price = price * quantity
    final_price = total_price - discount
    return final_price
```

### 1.2 Removing Duplicate Logic

**Before**

```python
price1 = item1_price * quantity1
price2 = item2_price * quantity2
price3 = item3_price * quantity3
```

**After**

```python
def calculate_price(price, quantity):
    return price * quantity
```

---

## 2. Readability

Readable code expresses intent clearly. Prefer direct constructs over clever or indirect ones.

### 2.1 Iterate Directly Over Collections

**Before**

```python
for i in range(len(users)):
    print(users[i])
```

**After**

```python
for user in users:
    print(user)
```

---

## 3. Documentation

Document **why** and **what** a function does. Use docstrings for public APIs; reserve inline comments for non-obvious logic.

### 3.1 Docstring Example

Generated function documentation using Cursor:

```python
def add_numbers(a, b):
    """
    Add two numbers and return the result.

    Args:
        a (int | float): First number.
        b (int | float): Second number.

    Returns:
        int | float: Sum of both numbers.
    """
    return a + b
```

---

## 4. Cursor Prompts

Use these prompts in Cursor to apply the practices above.

### Refactor Code

```text
Refactor this code using clean code principles and meaningful variable names.
```

### Improve Readability

```text
Improve the readability and maintainability of this Python code.
```

### Generate Documentation

```text
Generate professional docstrings and comments for this function.
```

### Explain Code

```text
Explain this code and suggest improvements.
```
