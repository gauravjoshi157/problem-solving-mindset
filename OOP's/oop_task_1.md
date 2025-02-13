# Object Oriented Programming

### Class
- `Class` is the blueprint which defines the properties(`attributes`) and behaviour(`method`es) of the objects.
- `Class` follows OOP's concepts which make the code more maintainable, scalable, ,modular reusable.
- It is Very benificary if the `class` use Single Responsibility Principle.It increases maintability and make debugging easy.
- We can define a `class` with `class` keyword.
- `Class`t stores data(`attributes` and `method`s) in `Class.__dict__` which is called `Class` Dictionary.
- `Class` does not occupy memory untill an object is created.(`Class` is partially compile time and partially runtime)
- Syntax of creating a `class`:
```python
class ClassName:
    # The attributes and methods are written inside class body.
```

- Question: Can we define a `class` without the `class` keyword?
- **Answer:** Yes! We can create a `class` without `class` keyword by using type() dynamically.
    - Syntax of type()
    ```python
    type(class_name, base_classes, attributes)
    ```
    - We can also use Meta`class` to generate and modify `class` at runtime.
    - type() create `class` in runtime and dynamically.
    - `Class`es created by `class` keyword are better in readability and make the code clean and classes created by type() 


### Objects:
- Objects is a instance of `class`.
- When a object is created, it is the actual implimentation of that `class`.
- Object Stores data(`attributes`) in `obj.__dict__` which is called Instance Dictionary/Object Dictionary.


### `Attributes`:
- `Attributes` are the variables stored within an ibject.
- `Attributes` defines the state of object.
- `Attributes` has two types:
    - Instance `Attributes`
    - `Class` `Attributes`:
- **Question:** What is the differece between Instance `Attributes` and `Class` `Attributes`.
- **Answer:** `Class` Variable vs. Instance Variable

| Feature       | `Class` Variable                                   | Instance Variable                                     |
|---------------|----------------------------------------------------|------------------------------------------------------|
| **Definition** | Defined at the `class` level                       | Defined inside the ``__init__`` `method`                   |
| **Scope**      | Shared among all objects of the `class`           | Unique to each object of the `class`                     |
| **Accessed Using** | `ClassName.variable` or `object.variable`     | `self.variable` (inside `class`) or `object.variable`   |
| **Stored In**   | `ClassName.__dict__`                             | `object.__dict__`                                      |
| **Modification**| Affects all objects if changed via ``Class`Name.variable` | Affects only that specific object                |
| **When to Use?**| When the value should be common for all instances | When each instance should have a unique value          |

### Method:
- `Method` define the behaviour of the `class`.
- The difference between functions and `method` is very minor. When we make function inside a `class`, the terminology we use is `method`.
- All the other things are same as function.

### Constructor:
- Constructer is a special `method` which is automatically called whenever a new `class` object is created.
- In python the constructor is defined using `__init__` `method`.
```python
class ClassName:
    def __init__(self, parameters):
        # Initialize attributes
```
- `__init__` is a reserved `method` name.
- self is a reference to current instance of the `class`.
- parameters are used to initialize obejct attribute.
- **Question:** We know _init_ constructor used for initialize the object `attributes` and what happens when we don't use this init constructor?
- **Answer:** Yes! Python will allow object creation without using `__init__` constructor but the `attributes` must be assigned manually.`__init__` ensure attribute to initialize at the creation
    - When we creat a object without `__init__` then we have to manually assign the `attributes` every time we create a new object. This process will take time and make our code complex.
- **Question:** What happen if we did not use self in  `__init__`?
- **Answer:** If we do not give self inside `__init__` then nothing will happen special. Python will treat the first parameter as self.
    - This is wrong implimentation of code because of the wrong naming convensions which leads error and confusion in collaberations.
    - This will give TypeError.


