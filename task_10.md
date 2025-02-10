# Task 10: Functions – Definition and Basic Syntax

**Objective:**
- Understand what functions are, their syntax, and why they are used (DRY: Don’t Repeat Yourself).

**Practice:**
- Create a simple function that prints a greeting.
- Use functions in a mini project to avoid repetitive code.

**What is a Function?**
A function is a block of organized, reusable code that performs a single, related action. Functions provide better modularity for your application and a high degree of code reusability.

**Syntax:**
```python
def function_name(parameters):
    # Code to execute
    return value
```
1. **Creating a Simple Function:**

 A basic example of a function that prints a greeting.

**Example:**
```python
def greet():
    print("Hello, welcome to the world of Python!")

# Calling the function
greet()
```

**Output:**
```python
Hello, welcome to the world of Python!
```
2. **Function with Parameters:** 

Functions can take parameters to make them more flexible.

**Example:**
```python
def greet(name):
    print(f"Hello, {name}! Welcome to the world of Python!")

# Calling the function with an argument
greet("Alice")
```
3. **Function with Return Value:**

 Functions can return values using the return statement.

**Example:**
```python
def add(a, b):
    return a + b

# Calling the function and storing the result
result = add(3, 5)
print(f"The sum is: {result}")
```
**Output:**
```python
The sum is: 8
```
4. **Using Functions to Avoid Repetitive Code:** 

Functions help in avoiding code repetition by encapsulating reusable code blocks.

**Example:**
```python

def display_menu():
    print("Menu:")
    print("1. Option 1")
    print("2. Option 2")
    print("3. Exit")

# Calling the function multiple times
display_menu()
```
**Output:**
```python
Menu:
1. Option 1
2. Option 2
3. Exit
```
5. **Advantages of Functions:**

- Improves code readability and organization.
- Facilitates code reuse and avoids redundancy.
- Makes code easier to maintain and debug.
6. **Disadvantages of Functions:**

- Overhead of function calls can affect performance in some cases.
- Improper use can lead to complex and hard-to-understand code.
7. **Common Use Cases:**

- Encapsulating repetitive tasks.
- Modularizing code for better organization.
- Implementing algorithms and logic in a reusable manner.

8. **Practice:** 

Create a function that takes a name as a parameter and prints a personalized greeting.
```python
def personalized_greet(name):
    print(f"Hello, {name}! How are you today?")

# Calling the function with different names
personalized_greet("Bob")
personalized_greet("Alice")
```

9. **Outcome:**

- Learn how to define and use functions in Python.
- Understand the importance of functions in avoiding code repetition.
- Apply functions in practical contexts, such as creating a simple calculator.
- Understand the use of parameters and return values in functions.
- Similar code found with 1 license type - View matches

