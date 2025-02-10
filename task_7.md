# Task 7: Conditional Statements (if, elif, else)
- **Objective:**
    - To implement conditions for decision-making.

- **Practice:**
    -Write a program that displays different messages based on a student's performance (e.g., “Needs Improvement”, “Good”, “Excellent”).

1. **Conditional Statements:**
    - Conditional statemnt are used to executes different blocks of code and depending on whether a condition is `True` or `False`. 

2. **`if` Statement:** 
    - The `if` Statement execute a block of code if the condition evaluates to `True`.
    - **Example:**
    ```python
        score = 85
        if score > 50:
            print("Pass")
    ```
3. **`if`-`else` Statement:**
    - The else block runs when the condition in the if statement is False.
    - **Example:**
    ```python
        score = 40
        if score > 50:
            print("Pass"
            )
        else:
            print("Fail")
    ```
4. **`if`-`elif`-`else` Statement:**
    - The elif (short for "else if") allows multiple conditions to be checked in sequence.
    - **Example:**
    ```python
    score = 75

    if score >= 90:
        print("Excellent")
    elif score >= 70:
        print("Good")
    elif score >= 50:
        print("Needs Improvement")
    else:
        print("Fail")
    ```

5. **Advantages of Conditional Statements:**
- Enables decision-making in programs.
- Improves readability and maintainability.
- Reduces redundant code by allowing logical flow control.

6. **Disadvantages of Conditional Statements**
- Overuse can make code complex and hard to debug.
- Nested conditions can reduce performance and readability.

7. **Practice:**
- Write a program that displays different messages based on a student's performance.
```python
score = int(input("Enter the student's score: "))

if score >= 90:
    print("Excellent")
elif score >= 70:
    print("Good")
elif score >= 50:
    print("Needs Improvement")
else:
    print("Fail")
```
8. **outcomes:**
- Understand how to use conditional statements.
- Implement logic for decision-making in Python programs.
- Differentiate between if, elif, and else conditions.
