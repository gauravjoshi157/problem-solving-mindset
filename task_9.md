# Task 9: Loops – While Loop

- **Objective:**
    - Run a loop as long as a condition is true.

- **Practice:**
    - Use a counter variable to write a while loop that runs until user input is received.
    - Implement a "menu loop" in a mini project.

**What is a While Loop?**
A `while` loop repeatedly executes a block of code as long as a given condition is true. It is useful when the number of iterations is not known beforehand and depends on some runtime condition.

**Syntax:**
```python
while condition:
    # Code to execute
```

**1. Basic While Loop:**
- A simple example of a while loop that runs as long as a counter variable is less than 5.

**Example:**
```python
counter = 0

while counter < 5:
    print(f"Counter is at {counter}")
    counter += 1
```
**Output:**
```python
Counter is at 0
Counter is at 1
Counter is at 2
Counter is at 3
Counter is at 4
```
**2. Using a While Loop to Wait for User Input:** 
- A while loop can be used to repeatedly prompt the user for input until a specific condition is met.

**Example:**
```python
user_input = ""

while user_input.lower() != "exit":
    user_input = input("Enter something (type 'exit' to quit): ")
    print(f"You entered: {user_input}")
```
**Output:**
```python
Enter something (type 'exit' to quit): hello
You entered: hello
Enter something (type 'exit' to quit): exit
You entered: exit
```
**3. Implementing a Menu Loop:** ```python
- A common use case for a while loop is to create a menu that allows users to select options until they choose to exit.

**Example:**
```python
def display_menu():
    print("Menu:")
    print("1. Option 1")
    print("2. Option 2")
    print("3. Exit")

choice = 0

while choice != 3:
    display_menu()
    choice = int(input("Enter your choice: "))
    
    if choice == 1:
        print("You selected Option 1.")
    elif choice == 2:
        print("You selected Option 2.")
    elif choice == 3:
        print("Exiting the menu.")
    else:
        print("Invalid choice. Please try again.")
```
**Output:**
```python
Menu:
1. Option 1
2. Option 2
3. Exit
Enter your choice: 1
You selected Option 1.
Menu:
1. Option 1
2. Option 2
3. Exit
Enter your choice: 2
You selected Option 2.
Menu:
1. Option 1
2. Option 2
3. Exit
Enter your choice: 3
Exiting the menu.
```
**4. Using continue and break Statements in While Loops:**
- The continue statement skips the rest of the code inside the loop for the current iteration and moves to the next iteration. The break statement exits the loop entirely.

**Example:**
```python
counter = 0

while counter < 10:
    counter += 1
    if counter == 3:
        print(f"Skipping number {counter} using continue statement.")
        continue  # Skip the rest of the code inside the loop for this iteration
    if counter == 7:
        print(f"Breaking the loop at number {counter} using break statement.")
        break  # Exit the loop when counter is 7
    print(f"Current counter is {counter}")
```
**Output:**
```pythonCurrent counter is 1
Current counter is 2
Skipping number 3 using continue statement.
Current counter is 4
Current counter is 5
Current counter is 6
Breaking the loop at number 7 using break statement.
```
**5. Advantages of While Loops:**
- Useful when the number of iterations is not known beforehand.
- Can handle dynamic conditions that change during execution.

**6. Disadvantages of While Loops:**
- Risk of creating infinite loops if the condition is never met.
- Can be less readable if the loop logic is complex.

**7. Common Use Cases:**
- Waiting for user input.
- Implementing menus and interactive programs.
- Repeating tasks until a condition is met.

**8. Practice:**
- Use a while loop to create a simple counter that increments until it reaches a specified value.
```python
counter = 0
limit = 5

while counter < limit:
    print(f"Counter is at {counter}")
    counter += 1
```
**9. Implement a Menu Loop in a Mini-Project:**
- Create a menu-driven program that allows users to select options until they choose to exit.

```python
def display_menu():
    print("Menu:")
    print("1. Collect Data")
    print("2. Process Data")
    print("3. Analyze Results")
    print("4. Generate Report")
    print("5. Exit")

choice = 0

while choice != 5:
    display_menu()
    choice = int(input("Enter your choice: "))
    
    if choice == 1:
        print("Collecting Data...")
    elif choice == 2:
        print("Processing Data...")
    elif choice == 3:
        print("Analyzing Results...")
    elif choice == 4:
        print("Generating Report...")
    elif choice == 5:
        print("Exiting the menu.")
    else:
        print("Invalid choice. Please try again.")
```
**Output:**
```python
Menu:
1. Collect Data
2. Process Data
3. Analyze Results
4. Generate Report
5. Exit
Enter your choice: 1
Collecting Data...
Menu:
1. Collect Data
2. Process Data
3. Analyze Results
4. Generate Report
5. Exit
Enter your choice: 5
Exiting the menu.
```
**10. Outcome:**
- Learn how to use the while loop in Python.
- Understand how to create interactive programs using loops.
- Apply loops in practical contexts, such as menu-driven applications.
- Understand the use of continue and break statements in loops.
