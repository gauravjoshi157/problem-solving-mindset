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
    
