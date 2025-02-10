# Task 8: Loops – For Loop
- **Objective:**
    - Iterate through lists or iterable objects.

- **Practice:**
    - Use a for loop to iterate through a list of learning topics and print each topic.
    - Implement iteration for topics in a mini project.


**What is a For Loop?**
A `for` loop is used to iterate over a sequence (such as a list, tuple, dictionary, or string) and execute a block of code for each item in the sequence.

 **Syntax:**
```python
for variable in iterable:
    # Code to execute
```

**1. Iterating Through a List:**
The most common use of a `for` loop is to iterate through a list.

**Example:**
```python
learning_topics = ["Variables", "Data Types", "Control Flow", "Functions"]

for topic in learning_topics:
    print(topic)
```
**Output:**
```
Variables
Data Types
Control Flow
Functions
```

**2. Iterating Through a Range of Numbers:**
The `range()` function is commonly used in loops to generate a sequence of numbers.

**Example:**
```python
for i in range(5):  # Iterates from 0 to 4
    print(i)
```
**Output:**
```
0
1
2
3
4
```

**3. Iterating Through a Dictionary:**
Dictionaries store key-value pairs, and we can loop through them.

**Example:**
```python
project_feedback = {
    "Variables": "Completed",
    "Data Types": "In Progress",
    "Control Flow": "Not Started"
}

for key, value in project_feedback.items():
    print(f"{key}: {value}")
```
**Output:**
```
Variables: Completed
Data Types: In Progress
Control Flow: Not Started
```

**4. Using `continue` and `break` Statements:**
-The `continue` statement skips the rest of the code inside the loop for the current iteration and moves to the next iteration. The `break` statement exits the loop entirely.

**Example:**
```python
numbers = list(range(10))

for number in numbers:
    if number == 3:
        print(f"Skipping number {number} using continue statement.")
        continue  # Skip the rest of the code inside the loop for this iteration
    if number == 7:
        print(f"Breaking the loop at number {number} using break statement.")
        break  # Exit the loop when number is 7
    print(f"Current number is {number}")
```
**5. Advantages of For Loops:**
- Simplifies iteration over sequences.
- Reduces redundancy in code.
- Improves readability.

**6. Disadvantages of For Loops:**
- Can be less efficient than `while` loops when conditions depend on computations.
- Overuse may lead to unnecessary iterations.

**7. Common Use Cases**
- Iterating through lists and dictionaries.
- Processing data in loops.
- Automating repetitive tasks.

**8. Practice:**
Use a for loop to iterate through a list of learning topics and print each topic.

```python
learning_topics = ["Variables", "Data Types", "Control Flow", "Functions", "Loops"]

for topic in learning_topics:
    print("Learning Topic:", topic)
```

**9. Implement iteration for topics in a mini-project:**
```python
project_tasks = ["Collect Data", "Process Data", "Analyze Results", "Generate Report"]

print("Project Workflow:")
for task in project_tasks:
    print(f"- {task}")
```

**Expected Output:**
```
Learning Topic: Variables
Learning Topic: Data Types
Learning Topic: Control Flow
Learning Topic: Functions
Learning Topic: Loops

Project Workflow:
- Collect Data
- Process Data
- Analyze Results
- Generate Report
```

**10. Outcome:**
- Learn how to use the `for` loop in Python.
- Understand how to iterate over lists, dictionaries, and sequences.
- Apply loops in a practical context, such as mini-project tasks.

