# Python Essentials 1 - Section 3.2: Loops in Python

Comprehensive summary notes covering all concepts, syntax, and lab logic from Module 3, Section 2 of Python Essentials 1.

---

## 1. The `while` Loop

* **Concept:** Repeats execution of a block of code as long as a specified condition evaluates to `True`.
* **Indentation:** All instructions inside the loop body must be indented identically.
* **First Test:** If the condition evaluates to `False` on the first test, the loop body is skipped entirely.

```python
# Counter variable pattern to exit safely
counter = 5
while counter > 0:
    print("Inside loop:", counter)
    counter -= 1
Infinite Loops & InterruptsAn infinite loop occurs when the condition never becomes False (e.g., while True:).Press Ctrl + C in the terminal to stop an infinite loop (KeyboardInterrupt).Pythonic Truthiness Shortcutwhile counter: is equivalent to while counter != 0: (Python treats non-zero numbers as True and 0 as False).2. The for Loop and range() FunctionConcept: Used to iterate over a sequence of items or execute a block of code a set number of times using an automatic control variable.pass Keyword: An empty placeholder instruction used when syntax requires a body but no action is needed.range() Function SyntaxInvocationRange GeneratedExamplerange(stop)Starts at 0, goes up to (excluding) stoprange(3) -> 0, 1, 2range(start, stop)Starts at start, goes up to (excluding) stoprange(2, 6) -> 2, 3, 4, 5range(start, stop, step)Starts at start, increments by step, goes up to stop - 1range(2, 8, 3) -> 2, 5Rules: All range() arguments must be integers. If start >= stop (e.g., range(2, 1)), the range is empty and the loop does not execute.3. Loop Control Statements (break and continue)break: Exits the loop immediately and moves to the first instruction following the loop.continue: Skips the remainder of the current iteration and jumps straight to evaluating the condition for the next turn.Python# break example (prints: 1, 2)
for i in range(1, 6):
    if i == 3:
        break
    print(i)

# continue example (prints: 1, 2, 4, 5)
for i in range(1, 6):
    if i == 3:
        continue
    print(i)
4. Loops with an else BranchBoth while and for loops in Python can be paired with an else: block.Execution Rule: The else block executes once after the loop finishes naturally.Break Exception: If a loop is exited early using a break statement, the else branch is skipped entirely.Variable Scope: In for...else, the control variable retains its last assigned value. If the loop body never runs, it retains whatever value it had prior to the loop.5. Summary of Section Labs & Algorithms3.2.4 Guess the Secret Number: while loop checks user input against a target number until matched.3.2.7 Counting Mississippily: for i in range(1, 6): combined with time.sleep(1) to pause between outputs.3.2.9 Stuck in a Loop: while True: loop reading words until the user enters "chupacabra", which triggers break.3.2.10 & 3.2.11 Vowel Eaters: Iterates over uppercase text, using if letter in "AEIOU": continue to filter out vowels.3.2.14 Pyramid Builder: while loop subtracts required blocks per layer (1, 2, 3...) from available blocks to determine completed height levels.3.2.15 Collatz's Hypothesis: while c0 != 1: loop executing $c_0 = c_0 // 2$ (if even) or $c_0 = 3 \times c_0 + 1$ (if odd) until the number collapses to 1.