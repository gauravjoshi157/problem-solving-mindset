# Task 3: Variables & Basic Data Types (Numbers & Strings)

**Objective:**
- Understand variables and how they store data.
- Learn about integer (int), floating-point (float), and string (str) data types.

**Practice:**
- Create a variable `college_problem` to store the description of your mini project.
- Perform arithmetic operations with numbers and observe the output.

1. **Variables:** 
- Variables are containers that store a value.
- Python does not require explicit declaration of a variable. The data type of the variable is defined automatically based on the assigned value.
- Rules for Naming Variables:
    - Start with a letter (a-z, A-Z) or an underscore (_).
    - Can contain letters, numbers (0-9), or underscores after the first character.
    - No spaces.
    - Case-sensitive (e.g., age, Age, AGE are different).
    - Cannot be a reserved keyword (like if, while, for).
- **Example:** `variable_name = "value"`

2. **Basic Data Types:**
    1. **Numbers**: Python contains two main types of numbers:
    - **Integer:** Integers are whole numbers without any decimal. Ex: `5`, `10`, etc.
    - **Float:** Floats are decimal numbers. Ex: `5.0`, `10.5`, etc.
    2. **String:** A string is a collection of characters. Ex: `"HELLO"`.
    - Strings can be defined inside single quotes `'...'` or double quotes `"..."`.

3. **Practice:**
    ```python
    # Createing a variable 'college_problem' and store the description of mini project.
    college_problem = "In india, the most of the colleges are profit oriented and do not have focus on the learning. This mini project help us to solve this problem."

    # Perform Arithmetic Operations (Integer and Float support similiar operations but if you mix integer with float then hte ouput automatically turn into float)
    x = 15
    y = 4 

    # Addition
    sum_result = x + y
    print("Addition:", sum_result)   # Expected Output: 19

    # Subtraction
    diff_result = x - y
    print("Subtraction:", diff_result)  # Expected Output: 11

    # Multiplication
    prod_result = x * y
    print("Multiplication:", prod_result)  # Expected Output: 60

    # Division (float result)
    div_result = x / y
    print("Division:", div_result)  # Expected Output: 3.75

    # Floor Division (integer result)
    floor_div_result = x // y
    print("Floor Division:", floor_div_result)  # Expected Output: 3

    # Modulus (remainder)
    mod_result = x % y
    print("Modulus:", mod_result)  # Expected Output: 3
    ```

**Outcome:**
- Understand how to declare and use variables in Python.
- Learn the basic data types: integers, floats, and strings.
- Understand the rules for naming variables.
- Gain familiarity with string manipulation and operations.
