# Module 3 Study Notes:

## Section 3.2: Loops in Python

## 1. The `while` Loop & Counter Variables
- *Definition:* Executes a block of code continuously as long as a boolean condition evaluates to `True`.
- *First Test:* If the condition is `False` initially, the loop body does not run at all.
- *Infinite Loops:* Occurs when the condition never becomes `False` (e.g., `while True:`). Press `Ctrl + C` in the console to stop (`KeyboardInterrupt`).
- *Counter Pattern:* Incrementing or decrementing a variable to safely reach a condition and exit the loop.
- *Truthiness Shortcut:* `while counter:` is equivalent to `while counter != 0:` (non-zero numbers evaluate to `True`, `0` evaluates to `False`).

## 2. The `for` Loop & `range()` Function
- *Definition:* Used to iterate over a sequence of values or repeat execution for a fixed count using an automatic control variable.
- *The `pass` Keyword:* An empty instruction placeholder required when syntax demands a loop body but no action is needed.
- *The `range()` Function Arguments:*
  - `range(stop)` → Starts at `0`, goes up to (excluding) `stop`. (e.g., `range(3)` → `0, 1, 2`)
  - `range(start, stop)` → Starts at `start`, goes up to (excluding) `stop`. (e.g., `range(2, 6)` → `2, 3, 4, 5`)
  - `range(start, stop, step)` → Starts at `start`, increments by `step`, goes up to `stop - 1`. (e.g., `range(2, 8, 3)` → `2, 5`)
- *Range Rules:* Arguments must be integers. If `start >= stop` (e.g., `range(2, 1)`), the range is empty and the loop body will not execute.

## 3. Loop Control Statements (`break` and `continue`)
- *`break`:* Immediately terminates the loop and jumps to the first instruction following the loop body.
- *`continue`:* Skips the rest of the current iteration and jumps directly to evaluating the condition for the next pass.

## 4. Loops with an `else` Branch
- *Execution:* The `else` block executes **once** after the loop finishes naturally (when the condition becomes `False` or the sequence ends).
- *Break Exception:* If the loop is terminated early using `break`, the `else` branch is **skipped entirely**.
- *Control Variable Scope:* In `for...else`, the variable retains its last assigned value. If the loop never ran, it retains its value prior to the loop.

## 5. Lab Scenarios & Problem Logic
- *Guess the Secret Number:* `while` loop continuously prompts for input until user input equals `secret_number`.
- *Counting Mississippily:* `for i in range(1, 6):` combined with `time.sleep(1)` to pause execution between iterations.
- *Vowel Eater:* Iterates over uppercase text with `user_word.upper()` and uses `if letter in "AEIOU": continue` to skip vowels.
- *Pyramid Builder:* `while` loop subtracts required layer blocks (`1, 2, 3...`) from total available blocks to count complete height levels.
- *Collatz's Hypothesis:* `while c0 != 1:` calculates `c0 // 2` (if even) or `3 * c0 + 1` (if odd) until $c_0$ collapses to 1.

## Section Code Examples

```python
# 1. The while Loop & Truthiness
counter = 3
while counter:
    print("Inside while loop:", counter)
    counter -= 1
else:
    print("Loop ended naturally at counter =", counter)
# Output:
# Inside while loop: 3
# Inside while loop: 2
# Inside while loop: 1
# Loop ended naturally at counter = 0

# 2. The for Loop & range() Variations
for i in range(2, 8, 3):
    print("Value of i:", i)
# Output:
# Value of i: 2
# Value of i: 5

# 3. break vs continue
print("break statement:")
for i in range(1, 6):
    if i == 3:
        break
    print(i, end=" ")
# Output: 1 2 

print("\ncontinue statement:")
for i in range(1, 6):
    if i == 3:
        continue
    print(i, end=" ")
# Output: 1 2 4 5
