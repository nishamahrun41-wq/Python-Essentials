# Module 2 Log: Sections 2.5 & 2.6

---

## Section 2.5: Comments

* **Purpose:** Notes inside code written for human readers to explain logic or intent.
* **Execution:** Completely **ignored by Python** during runtime.
* **Syntax:** Starts with `#` (applies to the end of that line). Multi-line comments require `#` on every line.
* **Shortcut:** Use `CTRL + /` (Win) or `CMD + /` (Mac) to comment/uncomment code lines.
* **Best Practice:** Keep comments accurate and meaningful; prefer clear variable names over unnecessary comments.

---

## Section 2.6: Interaction with the User

### 1. The `input()` Function
* **Purpose:** Reads user input from the console (returns execution back to the program).
* **Return Type:** **Always returns a string (`str`)**, even if the user enters digits.
* **Prompt Parameter:** Can accept a string argument to display a prompt message (e.g., `input("Enter name: ")`).
* **Storage:** Always assign `input()` to a variable, otherwise the entered data is lost.

### 2. Type Casting (Type Conversions)
Because `input()` returns a string, numerical operations require explicit type conversion:
* **`int(string)`:** Converts a valid string into an integer.
* **`float(string)`:** Converts a valid string into a float.
* **`str(number)`:** Converts a number (or other data types) into a string.
* **Chaining Example:** `val = float(input("Enter number: "))`

### 3. String Operators
* **Concatenation (`+`):** Glues two strings together (e.g., `"Py" + "thon"` $\rightarrow$ `"Python"`). Both operands must be strings (not commutative: `"a" + "b"` $\neq$ `"b" + "a"`).
* **Replication (`*`):** Multiplies a string by an integer (e.g., `"Hi" * 3` $\rightarrow$ `"HiHiHi"`). Multiplying by a number $\le 0$ produces an empty string (`""`).

---

