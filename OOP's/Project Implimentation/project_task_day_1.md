# Task 1
- Create a simple class (like LearningModule) with basic attributes (module_name, status).
- Create an object, access its attributes, and modify them.

- Attributes:
    - `module_name (str)`: Name of learning topic .
    - `status (str)`: Current status of the module (default: "Not Started").
- Methods:
    - `display_info()`: Print the details of the module.
    - `update_status(new_status)`: Update the status of the module.
```
# Creating LearningModule class and assigning attributes(module name, status)

class LearningModule:
    # Using __init__ constructer to initialize the instance.
    def __init__(self, module_name, status = "Not Started"):
        self.module_name = module_name
        self.status = status
    
    # Creat a method to displaying the information of the module  
    def display_info(self):
        print(f"Module:{self.module_name} | Status:{self.status}")

    # Crete a method to update the status of the module.
    def update_status(self, new_status):
        self.status = new_status
        print(f"Status of {self.module_name} successfully updated to: {self.status}")

# Creating object of the learningModule class
user1 = LearningModule("Variables")

# Use display_info method for getting the information 
user1.display_info()

# Update the status of the module
user1.update_status("Completed")

# Again displaying the info of the module
user1.display_info()
```