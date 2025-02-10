# Task 11: Functions – Parameters, Return Values, and Scope

**Objective:** 
- Understand how to pass parameters, use return values, and differentiate between variable scope (local vs global).

**Practice:**
- Create a function that adds two numbers and returns the result.
- Implement functions in your mini-project for calculations or processing.

## **Parameters in Functions:**
- Parameters are the variable which is used inside function defination to  `recieve input values` when the  function is called. 
- You provide the `arguments` which is the real value passed in the parameters.

- **Example:**
```python
def greet_function(name):   # Here name is parameter.
    print(f"Welcome, {name}")

greet_function("Gaurav")    # Here Gaurav is an argument which is used in the function.
```
- **output:**
```python 
Welcome, Gaurav
```
**Types of Function Parameters in Python:**
1. **Positional Parameters**
2. **Default Parameters**
3. **Keyword Parameters**
4. **Arbitary Positional Parameters**
5. **Arbitary Keyword Parameters**


### 1. **Positional Parameters:** 
- Parameters that must be provided in correct order when calling the function.
- The number of arguments must be same as the number of parameters of the function, Otherwise it will give error.
- **Example**
```python
def add(a,b):   # Here `a` and `b` are the positional parameters
    print(a+b)

add(5,6)    # Order matters in positional parameters.
add(24,46)
```

- **Output**
```
11
70
```
- Positional parameters must always be provided unless a default value is set.


### 2. **Default Parameters:**
- Parameters have a default value if no arguments are passed.
- **Example**
```python
def greet(name = "Guest"):          # The parameter is assigned a default value "Guest"
    print(f"Welcome, {name}!")      # Printing the greet message.

greet("Gaurav")                     # Calling function with an argument 
greet()                             # Calling function without argument
```

- **Output**
```
Welcome, Gaurav!
Welcome, Guest!
```

- **Advantages of Default Parameters:**
    - Makes functions flexible (you can call them with or without arguments).
    - Helps avoid errors from missing arguments.


### 3. **Keyword Parameters:**
- When calling a function you define parameter names explicit, `ignoring the order`. 
- **Example**
```Python
def person_details(name, age, city):        # Keyword parameters also refered as named arguments
    print(f"{name} is {age} years old and lives in {city}")

person_details(name = "Gaurav Joshi", age = 25, city =  "Jaipur")       # Calling function with arguments 
person_details(city = "Jaipur", name = "Gaurav Joshi", age = 25)        # Order dosen't amtter here
```

- **Output**
```
Gaurav Joshi is 25 years old and lives in Jaipur
Gaurav Joshi is 25 years old and lives in Jaipur
```
- **Advantages of Keyword Parameters:**
    - Improves code readability.
    - Reduces errors from misordered arguments.

### 4. **Arbitary Positional Arguments:**
- Arbitary Positionaal Arguments allow passing `multiple arguments` into function in the form of tuple.
- **Example**
```python
def sum_numbers(*numbers):       # Arbitary Positional Parameter are assigned via asterisk.
    print(f"Sum of the numbers is:{sum(numbers)}") # numbers is a tuple of all the arguments passed to the function.

sum_numbers(1,2,3,4,5,6,7,8,9,10) # Passing the numbers to the function.
sum_numbers(1,2,3,4,5) # Passing the numbers to the function.
```
- **Output**
```
Sum of the numbers is:55
Sum of the numbers is:15
```

- **Use Cases of `*args`:**
    - When you don’t know how many arguments will be passed.
    - Useful for functions like sum(), min(), and max().

### 5. **Arbitary Keyword Arguments:**
- Arbitary Keyword Arguments allow `multiple named arguments` into a function in the form of dictionary.
- **Example**
```python
def person_info(**info):     # Arbitary Positional Parameter are assigned via double asterisk.
    for key, value in info.items():     # info is a dictionary.
        print(f"{key} : {value}")

person_info(name = "John", age = 22, city = "New York", phone = "1234567890")     # Arbitary Positional Parameter are assigned via double asterisk.
```

- **Output**
```
name : John
age : 22
city : New York
phone : 1234567890
```
**Use Cases of `kwargs`:**
- When the number of named arguments is unknown.
- Useful in configuration settings or database queries.

### **8. Combining Different Parameter Types:**
- You can combine different types of parameters, but they must follow this order:
```
1️. Positional Parameters  
2. Default Parameters  
3️. *args (Arbitrary Positional Parameters)  
4️. **kwargs (Arbitrary Keyword Parameters)
```
- **Example**
```python
def example(a, b = 10, *args, **Kwargs):
    print(f" a = {a}")
    print(f" b = {b}")
    print(f" args = {args}")
    print(f" Kwargs = {Kwargs}")

example(1, 2, 3, 4, 5, 6, 7, 8, 9, 10, name = "John", age = 25, city = "New York")
```
- **Output**
```
a = 1
b = 2
args = (3, 4, 5, 6, 7, 8, 9, 10)
Kwargs = {'name': 'John', 'age': 25, 'city': 'New York'}
```
- **Benefits of Combining Parameters:**
    - Provides maximum flexibility in function calls.
    - Allows passing both fixed and variable arguments.


## **Return Values in Python Functions**

1. **What Are Return Values?**
    - A return value is the output of a function in Python. When a function completes execution, it can return a value to the caller using the return statement.

- **Example:**
```python
def add(a, b):
    return a + b  # Returning the sum of a and b

result = add(5, 10)
print(result)  # Output: 15
```
- Here, `add(5, 10)` returns `15`, which is stored in the variable result.

2. **Why Are Return Values Important?**
- Allows functions to produce meaningful output instead of just printing values.
- Improves code reusability – returned values can be used in different parts of a program.
- Enables function chaining – return values can be used as inputs to other functions.
- Follows the Single Responsibility Principle (SRP) – functions do one task and return results instead of handling multiple things.

3. **Types of Return Values in Python**

- Python functions can return different types of values:

1.  **Returning a Single Value**

A function can return a single value, such as an `integer`, `string`, `float`, or `boolean`.
```python
def square(num):
    return num * num

print(square(4))  # Output: 16
```
2. **Returning Multiple Values (Tuple Packing)**

A function can return multiple values as a tuple.
```python
def get_student_details():
    name = "Alice"
    age = 20
    course = "Python"
    return name, age, course  # Returning multiple values

student = get_student_details()
print(student)  # Output: ('Alice', 20, 'Python')

# Accessing individual values
name, age, course = get_student_details()
print(name, age, course)  # Output: Alice 20 Python
```
- This method is useful when a function needs to return multiple computed results.

3. **Returning a List**

If the number of values is variable, returning a `list` is better than a `tuple`.
```python
def get_even_numbers(limit):
    return [num for num in range(1, limit + 1) if num % 2 == 0]

print(get_even_numbers(10))  # Output: [2, 4, 6, 8, 10]
```
- This is useful when returning a collection of values that may change dynamically.

4. **Returning a Dictionary**

Returning a dictionary is useful when data has named keys.
```python
def get_student_data():
    return {"name": "Alice", "age": 20, "course": "Python"}

student = get_student_data()
print(student["name"])  # Output: Alice
```
- This approach improves readability and is useful when returning structured data.

5. **Returning a Function (Higher-Order Functions)**

A function can return another function.
```python
def multiplier(factor):
    def multiply(number):
        return number * factor
    return multiply  # Returning a function

double = multiplier(2)  # `double` is now a function that multiplies by 2
print(double(5))  # Output: 10
```
- This is commonly used in functional programming, such as decorators and closures.

6. **Returning None (No Return)**

If a function doesn’t use return, it implicitly returns None.
```python
def greet(name):
    print(f"Hello, {name}!")  # No return statement

result = greet("Alice")
print(result)  # Output: None
```
- Use this approach when a function only performs an action (e.g., printing, modifying a global state).

# Scope in Python

1. **What Is Scope?**
- In Python, scope refers to the region where a variable is accessible. When a variable is defined, it is only available within a certain part of the program.

2. **Types of Scope in Python**
- Python follows the LEGB Rule, which defines four types of scope:

    - Local Scope – Inside a function
    - Enclosing Scope – Inside nested functions
    - Global Scope – At the top level of a script/module
    - Built-in Scope – Provided by Python itself

3.**Local Scope (Function-Level Scope)**
- A variable declared inside a function is only accessible within that function.

- **Example:**
```python
def greet():
    message = "Hello, World!"  # Local variable
    print(message)

greet()  # Output: Hello, World!
print(message)  # Error: message is not defined
```
- Here, message is local to greet(), so it cannot be accessed outside the function.

4.**Enclosing Scope (Nested Functions)**
- When a function is defined inside another function, the inner function can access the variables of the outer function.

- **Example:**
```python
def outer_function():
    outer_var = "Outer"

    def inner_function():
        print(outer_var)  # Accessing enclosing variable

    inner_function()

outer_function()  # Output: Outer
```
- Here, inner_function() can access outer_var, which is from its enclosing scope.

5. **Global Scope (Module-Level Scope)**
- A variable declared outside any function is accessible throughout the script.

- **Example:**
```python
global_var = "Global"

def show():
    print(global_var)  # Accessible inside the function

show()  # Output: Global
print(global_var)  # Output: Global
```
- Here, global_var is globally available to all functions.

6. **Built-in Scope**
- Python has predefined functions and constants available anywhere in the program.

- **Example:**
```python
print(len("Python"))  # Output: 6
```
- Here, `len()` is a built-in function, accessible globally.

7. **Using the global Keyword**
- To modify a global variable inside a function, use the global keyword.

- **Example:**
```python
count = 0

def increment():
    global count  # Access the global variable
    count += 1

increment()
print(count)  # Output: 1
```
- Without `global`, modifying count inside `increment()` would cause an error.

8. **Using the nonlocal Keyword**
- To modify a variable from an enclosing scope inside a nested function, use nonlocal.

- **Example:**
```python
def outer():
    x = 10

    def inner():
        nonlocal x  # Accessing enclosing variable
        x += 5
        print(x)  # Output: 15

    inner()
    print(x)  # Output: 15

outer()
```
- Without nonlocal, x inside `inner()` would be treated as a new `local variable`.

**Outcome:**

- Understand function parameters, including positional, default, keyword, *args, and **kwargs.
- Learn how return values improve reusability by returning single/multiple values, lists, dictionaries, and functions.
- Master variable scope in Python using the LEGB rule (Local, Enclosing, Global, Built-in).
- Differentiate between local and global variables and use global and nonlocal keywords effectively.
- Learn the impact of function scope on data integrity and function independence.
- Improve code readability, maintainability, and debugging using structured functions.
- Use return values to build flexible, reusable functions in large projects
