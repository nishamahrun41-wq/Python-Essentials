# Module 2 Study Notes: 

## Section 2.4: Variables

### 1. Basics & Rules
* **Definition:** Named memory containers that store values. Created automatically when assigned a value using `=`.
* **Naming Rules:**
  * Must start with a letter or underscore (`_`); **cannot start with a digit** (e.g., `101` is illegal).
  * Allowed characters: letters, numbers, underscores. No spaces or special characters.
  * Case-sensitive (`var` $\neq$ `Var`). Cannot use reserved keywords (e.g., `import`, `del`).
* **Naming Style:** Use `snake_case` per PEP 8 guidelines.

### 2. Compound Assignment Shortcuts
Shorthand for `variable = variable op expression`:
* `x += 1` $\rightarrow$ `x = x + 1`
* `x *= 2` $\rightarrow$ `x = x * 2`
* `x /= 2` $\rightarrow$ `x = x / 2`
* `x %= 10` $\rightarrow$ `x = x % 10`
* `x **= 2` $\rightarrow$ `x = x ** 2`

---

## Section Code Examples

```python
# Formatting & Escape Sequences
print("Line 1\nLine 2", end=" | ")
print("A", "B", sep="-")
# Output:
# Line 1
# Line 2 | A-B

# Literals & Bases
print(0o123, 0x123, 3E8, True > False)
# Output: 83 291 300000000.0 True

# Operators & Precedence
print((2 ** 4), (-2 // 4), (2 ** 3 ** 2))
# Output: 16 -1 512

# Variables & Compound Division
a = 6
b = 3
a /= 2 * b  # Right side evaluated first: 2 * 3 = 6, then 6 / 6
print("a =", a)
# Output: a = 1.0
