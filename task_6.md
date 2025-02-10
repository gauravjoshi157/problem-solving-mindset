# Task 6: Operators: Arithmetic, Assignment, Comparison, Logical

**Objective:**
Understand the syntax and usage of different operators in Python.

- **Practice:**

    - Perform arithmetic operations.
    - Use comparison and logical operators to check conditions (e.g., if student score > 50 then print "Pass"). complete this task in the predefined format.


**1. Arithmetic Operators**
- Arithmetic operators perform mathematical operations on numbers.
- **Example:**

```python
# Arithmetic Operations
x = 10
y = 5

addition = x + y  # 10 + 5 = 15
subtraction = x - y  # 10 - 5 = 5
multiplication = x * y  # 10 * 5 = 50
division = x / y  # 10 / 5 = 2.0
modulus = x % y  # 10 % 5 = 0
exponentiation = x ** y  # 10^5 = 100000
floor_division = x // y  # 10 // 5 = 2

print("Addition:", addition)
print("Subtraction:", subtraction)
print("Multiplication:", multiplication)
print("Division:", division)
print("Modulus:", modulus)
print("Exponentiation:", exponentiation)
print("Floor Division:", floor_division)
```

**Advantages of Arithmetic Operators:**
- Perform mathematical calculations easily.
- Work on integers and floating-point numbers.

**Disadvantages:**
- Division by zero can cause errors.


**2. Assignment Operators**
- Used to assign values to variables.
- **Example:**

```python
# Assignment Operators
x = 10
x += 5  # Equivalent to x = x + 5 (x = 15)
x -= 3  # Equivalent to x = x - 3 (x = 12)
x *= 2  # Equivalent to x = x * 2 (x = 24)
x /= 4  # Equivalent to x = x / 4 (x = 6.0)
x %= 5  # Equivalent to x = x % 5 (x = 1)
x **= 2  # Equivalent to x = x ** 2 (x = 1)
x //= 2  # Equivalent to x = x // 2 (x = 0)

print("Final value of x:", x)
```

**Advantages of Assignment Operators:**
- Concise way to perform operations and assign values.
- Improves readability.

**Disadvantages:**
- Can sometimes reduce clarity when overused.


**3. Comparison Operators**
- Used to compare two values.
- **Example:**

```python
# Comparison Operators
x = 10
y = 5

print("x == y:", x == y)  # False
print("x != y:", x != y)  # True
print("x > y:", x > y)  # True
print("x < y:", x < y)  # False
print("x >= y:", x >= y)  # True
print("x <= y:", x <= y)  # False
```

**Advantages of Comparison Operators:**
- Essential for decision-making in programming.

**Disadvantages:**
- Only return boolean values (True or False), which may require additional logic.


**4. Logical Operators**
- Used to combine conditional statements.
- **Example:**

```python
# Logical Operators
x = 10
y = 5
z = 15

print("x > y and y < z:", x > y and y < z)  # True
print("x < y or y < z:", x < y or y < z)  # True
print("not(x > y):", not(x > y))  # False
```

**Advantages of Logical Operators:**
- Allow complex conditions to be evaluated efficiently.

**Disadvantages:**
- May lead to logical errors if conditions are not properly structured.


**Outcome:**
- Understand different types of operators.
- Learn how to use arithmetic, assignment, comparison, and logical operators.
- Apply these operators in real-world scenarios.

