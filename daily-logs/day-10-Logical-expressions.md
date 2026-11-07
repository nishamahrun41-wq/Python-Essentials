# Module Study Notes: Python Essentials 1

## Section 3.3.2: Logical Expressions

## 1. Logical Expressions & De Morgan's Laws
- *Logical Expressions:* Expressions using logical operators (`and`, `or`, `not`) to combine or invert boolean conditions.
- *Equivalent Formulations:*
  - `var > 0` is equivalent to `not (var <= 0)`
  - `var != 0` is equivalent to `not (var == 0)`
- *De Morgan's Laws:*
  - *Rule 1:* The negation of a conjunction is the disjunction of the negations:  
    `not (p and q) == (not p) or (not q)`
  - *Rule 2:* The negation of a disjunction is the conjunction of the negations:  
    `not (p or q) == (not p) and (not q)`
- *Abbreviated Assignment Restriction:* Logical operators (`and`, `or`, `not`) **cannot** be used in abbreviated assignment form (e.g., there is no `and=` or `or=` operator).

## Section Code Examples

```python
# 1. De Morgan's Laws Verification
p = True
q = False

# Rule 1 Check
print(not (p and q) == (not p) or (not q))  # Output: True

# Rule 2 Check
print(not (p or q) == (not p) and (not q))  # Output: True
