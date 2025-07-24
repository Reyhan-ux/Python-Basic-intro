
### **Introduction into Python By Reyhan Ebai*

This is a brief notebook covering all the core programming concepts with clear examples.


### **Key Topics Covered*
- Input/Output operations
- Data types & variables
- Control flow & loops
- Functions & error handling
- Data structures & a final project

## **Section 1: Input & Output*

### Key Skills
- Capture user input with `input()`  
- Display output using `print()`  
- Format strings with f-strings
- Manage different input types  

**Example 1: Basic Input/Output**  
  ``python  
user_name = input("Enter your name: ")  
print("Hello, World!")  
print("Welcome, " + user_name + "!")  
 ``

**Example 2: F-Strings (Formatted Strings)**
`python  
name = "Alex"  
print(f"Hello, {name}!")  # Cleaner than concatenation  
`  

**F-Strings vs. Concatenation*  
- **Concatenation**: Manual type conversion required.  
  `python  
  age = 30  
  print("Age: " + str(age))  # Explicit conversion  
  ` 
- **F-Strings**: Automatic conversion.  
  `python  
  print(f"Age: {age}")  # No conversion needed  
  `
--
## **Section 2: Data Types* 

Python supports multiple built-in data types:  
- *Text*: `str`  
- *Numeric**: `int`, `float`, `complex`  
- *Sequences*: `list`, `tuple`, `range`  
- *Mappings*: `dict`  
- *Sets*: `set`, `frozenset`  
- *Boolean*: `bool`  
- *Binary*: `bytes`, `bytearray`, `memoryview`  
- *None*: `NoneType`  

**Example: Type Checking**  
`python  
x = 10          # Integer  
y = 3.14        # Float  
z = "Python"    # String  
print(type(x))  # Output: <class 'int'>  
` 

**Type Casting**  
Convert between types using constructors:  
`python  
num_str = str(100)          # "100"  
num_int = int("50")         # 50  
num_float = float("3.14")   # 3.14  
`  
--
## **Section 3: Variables & Naming Rules*  

### **Variable Assignment**  
No explicit declaration needed—just assign a value:  
`python  
score = 95        # Integer  
pi = 3.14159      # Float  
language = "Python"  
`  

### **Naming Conventions**  
- **Valid**: Starts with a letter/underscore (`_`), contains letters/numbers/underscores.  
  - `user_age`, `total_count`, `_temp`  
- **Invalid**: Starts with a number or uses special characters.  
  - `2nd_place`, `user-name`  
- **Case-sensitive**: `name ≠ Name ≠ NAME`.  

--

## **Section 4: Indentation & Comments*  

### **Indentation**  
Python uses whitespace (tabs/spaces) to define code blocks:  
`python  
if score > 70:  
    print("Passed!")  # Indented block  
`  

### **Comments*
- **Single-line**:  
  `python  
  # This is a comment  
  `  
- **Multi-line**:  
  `python  
  """  
  This is a  
  multi-line comment  
  """  
  `
--- 

**Next Steps**: Control flow, loops, and functions