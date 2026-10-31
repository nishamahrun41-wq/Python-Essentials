# Day 4 Log: Python Literals (Section 2.2)

## 1. What is a Literal?
* **Literal:** Data whose value is determined directly by the literal itself (fixed values hardcoded into the script).
  * `123` is a literal because it always represents the number *123*.
  * `c` is **not** a literal because it is a variable/symbol (could mean speed of light, hypotenuse, etc.).

---

## 2. Integer Literals (`int`)
Whole numbers without fractional components (e.g., `5`, `-20`, `0`).

* **Formatting Rules:**
  * Do **not** use commas or spaces for large numbers (e.g., `11,111,111` is **invalid**).
  * Use **underscores (`_`)** for readability (e.g., `11_111_111` equals `11111111`).
* **Alternative Number Bases:**
  * **Octal (Base 8):** Prefix with `0o` or `0O` (e.g., `print(0o123)` $\rightarrow$ `83`).
  * **Hexadecimal (Base 16):** Prefix with `0x` or `0X` (e.g., `print(0x123)` $\rightarrow$ `291`).

---

## 3. Floating-Point Literals (`float`)
Numbers with a non-empty decimal fraction (e.g., `2.5`, `-0.4`).

* **Decimal Point Rule:** Always use a point (`.`), never a comma.
* **Shortcuts:** You can omit `0` before or after a point (`.4` means `0.4`, and `4.` means `4.0`).
* **`int` vs `float`:** `4` is an integer, whereas `4.0` is a float.
* **Scientific Notation (Exponent):** Uses `e` or `E` (times $10^n$).
  * Speed of light: `3E8` ($3 \times 10^8$)
  * Planck's constant: `6.62607E-34` ($6.62607 \times 10^{-34}$)

---

## 4. String Literals (`str`)
Used for storing and processing text.

* **Delimiters:** Enclosed in matching single (`'...'`) or double (`"..."`) quotes.
* **Escaping Quotes:**
  * Backslash (`\`) escapes quotes inside the string: `print("I like \"Monty Python\"")`
  * Alternatively, alternate quote types: `print('I like "Monty Python"')`
* **Empty String:** Valid string containing no characters (`""` or `''`).

---

## 5. Boolean Literals (`bool`)
Represents truth values with exactly two constants:
* `True` (equals `1` in numeric contexts)
* `False` (equals `0` in numeric contexts)
* **Strictly Case-Sensitive:** Must be capitalized (`True`/`False`).

---

## 6. Section Quiz Answers Quick Reference

1. **`"Hello "`, `"007"`:** Both are **string literals** (quotes treat digits as text).
2. **`"1.5"`, `2.0`, `528`, `False`:**
   * `"1.5"` $\rightarrow$ String
   * `2.0` $\rightarrow$ Float
   * `528` $\rightarrow$ Integer
   * `False` $\rightarrow$ Boolean
3. **Binary `1011` to Decimal:** **`11`** ($2^3 + 2^1 + 2^0 = 8 + 2 + 1$).
