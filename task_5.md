# Task 5: Other Data Types: Lists, Tuples, Dictionaries, and Sets

**Objective:**
- **Lists:** Ordered, mutable collection.
- **Tuples:** Ordered, immutable collection.
- **Dictionaries:** Key-value pairs.
- **Sets:** Unordered collection of unique items.

**Practice:**
- Create a list that stores different learning topics (e.g., `"Variables"`, `"Data Types"`, `"Control Flow"`, etc.).
- Create a tuple and a dictionary that represent elements of a mini project (e.g., feedback: `{ "topic": "Variables", "status": "Not Started" }`).
- Create a set that stores unique learning topics.


1. **Lists:**
- Lists are ordered collections of items that are mutable (can be changed).
- Lists are defined using square brackets `[]`.
- **Example:**
    ```python
    learning_topics = ["Variables", "Data Types", "Control Flow"]
    print("Learning Topics:", learning_topics)
    ```

**Advantages of Lists:**
- Mutable: Can be modified after creation.
- Dynamic: Can grow and shrink in size.
- Versatile: Can store items of different data types.

**Disadvantages of Lists:**
- Slower than tuples for iteration.
- Consumes more memory than tuples.

**Common List Methods:**
- `append()`: Adds an item to the end of the list.
    ```python
    learning_topics.append("Functions")
    print(learning_topics)  # Output: ["Variables", "Data Types", "Control Flow", "Functions"]
    ```
- `remove()`: Removes the first occurrence of an item.
    ```python
    learning_topics.remove("Data Types")
    print(learning_topics)  # Output: ["Variables", "Control Flow", "Functions"]
    ```
- `sort()`: Sorts the list in ascending order.
    ```python
    learning_topics.sort()
    print(learning_topics)  # Output: ["Control Flow", "Functions", "Variables"]
    ```

2. **Tuples:**
- Tuples are ordered collections of items that are immutable (cannot be changed).
- Tuples are defined using parentheses `()`.
- **Example:**
    ```python
    project_elements = ("Variables", "Data Types", "Control Flow")
    print("Project Elements (Tuple):", project_elements)
    ```

**Advantages of Tuples:**
- Immutable: More secure as they cannot be modified.
- Faster than lists for iteration.
- Consumes less memory than lists.

**Disadvantages of Tuples:**
- Immutable: Cannot be modified after creation.
- Less versatile than lists.

**Common Tuple Methods:**
- `count()`: Returns the number of times a specified value occurs in a tuple.
    ```python
    count = project_elements.count("Variables")
    print(count)  # Output: 1
    ```
- `index()`: Searches the tuple for a specified value and returns the position of where it was found.
    ```python
    index = project_elements.index("Control Flow")
    print(index)  # Output: 2
    ```

3. **Dictionaries:**
- Dictionaries are collections of key-value pairs.
- Dictionaries are defined using curly braces `{}` with keys and values separated by a colon `:`.
- **Example:**
    ```python
    feedback = {"topic": "Variables", "status": "Not Started"}
    print("Feedback (Dictionary):", feedback)
    ```

**Advantages of Dictionaries:**
- Fast lookups: Accessing elements by key is very fast.
- Flexible: Can store items of different data types.
- Dynamic: Can grow and shrink in size.

**Disadvantages of Dictionaries:**
- Unordered: Does not maintain the order of elements.
- Consumes more memory than lists and tuples.

**Common Dictionary Methods:**
- `keys()`: Returns a list containing the dictionary's keys.
    ```python
    keys = feedback.keys()
    print(keys)  # Output: dict_keys(['topic', 'status'])
    ```
- `values()`: Returns a list of all the values in the dictionary.
    ```python
    values = feedback.values()
    print(values)  # Output: dict_values(['Variables', 'Not Started'])
    ```
- `items()`: Returns a list containing a tuple for each key-value pair.
    ```python
    items = feedback.items()
    print(items)  # Output: dict_items([('topic', 'Variables'), ('status', 'Not Started')])
    ```

4. **Sets:**
- Sets are unordered collections of unique items.
- Sets are defined using curly braces `{}`.
- **Example:**
    ```python
    unique_topics = {"Variables", "Data Types", "Control Flow"}
    print("Unique Topics (Set):", unique_topics)
    ```

**Advantages of Sets:**
- Unique: Automatically removes duplicate items.
- Fast membership testing: Checking if an item is in a set is very fast.
- Dynamic: Can grow and shrink in size.

**Disadvantages of Sets:**
- Unordered: Does not maintain the order of elements.
- Cannot access elements by index.

**Common Set Methods:**
- `add()`: Adds an element to the set.
    ```python
    unique_topics.add("Functions")
    print(unique_topics)  # Output: {"Variables", "Data Types", "Control Flow", "Functions"}
    ```
- `remove()`: Removes a specified element.
    ```python
    unique_topics.remove("Data Types")
    print(unique_topics)  # Output: {"Variables", "Control Flow", "Functions"}
    ```
- `union()`: Returns a set containing the union of sets.
    ```python
    more_topics = {"Loops", "Conditions"}
    all_topics = unique_topics.union(more_topics)
    print(all_topics)  # Output: {"Variables", "Control Flow", "Functions", "Loops", "Conditions"}
    ```

5. **Practice:**
    ```python
    # Create a list that stores different learning topics
    learning_topics = ["Variables", "Data Types", "Control Flow", "Functions", "Loops"]
    print("Learning Topics:", learning_topics)

    # Create a tuple that represents elements of a mini project
    project_elements = ("Variables", "Data Types", "Control Flow", "Functions", "Loops")
    print("Project Elements (Tuple):", project_elements)

    # Create a dictionary that represents feedback for a mini project
    feedback = {"topic": "Variables", "status": "Not Started"}
    print("Feedback (Dictionary):", feedback)

    # Create a set that stores unique learning topics
    unique_topics = {"Variables", "Data Types", "Control Flow", "Functions", "Loops"}
    print("Unique Topics (Set):", unique_topics)
    ```

**Outcome:**
- Understand how to create and use lists, tuples, dictionaries, and sets in Python.
- Learn the differences between lists, tuples, dictionaries, and sets.
- Perform common operations on lists, tuples, dictionaries, and sets.
- Understand the use cases for lists, tuples, dictionaries, and sets.
- Know the advantages and disadvantages of each data type.
