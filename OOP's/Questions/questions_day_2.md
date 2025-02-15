# Question1: What is overloading. Does python support overloading?
**Explanation**
- Overloading happen when same name is used to create multiple methods which takes different parameters.
- Overloading has two types:
    - Method Overloadnig
    - Operator Overloading
- Python does not support method overloading but it can be achieved by `default arguments`, `*args`, `**kwargs` and `@staticmethod

**Method Overloadign:**
- Method overloading term refer that same name is used to create multiple methods that can accept different parameters.
- In python we can use method overloading by the following ways:
    - Using `default arguments:`
    ```python
    class Example:
        def show( self,a = None, b = None):
            if a is not None and b is not None:
                print("Two parameter",a,b)

            elif a is not None:
                        print("One argument",a)
            else:
                        print("No arguments")      
    obj = Example()
    obj.show()      # No arguments
    obj.show(20)    # One argument 20
    obj.show(20,30) # Two parameter 20 30
    ```
    
    - Using `*args`, `**kwargs`:
    ```python
    class Example:
    def show( self, *args):
        print("Arguments Passed", args)
            
    obj = Example()
    obj.show()      # No argument
    obj.show(20)    # One argument
    obj.show(20,30) ## Two parameter
    ```

    - Using `@staticmethod`:
    ```python
    class Example:
    @staticmethod
    def add(a, b = 0, c = 0):
        return a+b+c

    print(Example.add(10))     # One argument
    print(Example.add(10,20))    # Two arguments
    print(Example.add(10,20,30)) # Three arguments
    ```

# Question 2: Create methods inside class and use it via object.
```  
# Creatine methods inside the class

class Methametics:
    def __init__(self, number1, number2):
        self.number1 = number1
        self.number2 = number2

    def add(self):
        return (f"The sum of {self.number1} and {self.number2} is {self.number1 + self.number2}")
    
    def subtract(self):
        return (f"The subtraction of {self.number1} and {self.number2} is {self.number1 - self.number2}")
    
    def multiply(self):
        return (f"The multiply of {self.number1} and {self.number2} is {self.number1 * self.number2}")
    
    def divide(self):
        return (f"The divide of {self.number1} and {self.number2} is {self.number1 / self.number2}")
    
numbers = Methametics(45, 5)
numbers.__dict__
print(numbers.add())
print(numbers.subtract())
print(numbers.multiply())
print(numbers.divide())
```
# Question 2: Creating functions outside the class and using them inside the class.
```
# Using outside function inside the class 
def add(a,b):
        return (f"The sum of {a} and {b} is {a + b}")
    
def subtract(a,b):
        return (f"The subtraction of {a} and {b} is {a - b}")
    
def multiply(a,b):
        return (f"The multiply of {a} and {b} is {a * b}")
    
def divide(a,b):
        return (f"The divide of {a} and {b} is {a / b}")


class Methametics:
        def __init__(self, number1, number2):
                self.number1 = number1
                self.number2 = number2
        def calculation(self):
                print(add(self.number1, self.number2))
                print(subtract(self.number1, self.number2))
                print(multiply(self.number1, self.number2))
                print(divide(self.number1, self.number2))


nums = Methametics(45,5)    
nums.calculation()
```