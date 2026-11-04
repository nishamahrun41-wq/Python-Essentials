# 3.1 - Making Decisions in Python 🐍

This section covers the core concepts of conditional execution and decision-making logic in Python, including comparison operators, conditional statements (`if`, `elif`, `else`), and code structuring.

---

## 📌 Topics Covered

- **Comparison Operators:** `==`, `!=`, `>`, `<`, `>=`, `<=`
- **Conditional Statements:**
  - `if` statements
  - `if-else` statements
  - `if-elif-else` cascades
  - Nested `if` statements
- **Logic & Flow:** Truth values, indentation rules, and decision structures.

---

## 💻 Summary of Key Concepts

### 1. Comparison Operators
| Operator | Description | Example (`x = 5`, `y = 10`) | Result |
| :---: | :--- | :--- | :---: |
| `==` | Equal to | `x == y` | `False` |
| `!=` | Not equal to | `x != y` | `True` |
| `>` | Greater than | `y > x` | `True` |
| `<` | Less than | `x < y` | `True` |
| `>=` | Greater than or equal to | `x >= 5` | `True` |
| `<=` | Less than or equal to | `y <= 5` | `False` |

### 2. Conditional Structure Syntax

```python
# Standard if-elif-else cascade
x = 10

if x > 15:
    print("x is greater than 15")
elif x == 10:
    print("x is exactly 10")
else:
    print("x is less than 10")
