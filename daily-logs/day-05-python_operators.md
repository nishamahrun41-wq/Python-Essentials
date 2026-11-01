# Day 5 : Python Operators

## 1. Core Arithmetic Operators

* **Exponentiation (`**`):** Calculates power (e.g., `2 ** 3 = 8`). Uses **right-sided binding** (evaluates right to left).
* **Multiplication (`*`):** Standard multiplication (e.g., `2 * 3 = 6`).
* **Standard Division (`/`):** **Always returns a `float`**, even for whole numbers (e.g., `6 / 3` $\rightarrow$ `2.0`).
* **Floor / Integer Division (`//`):** Truncates the fractional part and **rounds down to the lesser integer** (e.g., `6 // 4 = 1`, `-6 // 4 = -2`).
* **Modulo / Remainder (`%`):** Returns the remainder left over after integer division (e.g., `14 % 4 = 2`).
* **Addition (`+`):** Standard addition (e.g., `2 + 3 = 5`).
* **Subtraction (`-`):** Subtraction; also acts as a unary operator to flip numerical signs.

---

## 2. Key Execution Rules

* **Integer vs. Float Rule:** 
  * Operating on two integers results in an integer (`int`).
  * If at least one operand is a float, the result is a float (`float`).
  * *Exception:* Standard division (`/`) **always** outputs a `float`.
* **Floor Division Rounding:** Always rounds toward the lesser integer on a number line (e.g., `-1.5` rounds down to `-2`).
* **Unary vs. Binary:**
  * **Unary:** Operates on 1 value (e.g., `-4`, `+2`).
  * **Binary:** Operates on 2 values (e.g., `4 - 2`).
* **Division by Zero:** Division, integer division, or modulo by zero triggers a `ZeroDivisionError`.

---

## 3. Operator Hierarchy & Binding

### Priority Order (Highest to Lowest)
1. **`**`** (Exponentiation)
2. **Unary `+`, `-`** *(note: unary operators located next to the right of `**` bind more strongly)*
3. **`*`, `/`, `//`, `%`**
4. **Binary `+`, `-`**

### Binding Rules
* **Left-Sided Binding (Default):** Evaluates left to right (e.g., `9 % 6 % 2` $\rightarrow$ `(9 % 6) % 2 = 1`).
* **Right-Sided Binding (`**`):** Exponentiation evaluates right to left (e.g., `2 ** 3 ** 2` $\rightarrow$ `2 ** (3 ** 2)` $\rightarrow$ `2 ** 9 = 512`).

---

## 4. Section Quiz Code Examples & Outputs

```python
# Question 1: Basic Operations & Types
print((2 ** 4), (2 * 4.), (2 * 4))
# Output: 16 8.0 8

# Question 2: Standard vs Floor Division with Negative Numbers
print((-2 / 4), (2 / 4), (2 // 4), (-2 // 4))
# Output: -0.5 0.5 0 -1

# Question 3: Modulo with Negative Divisor & Exponentiation Chaining
print((2 % -4), (2 % 4), (2 ** 3 ** 2))
# Output: -2 2 512
