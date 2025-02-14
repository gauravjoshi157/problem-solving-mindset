# Qeustion1: Can we define a `class` without the `class` keyword?

Yes! We can create a `class` without `class` keyword by using type().It creats `class` dynamically.
- Syntax of type()
```python
type(class_name, base_classes, attributes)
```
- We can also use Meta`class` to generate and modify `class` at runtime.
- type() create `class` in runtime and dynamically.
- `Class` created by `class` keyword are better in readability and make the code clean and classes created by type().
# Question 2: What is the differece between Instance `Attributes` and `Class` `Attributes`.

`Class` Variable vs. Instance Variable:

| Feature       | `Class` Variable                                   | Instance Variable                                     |
|---------------|----------------------------------------------------|------------------------------------------------------|
| **Definition** | Defined at the `class` level                       | Defined inside the ``__init__`` `method`                   |
| **Scope**      | Shared among all objects of the `class`           | Unique to each object of the `class`                     |
| **Accessed Using** | `ClassName.variable` or `object.variable`     | `self.variable` (inside `class`) or `object.variable`   |
| **Stored In**   | `ClassName.__dict__`                             | `object.__dict__`                                      |
| **Modification**| Affects all objects if changed via ``Class`Name.variable` | Affects only that specific object                |
| **When to Use?**| When the value should be common for all instances | When each instance should have a unique value          |
# Question 3: We know `__init__` constructor used for initialize the object `attributes` and what happens when we don't use this init constructor?

- Yes! Python will allow object creation without using `__init__` constructor but the `attributes` must be assigned manually.`__init__` ensure attribute to initialize at the creation
- When we creat a object without `__init__` then we have to manually assign the `attributes` every time we create a new object. This process will take time and make our code complex.
# Question 4: What happen if we did not use self in  `__init__`?
- If we do not give self inside `__init__` then nothing will happen special. Python will treat the first parameter as self.
- This is wrong implimentation of code because of the wrong naming convensions which leads error and confusion in collaberations.
- This will give TypeError.
# Question 5: Why we are making methods in every class if I want to use addition so I made a addition function and why don't I use that function in the class ? it takes less memory space and also fasten the program.
- When we make method it defines the behaviour of that class and become a part of it.
- If we have multiple related operations, keeping them inside a class make it easier to manage.
- We can use outside function inside a class. It make easier to use the function via multiple classes. 
- Use an external function if:

    - The function is stateless (does not depend on any object attributes).
    - The function will be reused frequently (even across different classes).
    - You want to optimize performance and memory.

- Use a method inside a class if:

    - The function depends on the object's state (attributes).
    - The function is only relevant to that specific class.
    - You want to follow encapsulation and object-oriented design principles.

# Question 6: Does `__init__` are actually constructor and what is meaning of double underscore in this?

**__init__:**
- Yes! In Python, `__init__` is called a constructor, but it is not a true constructor like in C++ or Java.
- Instead of creating an object, `__init__` only initializes an already created object.
- In Python, objects are created first (`__new__`), then `__init__` initializes them.
    - Calls `__new__()` → Allocates memory for the object.
    - Calls `__init__()` → Initializes the object's attributes.

**Double Underscore:**
- The double underscore (`__init__`) makes it a special (`dunder`) method, meaning:
- It is built-in and automatically called by Python.
- It is not meant to be called manually.
- It prevents naming conflicts with user-defined methods.
# Question 7: What will happen when we assign one object to another object?

- When we assign an object to another object they share the same memory address and refer to the same object.
- After assigning an object to another object if we modify the value of one object, the value of other object also modifies because of the refer to same value.
```python
# Create a sample class
class Sample:
    def __init__(self, value):
        self.value = value

# Creat two object
obj1 = Sample(10)
obj2 = obj1

# Print object values
print(obj1.value)
print(obj2.value)
 
# Modifying one object
obj2.value = 20

# Print after modifying
print(obj1.value)
print(obj2.value)
```
# Question 8: For calling an object we need (.) operator why we are using (.), can we call the object using parantheses().
- The dot operator is the syntax used to access the members of an object.
- object.member means "access the member (attribute or method) named member that belongs to the object object."
- It explicitly bind attributes to instance.
- 
- You cannot call an object using () directly unless the class defines a __call__() method.
```python
class Person:
    def __init__(self, name):
        self.name = name
    
    def __call__(self):
        return f"Hello, {self.name}!"

# Create an object
p = Person("Alice")

# Call the object like a function
print(p())  # ✅ Output: Hello, Alice!

```
- To call object by using () we have to create call function but it make code complex so it is better to use `.` for calling an object.
# Question 9:What happen if we don't write object in class or can we write multiple objects in one class. Does object is only using for creating instance of class or we can do more things with objects?
- If we define a class but do not create any object then:
    - The class exists in memory, but it doesn’t execute any code inside `__init__()` because no instance is created.
    - No attributes or methods of the class can be used unless they are class methods or static methods.
- Yes we can create multiple object of a class and eact object have its own data which stored in `__dict__`.  
- The object can be used for various purposes like:
    - Encapsulation → Storing both data (attributes) and behavior (methods).
    - Reusability → The same class can create multiple objects with different values.
    - Interacting with Other Objects → Objects can communicate with other objects.
# Question 10: Does class is compulsory to create object in python?
- In pyhton, whether it's a function or a variable everything is considered as a object.
- Class is not compulsory to create a object.
```python
x = 40
y = 'a'
```
# Question 11: Can you create an instance of a class without providing attributes?
- Yes! We can create a class whithout creating or defining attributes.
- We can create a class only defining methods.
```python
class Example:
    def show(self):
        return "Hello, I have no attributes!"

obj = Example()
print(obj.show())  # Output: Hello, I have no attributes!
```

- We can also create empty class which store the memory and we can use it in future.
```python
class Placeholder:
    pass  # Placeholder for future code

obj = Placeholder()
print(obj)  # Output: <__main__.Placeholder object at 0x...>
```

# Question 12: If we create multiple instances, it increase memory overhead so what we have to do to avoid this.
- When we create multiple instances, with every instances a `__dict__`  also created which allocates memory. Which leads to memory overhead.
- We can reuse objects instead of creating new object if possible.
- We can use `__slot__` to prevent creating `__dict__` for each object which save memory.
```python
class Example:
    __slots__ = ['name', 'age']  # Limits attributes, reduces memory usage

    def __init__(self, name, age):
        self.name = name
        self.age = age

obj1 = Example("Alice", 25)
obj2 = Example("Bob", 30)
```
- We can also use class variable instead of instance variable for pre-instance.
```python
class Example:
    class_variable = [] # It is a class variable which is shared among all methods

    def __init__(self, name):
        self.name = name    # It is an instance variable
```
    
# Question 13: Does a class get stored in memory even before we create an object?
- Yes! when we define a class python will compile the code and assign the memory to a class
- Python consider everything as objects and class is also a object of `type` that's why it store in memory without even creating an object.
- But instance attribute is only created  when a object is initiated.

# Question 14: What is instance dictionary?
- An instance dictionary(`__dict__`) is a built-in Python attribute that store instance specific attributes in dictionary format.
- `__dict__` dynamically store and update memory at runtime.
- We can use `__slot__` which stop instances to create their own `__dict__`.
 
# Question 15: How we can ensure taht a attribute only be accessed inside a class?
- To preventing use of attributes outside a class we can use double underscore `__`
- By using double underscore `__`   before a attribute name we can make the attribute private. This is called `Name Mangling`.
- Python doesn't have true private attributes, but name mangling renames `__var` to `_ClassName__var`, making accidental access harder.
- Private attributes can still be used outside the class using class methods.
```python
class Example:
    def __init__(self):
        self.__secret = "Hidden Message"  # Private attribute

    def reveal(self):
        return self.__secret  # Can be accessed inside class

obj = Example()

# Accessing inside the class works
print(obj.reveal())  # Output: Hidden Message

# Direct access will raise an error
print(obj.__secret)  # AttributeError
```
