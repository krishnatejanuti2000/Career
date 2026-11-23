# **Python – Complete Interview Questions & Answers**

# **Section 1 – Python Fundamentals**

### **Q1. What is Python? Explain its features, advantages and common applications.**

**Answer:**

Python is a high-level, interpreted, general-purpose programming language.

It is known for its simple syntax and readability.

Python supports both Procedural Programming and Object-Oriented Programming.

**Features of Python:**

1. **Simple Syntax:** Python code is easy to read and understand.
2. **Interpreted Language:** Python code is executed through the Python execution environment.
3. **Dynamically Typed:** We do not need to declare variable data types explicitly.
4. **Cross-Platform:** Python supports different operating systems.
5. **Object-Oriented:** Python supports classes and objects.
6. **Large Collection of Modules:** Python provides built-in and external modules.
7. **Code Reusability:** We can write reusable functions and modules.

**Advantages:**

- Easy to learn.
- Readable code.
- Cross-platform support.
- Large library ecosystem.
- Code reusability.
- Useful for automation and testing.

**Applications:**

- Application testing.
- Website testing.
- Storage testing.
- Test automation.
- System administration.
- Data processing.
- Web development.

### **Q2. How does Python execute a program? Explain the role of the Python Interpreter, Bytecode and Python Virtual Machine (PVM).**

**Answer:**

Python executes a program through its interpreter and runtime environment.

The general execution flow is:

```
Python Source Code
       |
       v
Python Interpreter
       |
       v
Compilation to Bytecode
       |
       v
Python Virtual Machine
       |
       v
Program Execution
       |
       v
     Output
```

**1. Python Source Code:**

We write Python instructions in a `.py` file.

**2. Python Interpreter:**

The interpreter reads and processes the Python source code.

**3. Bytecode:**

Python converts the source code into bytecode instructions.

Bytecode is an intermediate representation of the program.

**4. Python Virtual Machine (PVM):**

PVM is the runtime engine that executes Python bytecode instructions.

**5. Output:**

After execution, the program produces the required output.

### **Q3. What is the difference between a Compiler and an Interpreter? Is Python a compiled or interpreted language?**

**Answer:**

**Compiler:**

A compiler translates a program into machine code before execution.

It generally processes the complete program before producing the executable output.

**Interpreter:**

An interpreter executes program instructions through an interpreter runtime.

It commonly reports errors during execution as the relevant code is processed.

**Difference:**

| Compiler                                                            | Interpreter                                           |
| ------------------------------------------------------------------- | ----------------------------------------------------- |
| Translates the program into machine code or another executable form | Executes source code through an interpreter runtime   |
| Compilation occurs before program execution                         | Interpretation/execution occurs at runtime            |
| Compiled output can be executed separately                          | Commonly requires an interpreter runtime              |
| Examples: C and C++ compilation workflows                           | Python and traditional interpreted-language workflows |

**Is Python compiled or interpreted?**

Python is commonly described as an interpreted language.

However, Python also performs a compilation step.

In the standard CPython implementation:

1. Python source code is compiled into bytecode.
2. The Python Virtual Machine executes the bytecode.

Therefore, Python has both compilation and interpretation stages.

### **Q4. What is Dynamic Typing in Python? Do we need to declare variable data types explicitly?**

**Answer:**

Dynamic Typing means we do not need to declare the data type of a variable explicitly.

Python determines the data type at runtime based on the assigned value.

**Example:**

```
x = 100print(type(x))# <class 'int'>x = "Python"print(type(x))# <class 'str'>x = 10.5print(type(x))# <class 'float'>
```

Here, the same variable name is assigned different types of values.

Python automatically identifies the type.

### **Q5. What are Procedural Programming and Object-Oriented Programming? How does Python support both?**

**Answer:**

Python supports different programming approaches.

**1. Procedural Programming:**

Procedural Programming is a programming approach in which we divide the program into functions.

The functions perform specific operations.

Example:

```
def add(a, b):    return a + bresult = add(10, 20)print(result)
```

**2. Object-Oriented Programming:**

Object-Oriented Programming is a programming approach based on classes and objects.

We create classes containing attributes and methods.

Example:

```
class Student:    def display(self):        print("Student Details")obj = Student()obj.display()
```

**Difference:**

| Procedural Programming                  | Object-Oriented Programming    |
| --------------------------------------- | ------------------------------ |
| Based on functions                      | Based on classes and objects   |
| Focuses on procedures                   | Focuses on objects             |
| Uses functions to organize code         | Uses attributes and methods    |
| Suitable for simple structured programs | Useful for larger applications |

Python supports both approaches.

### **Q6. What are Interactive Mode and Script Mode in Python? Explain their differences.**

**Answer:**

There are two ways to execute Python programs.

**1. Interactive Mode:**

Interactive Mode allows us to execute Python statements directly in the Python interpreter.

Example:

```
>>> x = 10>>> print(x)10
```

The output is displayed immediately.

**2. Script Mode:**

In Script Mode, we write Python code in a `.py` file and execute it.

Example file: `test.py`

```
x = 10y = 20print(x + y)
```

Execution:

```
python test.py
```

**Difference:**

| Interactive Mode                 | Script Mode                    |
| -------------------------------- | ------------------------------ |
| Executes statements directly     | Executes code stored in a file |
| Immediate output                 | Executes the script            |
| Useful for small experiments     | Useful for complete programs   |
| No separate script file required | Requires a `.py` file          |

### **Q7. What are comments and docstrings in Python? What are the different ways of writing comments?**

**Answer:**

Comments are used to explain code.

Python ignores comments during normal program execution.

**Single-Line Comment:**

We use the `#` symbol.

```
# This is a single-line commentx = 100
```

**Multiple-Line Comments:**

We can write multiple comment lines using `#`.

```
# This is line one# This is line two# This is line three
```

**Docstrings:**

Docstrings are documentation strings used to describe functions, classes and modules.

They are commonly written using triple quotes.

```
def add(a, b):    """    This function adds two numbers.    """    return a + b
```

To access the function documentation:

```
print(add.__doc__)
```

# **Section 2 – Data Types, Type Conversion and Operators**

### **Q8. What are the different built-in data types in Python? Explain int, float, string, boolean, list, tuple, set and dictionary.**

**Answer:**

Data types define the type of data stored in a variable.

The important built-in data types in my notes are:

**1. Integer (**`int`**):**

Stores whole numbers.

```
x = 100
```

**2. Float (**`float`**):**

Stores decimal numbers.

```
x = 10.5
```

**3. String (**`str`**):**

Stores a sequence of characters.

```
name = "Python"
```

**4. Boolean (**`bool`**):**

Stores either `True` or `False`.

```
status = True
```

**5. List (**`list`**):**

Stores multiple elements in square brackets.

```
values = [10, 20, 30]
```

Lists are mutable and ordered.

**6. Tuple (**`tuple`**):**

Stores multiple elements in parentheses.

```
values = (10, 20, 30)
```

Tuples are immutable and ordered.

**7. Set (**`set`**):**

Stores unique elements.

```
values = {10, 20, 30}
```

Sets are mutable and do not support indexing.

**8. Dictionary (**`dict`**):**

Stores data in key-value pairs.

```
student = {    "name": "John",    "age": 25}
```

### **Q9. What are Mutable and Immutable data types? Explain with examples.**

**Answer:**

**Mutable:**

Mutable data types allow us to modify their contents after creating them.

Examples:

- List.
- Dictionary.
- Set.

Example:

```
list1 = [10, 20, 30]list1[0] = 100print(list1)# [100, 20, 30]
```

**Immutable:**

Immutable data types cannot be modified after creation.

Examples:

- Integer.
- Float.
- String.
- Tuple.
- Boolean.

Example:

```
str1 = "Python"str1 = str1 + " Programming"print(str1)# Python Programming
```

The original string was not modified. A new string was created and assigned to the variable.

**Difference:**

| Mutable                         | Immutable                                  |
| ------------------------------- | ------------------------------------------ |
| Can be modified after creation  | Cannot be modified after creation          |
| Contents can change             | New objects are created for changed values |
| Examples: List, Set, Dictionary | Examples: String, Tuple, Integer           |

### **Q10. How do you check the data type of a variable using&#x20;**`type()`**&#x20;and&#x20;**`isinstance()`**?**

**Answer:**

We use two functions to check the data type of a variable.

**1.&#x20;**`type()`**:**

Returns the exact type of an object.

Example:

```
x = 100print(type(x))# <class 'int'>name = "Python"print(type(name))# <class 'str'>
```

**2.&#x20;**`isinstance()`**:**

Checks whether an object belongs to a particular type or class.

Example:

```
x = 100print(isinstance(x, int))# Trueprint(isinstance(x, str))# False
```

**Difference:**

- `type()` returns the object's exact type.
- `isinstance()` checks whether the object is an instance of a specified class or its subclasses.

### **Q11. What is Type Conversion in Python? Explain implicit and explicit type conversion with examples.**

**Answer:**

Type Conversion is the process of converting a variable from one data type to another.

There are two types.

**1. Implicit Type Conversion:**

Python automatically converts a value from one type to another when appropriate.

Example:

```
a = 10b = 10.5c = a + bprint(c)# 20.5print(type(c))# <class 'float'>
```

Here, Python converts the integer into a float during the operation.

**2. Explicit Type Conversion:**

We manually convert a value using built-in conversion functions.

Examples:

```
x = "100"y = int(x)print(y)# 100
```

Other examples:

```
int("10")float("10.5")str(100)list((1, 2, 3))tuple([1, 2, 3])set([1, 2, 2, 3])
```

### **Q12. What is the purpose of the&#x20;**`input()`**&#x20;function? What type of data does it return?**

**Answer:**

The `input()` function is used to read information from the user during program execution.

Example:

```
name = input("Enter your name: ")print(name)
```

**Important point:**

The `input()` function returns data in string format by default.

Example:

```
age = input("Enter age: ")print(type(age))# <class 'str'>
```

To accept an integer:

```
age = int(input("Enter age: "))
```

To accept a float:

```
salary = float(input("Enter salary: "))
```

### **Q13. What are the different types of operators in Python? Explain Arithmetic, Comparison, Logical, Assignment, Membership, Identity and Bitwise operators.**

**Answer:**

Operators are special symbols or keywords used to perform operations on variables and values.

Python supports seven major categories of operators.

**1. Arithmetic Operators:**

Used to perform mathematical operations.

| Operator | Purpose        | Example       |
| -------- | -------------- | ------------- |
| `+`      | Addition       | `5 + 3 = 8`   |
| `-`      | Subtraction    | `5 - 3 = 2`   |
| `*`      | Multiplication | `5 * 3 = 15`  |
| `/`      | Division       | `5 / 2 = 2.5` |
| `//`     | Floor division | `5 // 2 = 2`  |
| `%`      | Modulus        | `5 % 2 = 1`   |
| `**`     | Exponentiation | `2 ** 3 = 8`  |

**2. Comparison Operators:**

Used to compare values.

- `==`
- `!=`
- `>`
- `<`
- `>=`
- `<=`

Example:

```
x = 10y = 20print(x < y)# True
```

**3. Logical Operators:**

Used to combine conditions.

- `and`
- `or`
- `not`

**4. Assignment Operators:**

Used to assign values.

- `=`
- `+=`
- `-=`
- `*=`
- `/=`

Example:

```
x = 10x += 5print(x)# 15
```

**5. Membership Operators:**

Used to check whether an element exists in a sequence.

- `in`
- `not in`

Example:

```
list1 = [10, 20, 30]print(20 in list1)# True
```

**6. Identity Operators:**

Used to check whether two variables refer to the same object.

- `is`
- `is not`

**7. Bitwise Operators:**

Used to perform operations on binary representations of integers.

- `&` – AND.
- `|` – OR.
- `^` – XOR.
- `~` – NOT.
- `<<` – Left shift.
- `>>` – Right shift.

### **Q14. What is the difference between&#x20;**`==`**&#x20;and&#x20;**`is`**&#x20;operators?**

**Answer:**

Both operators are used for comparison, but they have different purposes.

`==`**&#x20;– Equality Operator:**

Checks whether two objects have equal values.

`is`**&#x20;– Identity Operator:**

Checks whether two variables refer to the same object in memory.

Example:

```
a = [10, 20]b = [10, 20]print(a == b)# Trueprint(a is b)# False
```

Here:

- Both lists contain the same values.
- But they are two different objects.

### **Q15. What are Membership Operators and Bitwise Operators? Explain with examples.**

**Answer:**

**Membership Operators:**

Membership operators check whether an element exists in a sequence or collection.

There are two operators:

- `in`
- `not in`

Example:

```
str1 = "Python"print("P" in str1)# Trueprint("z" not in str1)# True
```

**Bitwise Operators:**

Bitwise operators perform operations on binary representations of integer values.

Example:

```
a = 5b = 3print(a & b)# 1print(a | b)# 7print(a ^ b)# 6
```

Explanation:

```
5 = 101
3 = 011

AND = 001 = 1
OR  = 111 = 7
XOR = 110 = 6
```

# **Section 3 – Python Strings**

### **Q16. What is a String in Python? Is it mutable or immutable?**

**Answer:**

A String is a sequence of characters enclosed within single quotes, double quotes or triple quotes.

Examples:

```
str1 = "Python"str2 = 'Python'str3 = """Python Programming"""
```

Strings are immutable.

Once a string is created, we cannot modify its individual characters directly.

Example:

```
str1 = "Python"# This causes TypeError:# str1[0] = "J"
```

We can create a new string and assign it to the same variable.

### **Q17. What is String Indexing? Explain positive indexing and negative indexing.**

**Answer:**

String indexing is used to access individual characters from a string.

There are two types.

**1. Positive Indexing:**

Positive indexing starts from zero at the beginning of the string.

Example:

```
str1 = "Python"print(str1[0])# Pprint(str1[1])# y
```

**2. Negative Indexing:**

Negative indexing starts from `-1` at the end of the string.

Example:

```
str1 = "Python"print(str1[-1])# nprint(str1[-2])# o
```

### **Q18. What is String Slicing? Explain start, stop and step values with examples. How do you reverse a string using slicing?**

**Answer:**

String slicing is used to extract a portion of a string.

Syntax:

```
string[start:stop:step]
```

- `start` – Starting index.
- `stop` – Ending index, excluded from the result.
- `step` – Number of positions to skip.

Example:

```
str1 = "Python"print(str1[0:3])# Pytprint(str1[1:5])# ythoprint(str1[0:6:2])# Pto
```

**Reverse a String:**

```
str1 = "Python"print(str1[::-1])# nohtyP
```

The negative step moves through the string from right to left.

### **Q19. What is the difference between&#x20;**`find()`**&#x20;and&#x20;**`index()`**&#x20;methods in strings?**

**Answer:**

Both `find()` and `index()` are used to identify the position of a substring or character.

**find():**

Returns the index when the substring is found.

If the substring is not found, it returns `-1`.

**index():**

Returns the index when the substring is found.

If the substring is not found, it raises a `ValueError`.

Example:

```
str1 = "Python"print(str1.find("P"))# 0print(str1.find("z"))# -1print(str1.index("y"))# 1
```

**Difference:**

| find()                                        | index()                               |
| --------------------------------------------- | ------------------------------------- |
| Returns index if found                        | Returns index if found                |
| Returns -1 if not found                       | Raises ValueError if not found        |
| Does not raise an error for missing substring | Raises an error for missing substring |

### **Q20. Explain commonly used string methods such as&#x20;**`upper()`**,&#x20;**`lower()`**,&#x20;**`capitalize()`**,&#x20;**`title()`**,&#x20;**`startswith()`**,&#x20;**`endswith()`**,&#x20;**`isdigit()`**,&#x20;**`isalpha()`**,&#x20;**`isspace()`**,&#x20;**`strip()`**,&#x20;**`lstrip()`**&#x20;and&#x20;**`rstrip()`**.**

**Answer:**

Python provides many built-in string methods.

Consider:

```
str1 = "python language 3.0"
```

| Method         | Purpose                                      | Example                     |
| -------------- | -------------------------------------------- | --------------------------- |
| `upper()`      | Converts characters to uppercase             | `str1.upper()`              |
| `lower()`      | Converts characters to lowercase             | `str1.lower()`              |
| `capitalize()` | Capitalizes the first character              | `str1.capitalize()`         |
| `title()`      | Capitalizes the first character of each word | `str1.title()`              |
| `startswith()` | Checks the beginning of a string             | `str1.startswith("python")` |
| `endswith()`   | Checks the end of a string                   | `str1.endswith("3.0")`      |
| `isdigit()`    | Checks whether all characters are digits     | `"123".isdigit()`           |
| `isalpha()`    | Checks whether all characters are letters    | `"Python".isalpha()`        |
| `isspace()`    | Checks whether all characters are whitespace | `"   ".isspace()`           |
| `strip()`      | Removes leading and trailing whitespace      | `str1.strip()`              |
| `lstrip()`     | Removes leading whitespace                   | `str1.lstrip()`             |
| `rstrip()`     | Removes trailing whitespace                  | `str1.rstrip()`             |

**Example:**

```
str1 = " python "print(str1.strip())# pythonprint(str1.upper())#  PYTHON
```

These methods return new strings because strings are immutable.

### **Q21. How do you perform String Formatting and String Concatenation in Python? Explain&#x20;**`format()`**&#x20;and f-strings.**

**Answer:**

**String Formatting:**

String formatting allows us to insert variable values into a string.

Two common ways are:

1. `format()`.
2. f-strings.

**Using format():**

```
x = 10y = 20str1 = "The value of x is {} and y is {}".format(x, y)print(str1)
```

Output:

```
The value of x is 10 and y is 20
```

**Using f-strings:**

```
x = 10y = 20print(f"The sum of {x} and {y} is {x + y}")
```

Output:

```
The sum of 10 and 20 is 30
```

**String Concatenation:**

String concatenation means joining two or more strings.

We use the `+` operator.

```
str1 = "Python"str2 = " Programming"str3 = str1 + str2print(str3)# Python Programming
```

### **Q22. Write Python programs for the following string operations.**

**Answer:**

**1. Reverse a given string**

```
str1 = "Python"result = ""for i in range(len(str1) - 1, -1, -1):    result += str1[i]print(result)
```

Output:

```
nohtyP
```

**2. Count characters in a string**

```
str1 = "Python"count = 0for ch in str1:    count += 1print(count)
```

Output:

```
6
```

**3. Count the occurrence of each character**

```
str1 = "aabbcc"result = {}for ch in str1:    if ch in result:        result[ch] += 1    else:        result[ch] = 1print(result)
```

Output:

```
{'a': 2, 'b': 2, 'c': 2}
```

**4. Count alphabets, digits, spaces and special characters**

```
str1 = "Python 123@"alphabets = 0digits = 0spaces = 0special = 0for ch in str1:    if ('a' <= ch <= 'z') or ('A' <= ch <= 'Z'):        alphabets += 1    elif '0' <= ch <= '9':        digits += 1    elif ch == " ":        spaces += 1    else:        special += 1print("Alphabets:", alphabets)print("Digits:", digits)print("Spaces:", spaces)print("Special characters:", special)
```

**5. Remove duplicate characters from a string**

```
str1 = "aabbccdde"result = ""for ch in str1:    if ch not in result:        result += chprint(result)
```

Output:

```
abcde
```

**6. Find the longest repeated character sequence**

This example finds the longest consecutive run of the same character.

```
str1 = "aaabbccccdd"current_char = ""current_count = 0max_char = ""max_count = 0for ch in str1:    if ch == current_char:        current_count += 1    else:        current_char = ch        current_count = 1    if current_count > max_count:        max_count = current_count        max_char = chprint("Character:", max_char)print("Count:", max_count)print("Sequence:", max_char * max_count)
```

Output:

```
Character: c
Count: 4
Sequence: cccc
```

# **Section 4 – Python Collections: Lists, Tuples, Sets and Dictionaries**

## **Lists**

### **Q23. What is a List in Python? Explain its characteristics, indexing, slicing and mutability.**

**Answer:**

A List is a collection of elements stored in square brackets `[]`.

Example:

```
list1 = [10, 20, 30, "Python", 40.5]
```

**Characteristics:**

1. Lists are ordered.
2. Lists are mutable.
3. Lists allow duplicate elements.
4. Lists support indexing.
5. Lists support slicing.
6. Lists can contain different data types.

**Indexing:**

```
list1 = [10, 20, 30, 40]print(list1[0])# 10print(list1[-1])# 40
```

**Slicing:**

```
print(list1[0:2])# [10, 20]
```

**Mutability:**

```
list1[0] = 100print(list1)# [100, 20, 30, 40]
```

### **Q24. Explain different List methods such as&#x20;**`append()`**,&#x20;**`extend()`**,&#x20;**`insert()`**,&#x20;**`remove()`**,&#x20;**`pop()`**,&#x20;**`count()`**,&#x20;**`reverse()`**,&#x20;**`sort()`**,&#x20;**`copy()`**&#x20;and&#x20;**`clear()`**.**

**Answer:**

Python provides different built-in List methods.

Consider:

```
list1 = [10, 20, 30]
```

| Method      | Purpose                                             |
| ----------- | --------------------------------------------------- |
| `append()`  | Adds one element at the end                         |
| `extend()`  | Adds elements from another iterable                 |
| `insert()`  | Inserts an element at a specified index             |
| `remove()`  | Removes the first occurrence of a specified value   |
| `pop()`     | Removes and returns an element at a specified index |
| `count()`   | Counts occurrences of a specified value             |
| `reverse()` | Reverses the list in place                          |
| `sort()`    | Sorts the list in place                             |
| `copy()`    | Creates a shallow copy                              |
| `clear()`   | Removes all elements                                |

**Examples:**

```
list1 = [10, 20, 30]list1.append(40)# [10, 20, 30, 40]list1.extend([50, 60])# [10, 20, 30, 40, 50, 60]list1.insert(1, 15)# [10, 15, 20, 30, 40, 50, 60]list1.remove(15)x = list1.pop()print(list1.count(20))list1.reverse()list1.sort()list2 = list1.copy()list1.clear()
```

### **Q25. Write Python programs for the following list operations.**

**Answer:**

**1. Find the largest number**

```
list1 = [10, 20, 177, 16]largest = list1[0]for num in list1:    if num > largest:        largest = numprint(largest)
```

Output:

```
177
```

**2. Find the second-largest distinct number**

```
list1 = [10, 20, 177, 16, 177]largest = Nonesecond = Nonefor num in list1:    if largest is None or num > largest:        if num != largest:            second = largest        largest = num    elif num != largest and (second is None or num > second):        second = numprint(second)
```

Output:

```
20
```

**3. Remove duplicate elements**

```
list1 = [10, 20, 10, 30, 20]result = []for num in list1:    if num not in result:        result.append(num)print(result)
```

Output:

```
[10, 20, 30]
```

**4. Sort a list in ascending and descending order**

```
list1 = [40, 10, 30, 20]for i in range(len(list1)):    for j in range(i + 1, len(list1)):        if list1[i] > list1[j]:            list1[i], list1[j] = list1[j], list1[i]print("Ascending:", list1)for i in range(len(list1)):    for j in range(i + 1, len(list1)):        if list1[i] < list1[j]:            list1[i], list1[j] = list1[j], list1[i]print("Descending:", list1)
```

**5. Implement Bubble Sort**

```
list1 = [77, 10, 85, 5, 99, 10]n = len(list1)for i in range(n):    for j in range(0, n - i - 1):        if list1[j] > list1[j + 1]:            list1[j], list1[j + 1] = list1[j + 1], list1[j]print(list1)
```

**6. Merge two lists by alternating their elements**

```
list1 = [1, 3, 5]list2 = [2, 4, 6]result = []i = 0while i < len(list1) or i < len(list2):    if i < len(list1):        result.append(list1[i])    if i < len(list2):        result.append(list2[i])    i += 1print(result)
```

Output:

```
[1, 2, 3, 4, 5, 6]
```

**7. Find the difference between two lists**

```
list1 = [1, 2, 3, 4, 5]list2 = [2, 4, 6]result = []for item in list1:    if item not in list2:        result.append(item)print(result)
```

Output:

```
[1, 3, 5]
```

**8. Flatten a nested list**

For an arbitrarily nested list:

```
def flatten(lst):    result = []    for item in lst:        if isinstance(item, list):            result += flatten(item)        else:            result.append(item)    return resultlist1 = [1, [2, 3], [4, [5, 6]]]print(flatten(list1))
```

Output:

```
[1, 2, 3, 4, 5, 6]
```

## **Tuples**

### **Q26. What is a Tuple in Python? Explain its characteristics and methods.**

**Answer:**

A Tuple is a collection of elements stored in parentheses `()`.

Example:

```
t1 = (10, 20, 30)
```

**Characteristics:**

1. Tuples are ordered.
2. Tuples are immutable.
3. Tuples allow duplicate elements.
4. Tuples support indexing.
5. Tuples support slicing.
6. Tuples can store multiple data types.

**Important Tuple Methods:**

**count():**

Returns the number of occurrences of an element.

```
t1 = (10, 20, 10, 30)print(t1.count(10))# 2
```

**index():**

Returns the index of a specified element.

```
print(t1.index(20))# 1
```

**Single-element Tuple:**

```
t1 = (10,)
```

The comma is required to create a single-element tuple.

### **Q27. What is the difference between List and Tuple? Why is a tuple immutable, and how do you create a tuple containing only one element?**

**Answer:**

| List                          | Tuple                                              |
| ----------------------------- | -------------------------------------------------- |
| Uses square brackets `[]`     | Uses parentheses `()`                              |
| Mutable                       | Immutable                                          |
| Allows duplicates             | Allows duplicates                                  |
| Supports indexing and slicing | Supports indexing and slicing                      |
| Has many modifying methods    | Has fewer methods                                  |
| Generally uses more memory    | Generally uses less memory for comparable contents |

**Why is Tuple immutable?**

Once a tuple is created, its elements cannot be reassigned, added or removed.

This makes it suitable for data that should not be changed.

**Single-element Tuple:**

```
t1 = (10,)print(type(t1))# <class 'tuple'>
```

Without the comma:

```
t1 = (10)print(type(t1))# <class 'int'>
```

## **Sets**

### **Q28. What is a Set in Python? Explain its characteristics and why sets do not support indexing or duplicate elements.**

**Answer:**

A Set is a collection of unique elements in Python.

It is created using curly brackets `{}` or the `set()` function.

Example:

```
set1 = {10, 20, 30}
```

**Characteristics:**

1. Sets are mutable.
2. Sets do not store duplicate elements.
3. Sets do not support indexing.
4. Sets are unordered collections.
5. Sets support mathematical operations.

**Example:**

```
set1 = {10, 20, 10, 30}print(set1)
```

Output contains only unique values:

```
{10, 20, 30}
```

**Why no indexing?**

Sets do not provide a stable positional sequence of elements. Therefore, we cannot access elements using indexes.

### **Q29. Explain different Set methods such as&#x20;**`add()`**,&#x20;**`update()`**,&#x20;**`remove()`**,&#x20;**`discard()`**,&#x20;**`pop()`**,&#x20;**`copy()`**&#x20;and&#x20;**`clear()`**.**

**Answer:**

| Method      | Purpose                                       |
| ----------- | --------------------------------------------- |
| `add()`     | Adds one element                              |
| `update()`  | Adds multiple elements from an iterable       |
| `remove()`  | Removes an element; raises KeyError if absent |
| `discard()` | Removes an element without error if absent    |
| `pop()`     | Removes and returns an arbitrary element      |
| `copy()`    | Creates a shallow copy                        |
| `clear()`   | Removes all elements                          |

Example:

```
set1 = {10, 20, 30}set1.add(40)set1.update([50, 60])set1.remove(20)set1.discard(100)set2 = set1.copy()set1.clear()print(set1)# set()
```

### **Q30. Explain Set operations such as Union, Intersection, Difference and Symmetric Difference with examples.**

**Answer:**

Consider:

```
set1 = {1, 2, 3, 4, 5}set2 = {3, 4, 5, 6, 7}
```

**1. Union:**

Combines all unique elements from both sets.

```
print(set1.union(set2))
```

Output:

```
{1, 2, 3, 4, 5, 6, 7}
```

**2. Intersection:**

Returns common elements from both sets.

```
print(set1.intersection(set2))
```

Output:

```
{3, 4, 5}
```

**3. Difference:**

Returns elements present in the first set but not in the second set.

```
print(set1.difference(set2))
```

Output:

```
{1, 2}
```

**4. Symmetric Difference:**

Returns elements present in either set but not both.

```
print(set1.symmetric_difference(set2))
```

Output:

```
{1, 2, 6, 7}
```

## **Dictionaries**

### **Q31. What is a Dictionary in Python? Explain its structure, properties and key-value pairs.**

**Answer:**

A Dictionary is a collection of key-value pairs in Python.

It is defined using curly brackets `{}`.

Example:

```
dict1 = {    "name": "John",    "age": 30,    "location": "New York"}
```

Here:

- `name`, `age` and `location` are keys.
- `John`, `30` and `New York` are values.

**Characteristics:**

1. Dictionaries are mutable.
2. They store key-value pairs.
3. Keys must be unique.
4. Values can be duplicated.
5. Dictionaries preserve insertion order in modern Python.
6. Dictionaries do not support positional indexing or slicing.
7. Keys must be hashable.

**Accessing Values:**

```
print(dict1["name"])# John
```

### **Q32. Explain different Dictionary methods such as&#x20;**`get()`**,&#x20;**`setdefault()`**,&#x20;**`update()`**,&#x20;**`keys()`**,&#x20;**`values()`**,&#x20;**`items()`**,&#x20;**`pop()`**,&#x20;**`popitem()`**,&#x20;**`copy()`**&#x20;and&#x20;**`clear()`**.**

**Answer:**

Consider:

```
dict1 = {    "a": 10,    "b": 20,    "c": 30}
```

| Method         | Purpose                                              |
| -------------- | ---------------------------------------------------- |
| `get()`        | Returns the value for a key, or a default value      |
| `setdefault()` | Returns a key's value or inserts a default           |
| `update()`     | Adds or updates key-value pairs                      |
| `keys()`       | Returns dictionary keys                              |
| `values()`     | Returns dictionary values                            |
| `items()`      | Returns key-value pairs                              |
| `pop()`        | Removes a specified key and returns its value        |
| `popitem()`    | Removes and returns the last inserted key-value pair |
| `copy()`       | Creates a shallow copy                               |
| `clear()`      | Removes all key-value pairs                          |

**Examples:**

```
print(dict1.get("a"))# 10print(dict1.get("d"))# Nonedict1.setdefault("d", 40)dict1.update({"e": 50})print(dict1.keys())print(dict1.values())print(dict1.items())dict1.pop("a")dict1.popitem()dict2 = dict1.copy()dict1.clear()
```

### **Q33. How do you merge two dictionaries? Explain the following scenarios.**

**Answer:**

Consider:

```
dict1 = {"a": 10, "b": 20, "c": 40}dict2 = {"a": 30, "c": 30, "d": 50}
```

**1. Merge two dictionaries**

```
result = dict1.copy()result.update(dict2)print(result)
```

For duplicate keys, the second dictionary's value replaces the first.

**2. Add values if keys are common**

```
result = {}for key in dict1:    result[key] = dict1[key]for key in dict2:    if key in result:        result[key] += dict2[key]    else:        result[key] = dict2[key]print(result)
```

Output:

```
{'a': 40, 'b': 20, 'c': 70, 'd': 50}
```

**3. Store common values in a list**

```
result = {}for key in dict1:    if key in dict2:        result[key] = [dict1[key], dict2[key]]    else:        result[key] = dict1[key]for key in dict2:    if key not in result:        result[key] = dict2[key]print(result)
```

Output:

```
{'a': [10, 30], 'b': 20, 'c': [40, 30], 'd': 50}
```

**4. Ignore common keys**

```
result = {}for key in dict1:    if key not in dict2:        result[key] = dict1[key]for key in dict2:    if key not in dict1:        result[key] = dict2[key]print(result)
```

Output:

```
{'b': 20, 'd': 50}
```

**5. Print common keys**

```
common = []for key in dict1:    if key in dict2:        common.append(key)print(common)
```

Output:

```
['a', 'c']
```

### **Q34. Write Python programs for the following dictionary operations.**

**Answer:**

**1. Find the key with maximum and minimum values**

```
dict1 = {    "a": 40,    "b": 20,    "c": 70,    "d": 50}max_key = Nonemin_key = Nonefor key in dict1:    if max_key is None or dict1[key] > dict1[max_key]:        max_key = key    if min_key is None or dict1[key] < dict1[min_key]:        min_key = keyprint("Maximum:", max_key, dict1[max_key])print("Minimum:", min_key, dict1[min_key])
```

**2. Count character occurrences using a dictionary**

```
str1 = "aabbcc"result = {}for ch in str1:    if ch in result:        result[ch] += 1    else:        result[ch] = 1print(result)
```

**3. Create a dictionary from two lists**

```
keys = ['a', 'b', 'c']values = [1, 2, 3]result = {}for i in range(len(keys)):    result[keys[i]] = values[i]print(result)
```

Output:

```
{'a': 1, 'b': 2, 'c': 3}
```

**4. Convert a dictionary into a list of tuples**

```
dict1 = {    "name": "John",    "age": 30,    "city": "New York"}result = []for key, value in dict1.items():    result.append((key, value))print(result)
```

Output:

```
[('name', 'John'), ('age', 30), ('city', 'New York')]
```

**5. Count element occurrences and create a dictionary**

```
list1 = ["a", "b", "c", "a", "b"]result = {}for item in list1:    if item in result:        result[item] += 1    else:        result[item] = 1print(result)
```

Output:

```
{'a': 2, 'b': 2, 'c': 1}
```

**6. Group words based on their length**

```
words = ['cat', 'dog', 'elephant', 'bat', 'batman']result = {}for word in words:    size = len(word)    if size in result:        result[size].append(word)    else:        result[size] = [word]print(result)
```

Output:

```
{
    3: ['cat', 'dog', 'bat'],
    8: ['elephant', 'batman']
}
```

### **Q35. Given a nested company dictionary containing departments, employees and budgets, write programs to perform the required operations.**

**Answer:**

Consider the dictionary:

```
company = {    'department1': {        'name': 'Sales',        'employees': {            'e1': {                'name': 'John',                'age': 30,                'position': 'Manager'            },            'e2': {                'name': 'Alice',                'age': 25,                'position': 'Sales Associate'            }        },        'budget': 100000    },    'department2': {        'name': 'Engineering',        'employees': {            'e3': {                'name': 'Bob',                'age': 35,                'position': 'Lead Engineer'            },            'e4': {                'name': 'Charlie',                'age': 28,                'position': 'Software Engineer'            }        },        'budget': 200000    },    'department3': {
```

**1. Print all dictionary keys**

```
for key in company:    print(key)
```

**2. Print the name of department1**

```
print(company["department1"]["name"])
```

Output:

```
Sales
```

**3. Calculate the total company budget**

```
total = 0for department in company:    total += company[department]["budget"]print(total)
```

Output:

```
350000
```

**4. Find the age of John**

```
for department in company:    employees = company[department]["employees"]    for employee in employees:        details = employees[employee]        if details["name"] == "John":            print(details["age"])
```

Output:

```
30
```

**5. Find the position of David**

```
for department in company:    employees = company[department]["employees"]    for employee in employees:        details = employees[employee]        if details["name"] == "David":            print(details["position"])
```

Output:

```
Marketing Manager
```

**6. Identify the department with the lowest budget**

```
lowest_department = Nonelowest_budget = Nonefor department in company:    budget = company[department]["budget"]    if lowest_budget is None or budget < lowest_budget:        lowest_budget = budget        lowest_department = company[department]["name"]print(lowest_department)print(lowest_budget)
```

Output:

```
Marketing
50000
```

### **Q36. What is the difference between Shallow Copy and Deep Copy in Python? Explain&#x20;**`copy.copy()`**&#x20;and&#x20;**`copy.deepcopy()`**&#x20;with examples.**

**Answer:**

Python supports two types of copying:

1. Shallow Copy.
2. Deep Copy.

We use the `copy` module.

```
import copy
```

**1. Shallow Copy:**

Shallow Copy creates a new outer object, but the nested objects are still referenced by both the original and copied objects.

Example:

```
import copylist1 = [1, 2, [3, 4]]list2 = copy.copy(list1)list2[2][0] = 99print(list1)print(list2)
```

Output:

```
[1, 2, [99, 4]]
[1, 2, [99, 4]]
```

The nested list is shared between both objects.

**2. Deep Copy:**

Deep Copy creates a new outer object and recursively copies nested objects.

Example:

```
import copylist1 = [1, 2, [3, 4]]list2 = copy.deepcopy(list1)list2[2][0] = 99print(list1)print(list2)
```

Output:

```
[1, 2, [3, 4]]
[1, 2, [99, 4]]
```

Here, modifying the nested list in the copied object does not affect the original.

**Difference:**

| Shallow Copy                              | Deep Copy                                                   |
| ----------------------------------------- | ----------------------------------------------------------- |
| Creates a new outer object                | Creates an independent copy of nested objects too           |
| Nested objects are shared                 | Nested objects are copied recursively                       |
| Changes to nested objects can affect both | Changes to copied nested objects do not affect the original |
| Uses `copy.copy()`                        | Uses `copy.deepcopy()`                                      |

# **Section 5 – Conditional Statements, Loops and Comprehensions**

### **Q37. What are Conditional Statements in Python? Explain&#x20;**`if`**,&#x20;**`elif`**&#x20;and&#x20;**`else`**&#x20;with examples.**

**Answer:**

Conditional statements are used to execute different blocks of code depending on whether a condition is True or False.

Python supports:

1. `if`
2. `elif`
3. `else`

**1. if:**

Executes a block when the condition is True.

```
x = 10if x > 5:    print("Greater than 5")
```

**2. if-else:**

Executes one block when the condition is True and another when it is False.

```
x = 10if x % 2 == 0:    print("Even")else:    print("Odd")
```

**3. if-elif-else:**

Used when we need to check multiple conditions.

```
x = 100if x > 100:    print("Above 100")elif x == 100:    print("Equal to 100")else:    print("Below 100")
```

### **Q38. What are Loops in Python? Explain&#x20;**`for`**&#x20;and&#x20;**`while`**&#x20;loops with examples.**

**Answer:**

Loops are used to execute a block of code repeatedly.

Python supports two main loops:

**1. For Loop:**

A `for` loop iterates over a sequence such as a string, list, tuple or range.

Example:

```
list1 = [10, 20, 30, 40]for i in list1:    print(i)
```

**2. While Loop:**

A `while` loop executes a block of code as long as the condition remains True.

Example:

```
i = 1while i <= 5:    print(i)    i += 1
```

**Difference:**

| For Loop                                      | While Loop                                            |
| --------------------------------------------- | ----------------------------------------------------- |
| Iterates over a sequence or iterable          | Repeats while a condition is True                     |
| Commonly used when iterating over collections | Commonly used when repetition depends on a condition  |
| Iteration is controlled by the iterable       | We generally manage the condition and update manually |

### **Q39. What is the&#x20;**`range()`**&#x20;function? Explain&#x20;**`range(start, stop, step)`**&#x20;with examples.**

**Answer:**

The `range()` function is a built-in Python function used to generate a sequence of integers.

Syntax:

```
range(start, stop, step)
```

- `start` – Starting value, included.
- `stop` – Ending value, excluded.
- `step` – Difference between consecutive values.

Example:

```
for i in range(1, 6):    print(i)
```

Output:

```
1
2
3
4
5
```

Using step:

```
for i in range(2, 11, 2):    print(i)
```

Output:

```
2
4
6
8
10
```

Reverse range:

```
for i in range(5, 0, -1):    print(i)
```

Output:

```
5
4
3
2
1
```

### **Q40. What are the Loop Control Statements? Explain&#x20;**`break`**,&#x20;**`continue`**&#x20;and&#x20;**`pass`**.**

**Answer:**

Loop control statements are used to control the execution flow of loops.

There are three important statements.

**1. break:**

Terminates the loop completely.

```
for i in range(1, 6):    if i == 3:        break    print(i)
```

Output:

```
1
2
```

**2. continue:**

Skips the current iteration and moves to the next iteration.

```
for i in range(1, 6):    if i == 3:        continue    print(i)
```

Output:

```
1
2
4
5
```

**3. pass:**

Does nothing. It is used as a placeholder when a statement or block is required syntactically but its implementation is not yet provided.

```
for i in range(1, 6):    if i == 3:        pass    print(i)
```

Output:

```
1
2
3
4
5
```

**Difference:**

| break               | continue                      | pass                                    |
| ------------------- | ----------------------------- | --------------------------------------- |
| Terminates the loop | Skips current iteration       | Does nothing                            |
| Exits the loop      | Continues with next iteration | Allows the program to continue normally |

### **Q41. What is the&#x20;**`enumerate()`**&#x20;function? How do you access both the index and value of a sequence?**

**Answer:**

`enumerate()` is a built-in Python function used to access both the index and actual element of a sequence.

Example:

```
list1 = [10, 20, 30, 40]for index, value in enumerate(list1):    print(index, value)
```

Output:

```
0 10
1 20
2 30
3 40
```

We can also provide a starting index.

```
for index, value in enumerate(list1, start=1):    print(index, value)
```

Output:

```
1 10
2 20
3 30
4 40
```

### **Q42. What is the&#x20;**`zip()`**&#x20;function? How do you combine two or more lists using&#x20;**`zip()`**?**

**Answer:**

The `zip()` function combines corresponding elements from two or more iterables.

It returns an iterator containing tuples.

Example:

```
list1 = [1, 2, 3]list2 = [4, 5, 6]result = list(zip(list1, list2))print(result)
```

Output:

```
[(1, 4), (2, 5), (3, 6)]
```

**Using zip to create a dictionary:**

```
keys = ["a", "b", "c"]values = [10, 20, 30]result = dict(zip(keys, values))print(result)
```

Output:

```
{'a': 10, 'b': 20, 'c': 30}
```

When the iterables have different lengths, normal `zip()` stops at the shortest iterable.

### **Q43. What is Packing and Unpacking in Python? Explain with examples.**

**Answer:**

**Packing:**

Packing means combining multiple values into a single variable, commonly a tuple.

Example:

```
a = 10b = 20c = 30values = a, b, cprint(values)# (10, 20, 30)
```

**Unpacking:**

Unpacking means assigning elements of a collection to separate variables.

Example:

```
values = (10, 20, 30)a, b, c = valuesprint(a)print(b)print(c)
```

Output:

```
10
20
30
```

**Extended Unpacking:**

```
a, *b = [10, 20, 30, 40]print(a)# 10print(b)# [20, 30, 40]
```

### **Q44. What are Comprehensions in Python? Explain List, Dictionary and Set Comprehensions with examples. How do they differ from normal loops?**

**Answer:**

Comprehensions are a concise way of creating collections in Python using a single expression.

They reduce the amount of code required for common collection-building operations.

There are three important types.

**1. List Comprehension:**

Creates a list.

Syntax:

```
[expression for item in iterable if condition]
```

Example:

```
list1 = [i for i in range(10) if i % 2 == 0]print(list1)
```

Output:

```
[0, 2, 4, 6, 8]
```

**Using a normal loop:**

```
list1 = []for i in range(10):    if i % 2 == 0:        list1.append(i)
```

**2. Dictionary Comprehension:**

Creates a dictionary.

Example:

```
dict1 = {i: i * i for i in range(1, 6)}print(dict1)
```

Output:

```
{1: 1, 2: 4, 3: 9, 4: 16, 5: 25}
```

**3. Set Comprehension:**

Creates a set.

Example:

```
set1 = {i for i in [1, 2, 2, 3, 3, 4]}print(set1)
```

Output contains unique elements:

```
{1, 2, 3, 4}
```

**Difference:**

| Normal Loop                             | Comprehension                                    |
| --------------------------------------- | ------------------------------------------------ |
| Requires multiple lines in common cases | Often written in one expression                  |
| Uses explicit collection updates        | Creates the collection directly                  |
| Easy for complex control flow           | Useful for concise transformations and filtering |

# **Section 6 – Python Functions**

### **Q45. What is a Function in Python? How do you define and call a function?**

**Answer:**

A function is a reusable block of code that performs a particular task.

Functions help us avoid writing the same code repeatedly.

We define a function using the `def` keyword.

**Syntax:**

```
def function_name():    # block of code
```

**Example:**

```
def add():    a = 10    b = 20    print(a + b)add()
```

Output:

```
30
```

Here:

- `def` defines the function.
- `add` is the function name.
- `add()` calls the function.

### **Q46. What is the difference between&#x20;**`print()`**&#x20;and&#x20;**`return`**&#x20;in Python functions?**

**Answer:**

**print():**

`print()` displays output on the screen.

It is mainly used to display information and debug programs.

**return:**

`return` sends a value back to the caller of the function.

It also terminates the function's execution.

**Example:**

```
def add(a, b):    print(a + b)add(10, 20)
```

Output:

```
30
```

Here, the function displays the result but does not return it.

**Using return:**

```
def add(a, b):    return a + bresult = add(10, 20)print(result)
```

Output:

```
30
```

**Difference:**

| print()                                 | return                                |
| --------------------------------------- | ------------------------------------- |
| Displays output                         | Sends a value back to the caller      |
| Used for displaying and debugging       | Used for further processing           |
| Does not terminate a function by itself | Terminates the function when executed |
| Returns `None` itself                   | Returns the specified value           |

### **Q47. What are the different types of arguments accepted by Python functions? Explain the order in which arguments are defined.**

**Answer:**

Python supports different types of function arguments.

The important types are:

1. Positional Arguments.
2. Keyword Arguments.
3. Default Arguments.
4. Variable-Length Positional Arguments (`*args`).
5. Variable-Length Keyword Arguments (`**kwargs`).

**Function Argument Order:**

A common valid definition order is:

```
def function(a, b=10, *args, c, **kwargs):    pass
```

Here:

- `a` – Required positional argument.
- `b` – Default argument.
- `*args` – Variable-length positional arguments.
- `c` – Keyword-only argument.
- `**kwargs` – Variable-length keyword arguments.

**Important Rule:**

Non-default parameters cannot follow default positional parameters in a function definition.

### **Q48. What is the difference between Positional Arguments and Keyword Arguments?**

**Answer:**

**Positional Arguments:**

Values are passed according to the position of parameters in the function definition.

Example:

```
def add(a, b):    return a + bprint(add(10, 20))
```

Here:

- `a = 10`.
- `b = 20`.

**Keyword Arguments:**

Values are passed using parameter names.

Example:

```
def add(a, b):    return a + bprint(add(b=20, a=10))
```

Output:

```
30
```

**Difference:**

| Positional Arguments        | Keyword Arguments             |
| --------------------------- | ----------------------------- |
| Based on parameter position | Based on parameter name       |
| Order matters               | Order can be changed          |
| Values are passed directly  | Parameter names are specified |

### **Q49. What are Default Arguments in Python? How do they work?**

**Answer:**

Default arguments are parameters that have predefined values in the function definition.

If we do not provide a value during the function call, Python uses the default value.

Example:

```
def add(a, b=20):    return a + bprint(add(10))# 30print(add(10, 50))# 60
```

Here, the default value of `b` is 20.

When we pass `50`, the default value is overridden.

### **Q50. What are Variable-Length Arguments? Explain&#x20;**`*args`**&#x20;and&#x20;**`**kwargs`**&#x20;with examples.**

**Answer:**

Variable-Length Arguments allow a function to accept any number of arguments.

There are two types.

**1.&#x20;**`*args`**:**

Used to accept multiple positional arguments.

Inside the function, the values are available as a tuple.

Example:

```
def add(*args):    total = 0    for num in args:        total += num    return totalprint(add(10, 20))print(add(10, 20, 30))
```

Output:

```
30
60
```

**2.&#x20;**`**kwargs`**:**

Used to accept multiple keyword arguments.

Inside the function, the values are available as a dictionary.

Example:

```
def display(**kwargs):    for key, value in kwargs.items():        print(key, value)display(name="John", age=30, city="London")
```

**Difference:**

| `*args`                               | `**kwargs`                         |
| ------------------------------------- | ---------------------------------- |
| Accepts variable positional arguments | Accepts variable keyword arguments |
| Stores values in a tuple              | Stores values in a dictionary      |
| Uses positional values                | Uses named values                  |

### **Q51. What is Variable Scope in Python? Explain Local Variables, Global Variables and the&#x20;**`global`**&#x20;keyword.**

**Answer:**

Variable Scope defines where a variable can be accessed in a Python program.

There are two main scopes covered in my notes.

**1. Global Variable:**

A global variable is defined outside a function.

It can be accessed from different functions within the same module, subject to normal name-resolution rules.

Example:

```
x = 10def display():    print(x)display()
```

Output:

```
10
```

**2. Local Variable:**

A local variable is defined inside a function.

It is generally accessible only within that function.

Example:

```
x = 10def display():    x = 20    print(x)display()print(x)
```

Output:

```
20
10
```

**global Keyword:**

We use the `global` keyword when we want to assign to a global variable inside a function.

Example:

```
x = 10def update():    global x    x = 20update()print(x)
```

Output:

```
20
```

### **Q52. What is a Lambda Function? How does it differ from a regular function defined using&#x20;**`def`**?**

**Answer:**

A Lambda Function is an anonymous function created using the `lambda` keyword.

It is generally used for small operations that can be expressed in a single expression.

**Syntax:**

```
lambda arguments: expression
```

**Example:**

```
add = lambda a, b: a + bprint(add(10, 20))
```

Output:

```
30
```

**Difference:**

| Lambda Function                   | Regular Function                |
| --------------------------------- | ------------------------------- |
| Uses `lambda` keyword             | Uses `def` keyword              |
| Usually has a single expression   | Can contain multiple statements |
| Returns the expression result     | Can use an explicit `return`    |
| Usually used for small operations | Used for larger reusable logic  |
| Anonymous by default              | Has a defined function name     |

### **Q53. What is the purpose of the&#x20;**`map()`**&#x20;function? How do you use it with lambda functions?**

**Answer:**

The `map()` function applies a given function to every element of an iterable.

It returns a map object, which can be converted into a list or another suitable collection.

**Syntax:**

```
map(function, iterable)
```

**Example using lambda:**

```
list1 = [1, 2, 3, 4]result = list(map(lambda x: x * x, list1))print(result)
```

Output:

```
[1, 4, 9, 16]
```

Here, the lambda function calculates the square of each element.

**Example without lambda:**

```
def square(x):    return x * xresult = list(map(square, [1, 2, 3]))print(result)
```

Output:

```
[1, 4, 9]
```

### **Q54. How does the&#x20;**`filter()`**&#x20;function work? Explain with examples.**

**Answer:**

The `filter()` function selects elements from an iterable based on a condition.

It applies a function to each element and retains the elements for which the function returns True.

**Syntax:**

```
filter(function, iterable)
```

**Example:**

Print only even numbers.

```
list1 = [10, 20, 30, 40, 50]result = list(    filter(lambda x: x % 2 == 0, list1))print(result)
```

Output:

```
[10, 20, 30, 40, 50]
```

**Example – Filter numbers greater than 30:**

```
list1 = [10, 20, 30, 40, 50]result = list(    filter(lambda x: x > 30, list1))print(result)
```

Output:

```
[40, 50]
```

### **Q55. What is the purpose of the&#x20;**`reduce()`**&#x20;function? From which module do we import it?**

**Answer:**

The `reduce()` function is used to reduce an iterable into a single accumulated result.

It applies a function cumulatively to the elements.

We import it from the `functools` module.

Example:

```
from functools import reducelist1 = [1, 2, 3, 4]result = reduce(lambda x, y: x + y, list1)print(result)
```

Output:

```
10
```

**Working:**

```
1 + 2 = 3
3 + 3 = 6
6 + 4 = 10
```

### **Q56. What is a Higher-Order Function? How do you pass one function as an argument to another function?**

**Answer:**

A Higher-Order Function is a function that takes another function as an argument or returns a function.

Example:

```
def add(a, b):    return a + bdef calculate(func, x, y):    return func(x, y)result = calculate(add, 10, 20)print(result)
```

Output:

```
30
```

Here:

- `add()` is passed as an argument to `calculate()`.
- `calculate()` calls the passed function.

This is called a Higher-Order Function.

### **Q57. What is Recursion in Python? How does a recursive function work?**

**Answer:**

Recursion is a programming technique in which a function calls itself.

A recursive function requires:

1. Base Condition.
2. Recursive Call.

The base condition stops the recursion.

Example – Factorial:

```
def factorial(n):    if n == 0:        return 1    return n * factorial(n - 1)print(factorial(5))
```

Output:

```
120
```

Working:

```
5 * 4 * 3 * 2 * 1 = 120
```

### **Q58. Write Python functions for the following scenarios.**

**Answer:**

**1. Find the largest number from a list**

```
def largest(lst):    max_num = lst[0]    for num in lst:        if num > max_num:            max_num = num    return max_numprint(largest([10, 20, 30, 5]))
```

**Output:** `30`

**2. Find the second-largest number**

```
def second_largest(lst):    first = None    second = None    for num in lst:        if first is None or num > first:            if num != first:                second = first            first = num        elif num != first and (second is None or num > second):            second = num    return secondprint(second_largest([10, 20, 30, 40, 40]))
```

**Output:** `30`

**3. Reverse a string**

```
def reverse_string(s):    result = ""    for i in range(len(s) - 1, -1, -1):        result += s[i]    return resultprint(reverse_string("Python"))
```

**Output:** `nohtyP`

**4. Remove duplicates from a list**

```
def remove_duplicates(lst):    result = []    for item in lst:        if item not in result:            result.append(item)    return resultprint(remove_duplicates([1, 2, 2, 3, 1]))
```

**Output:** `[1, 2, 3]`

**5. Sort a list and return it**

```
def sort_list(lst):    for i in range(len(lst)):        for j in range(i + 1, len(lst)):            if lst[i] > lst[j]:                lst[i], lst[j] = lst[j], lst[i]    return lstprint(sort_list([5, 2, 8, 1]))
```

**Output:** `[1, 2, 5, 8]`

**6. Generate prime numbers in a given range**

```
def prime_numbers(start, end):    result = []    for num in range(start, end + 1):        if num > 1:            is_prime = True            for i in range(2, num):                if num % i == 0:                    is_prime = False                    break            if is_prime:                result.append(num)    return resultprint(prime_numbers(1, 20))
```

**Output:** `[2, 3, 5, 7, 11, 13, 17, 19]`

**7. Calculate factorial**

```
def factorial(n):    if n < 0:        raise ValueError("Negative number is not allowed")    fact = 1    for i in range(1, n + 1):        fact *= i    return factprint(factorial(5))
```

**Output:** `120`

**8. Check whether a string is a palindrome**

```
def is_palindrome(s):    reverse = ""    for i in range(len(s) - 1, -1, -1):        reverse += s[i]    return s == reverseprint(is_palindrome("madam"))
```

**Output:** `True`

**9. Generate the Fibonacci sequence up to n terms**

```
def fibonacci(n):    a = 0    b = 1    result = []    for i in range(n):        result.append(a)        a, b = b, a + b    return resultprint(fibonacci(7))
```

**Output:** `[0, 1, 1, 2, 3, 5, 8]`

**10. Calculate the sum of digits**

```
def sum_of_digits(n):    total = 0    while n > 0:        digit = n % 10        total += digit        n //= 10    return totalprint(sum_of_digits(1234))
```

**Output:** `10`

**11. Count vowels in a string**

```
def count_vowels(s):    count = 0    for ch in s.lower():        if ch in "aeiou":            count += 1    return countprint(count_vowels("Python Programming"))
```

**Output:** `4`

**12. Sort a dictionary based on its values**

```
def sort_dict_by_value(d):    result = []    for key in d:        result.append((key, d[key]))    for i in range(len(result)):        for j in range(i + 1, len(result)):            if result[i][1] > result[j][1]:                result[i], result[j] = result[j], result[i]    return resultdict1 = {"a": 30, "b": 10, "c": 20}print(sort_dict_by_value(dict1))
```

**Output:**

```
[('b', 10), ('c', 20), ('a', 30)]
```

**13. Merge two lists by alternating their elements**

```
def merge_lists(lst1, lst2):    result = []    i = 0    while i < len(lst1) or i < len(lst2):        if i < len(lst1):            result.append(lst1[i])        if i < len(lst2):            result.append(lst2[i])        i += 1    return resultprint(merge_lists([1, 3, 5], [2, 4, 6]))
```

**Output:** `[1, 2, 3, 4, 5, 6]`

**14. Flatten a nested list**

```
def flatten(lst):    result = []    for item in lst:        if isinstance(item, list):            result += flatten(item)        else:            result.append(item)    return resultprint(flatten([1, [2, 3], [4, [5, 6]]]))
```

**Output:** `[1, 2, 3, 4, 5, 6]`

**15. Generate Fibonacci series using recursion**

```
def fibonacci(n):    if n <= 1:        return n    return fibonacci(n - 1) + fibonacci(n - 2)for i in range(7):    print(fibonacci(i))
```

**Output:**

```
0
1
1
2
3
5
8
```

# **Section 7 – Python File Handling and JSON**

### **Q59. What is File Handling in Python? Why do we use it?**

**Answer:**

File Handling is the process of creating, opening, reading, writing, appending and closing files using Python.

We use File Handling to store information permanently and retrieve it whenever required.

**Common operations:**

1. Open a file.
2. Read file contents.
3. Write data into a file.
4. Append data.
5. Close a file.
6. Search and modify file contents.

Example:

```
file1 = open("test.txt", "w")file1.write("Hello Python")file1.close()
```

### **Q60. What are the different file access modes in Python? Explain&#x20;**`r`**,&#x20;**`w`**,&#x20;**`a`**,&#x20;**`x`**,&#x20;**`r+`**,&#x20;**`w+`**&#x20;and&#x20;**`a+`**.**

**Answer:**

File access modes define how we open and operate on a file.

| Mode | Purpose                                                                 |
| ---- | ----------------------------------------------------------------------- |
| `r`  | Opens an existing file for reading                                      |
| `w`  | Opens a file for writing; overwrites existing content or creates a file |
| `a`  | Opens a file for appending; creates it if it does not exist             |
| `x`  | Creates a new file and raises an error if it already exists             |
| `r+` | Opens an existing file for both reading and writing                     |
| `w+` | Opens a file for reading and writing; truncates existing content        |
| `a+` | Opens a file for reading and appending; creates it if required          |

**Examples:**

Read mode:

```
file1 = open("test.txt", "r")
```

Write mode:

```
file1 = open("test.txt", "w")
```

Append mode:

```
file1 = open("test.txt", "a")
```

Create mode:

```
file1 = open("test.txt", "x")
```

Read/write modes:

```
file1 = open("test.txt", "r+")file1 = open("test.txt", "w+")file1 = open("test.txt", "a+")
```

**Important:** The `w` and `w+` modes remove the previous file contents when opening the file.

### **Q61. What is a File Handler? Explain the syntax for opening and accessing a file.**

**Answer:**

A File Handler is an object returned by Python when we open a file.

It allows us to perform file operations such as reading, writing and appending.

**Syntax:**

```
file_handler = open(filename, mode)
```

Example:

```
file1 = open("test.txt", "r")data = file1.read()print(data)file1.close()
```

Here:

- `test.txt` is the filename.
- `r` is the access mode.
- `file1` is the file handler.
- `read()` reads the file contents.
- `close()` closes the file.

### **Q62. What is the difference between&#x20;**`read()`**,&#x20;**`readline()`**&#x20;and&#x20;**`readlines()`**&#x20;methods?**

**Answer:**

These methods are used to read file contents.

**1. read():**

Reads the file contents and returns them as a string.

```
with open("test.txt", "r") as file1:    data = file1.read()    print(data)
```

**2. readline():**

Reads one line at a time from the current file position.

```
with open("test.txt", "r") as file1:    line1 = file1.readline()    print(line1)
```

**3. readlines():**

Reads all remaining lines and returns them as a list of strings.

```
with open("test.txt", "r") as file1:    lines = file1.readlines()    print(lines)
```

**Difference:**

| read()                            | readline()                      | readlines()                             |
| --------------------------------- | ------------------------------- | --------------------------------------- |
| Reads all remaining content       | Reads one line                  | Reads all remaining lines               |
| Returns a string                  | Returns a string                | Returns a list                          |
| Useful for complete file contents | Useful for line-by-line reading | Useful when we need all lines as a list |

### **Q63. What is the difference between&#x20;**`write()`**&#x20;and&#x20;**`writelines()`**? How do you append data to an existing file?**

**Answer:**

**write():**

The `write()` method writes a string into a file.

Example:

```
with open("test.txt", "w") as file1:    file1.write("Python Programming")
```

**writelines():**

The `writelines()` method writes multiple strings from an iterable into a file.

Example:

```
lines = [    "First line\n",    "Second line\n",    "Third line\n"]with open("test.txt", "w") as file1:    file1.writelines(lines)
```

**Append Data:**

We use append mode `a`.

```
with open("test.txt", "a") as file1:    file1.write("\nNew line")
```

**Difference:**

| write()                              | writelines()                             |
| ------------------------------------ | ---------------------------------------- |
| Writes one string                    | Writes multiple strings from an iterable |
| Does not automatically add a newline | Does not automatically add newlines      |
| Accepts a string                     | Accepts an iterable of strings           |

### **Q64. What is the purpose of the&#x20;**`with`**&#x20;statement in file handling? How is it different from manually closing a file using&#x20;**`close()`**?**

**Answer:**

The `with` statement is used for automatic resource management in Python.

When we use `with` to open a file, Python automatically closes the file after the block completes, even when an exception occurs.

**Without&#x20;**`with`**:**

```
file1 = open("test.txt", "r")data = file1.read()print(data)file1.close()
```

Here, we must manually close the file.

**Using&#x20;**`with`**:**

```
with open("test.txt", "r") as file1:    data = file1.read()    print(data)
```

Here, Python automatically closes the file.

**Difference:**

| Using close()                         | Using with                             |
| ------------------------------------- | -------------------------------------- |
| We manually close the file            | File closes automatically              |
| We must ensure closure on error paths | Automatically handles resource cleanup |
| More code                             | Cleaner and safer structure            |

### **Q65. What are&#x20;**`seek()`**&#x20;and&#x20;**`tell()`**&#x20;methods? Why do we use them?**

**Answer:**

Both methods are used to manage the file cursor position.

**1. tell():**

Returns the current position of the file cursor.

Example:

```
with open("test.txt", "r") as file1:    print(file1.tell())
```

**2. seek():**

Moves the file cursor to a specified position.

Example:

```
with open("test.txt", "r") as file1:    print(file1.tell())    file1.seek(5)    print(file1.tell())
```

If we call `read()` after `seek(5)`, reading starts from the new position.

**Difference:**

| seek()                      | tell()                                |
| --------------------------- | ------------------------------------- |
| Changes the cursor position | Returns the cursor position           |
| Used to move within a file  | Used to identify the current position |

### **Q66. How do you check whether a file exists before opening it? How do you handle a missing file?**

**Answer:**

We can use the `os.path.exists()` method to check whether a file path exists.

Example:

```
import ospath = "test.txt"if os.path.exists(path):    with open(path, "r") as file1:        print(file1.read())else:    print("File does not exist")
```

We can also use exception handling.

```
try:    with open("test.txt", "r") as file1:        print(file1.read())except FileNotFoundError:    print("File not found")
```

The second approach handles the case where a file disappears or becomes unavailable between checking and opening.

### **Q67. Write Python programs for the following file operations.**

**Answer:**

**1. Count the number of lines, words and characters in a file**

```
with open("test.txt", "r") as file1:    data = file1.read()lines = data.splitlines()words = data.split()characters = len(data)print("Lines:", len(lines))print("Words:", len(words))print("Characters:", characters)
```

**2. Count the occurrence of the keyword&#x20;**`Failed`

```
with open("test.txt", "r") as file1:    data = file1.read()count = data.count("Failed")print(count)
```

This counts non-overlapping exact, case-sensitive occurrences.

**3. Search for a particular string and return line numbers**

```
def search_string(filename, keyword):    result = []    with open(filename, "r") as file1:        for line_no, line in enumerate(file1, start=1):            if keyword in line:                result.append(line_no)    return resultprint(search_string("test.txt", "Failed"))
```

**4. Find and replace all occurrences of a string**

```
with open("test.txt", "r") as file1:    data = file1.read()data = data.replace("Failed", "Passed")with open("test.txt", "w") as file1:    file1.write(data)
```

**5. Copy the contents of one file into another**

```
with open("source.txt", "r") as file1:    data = file1.read()with open("destination.txt", "w") as file2:    file2.write(data)
```

**6. Merge multiple text files into a single file**

```
files = ["file1.txt", "file2.txt", "file3.txt"]with open("merged.txt", "w") as output:    for filename in files:        with open(filename, "r") as file1:            data = file1.read()            output.write(data)            output.write("\n")
```

**7. Sort the lines of a text file alphabetically and save them to a new file**

```
with open("input.txt", "r") as file1:    lines = file1.readlines()lines.sort()with open("sorted.txt", "w") as file2:    file2.writelines(lines)
```

### **Q68. Write Python programs for the following advanced file operations.**

**Answer:**

**1. Reverse the contents of a file**

This program reverses the character sequence in the file.

```
with open("test.txt", "r") as file1:    data = file1.read()reverse_data = data[::-1]with open("reverse.txt", "w") as file1:    file1.write(reverse_data)
```

**2. Count the occurrences of each word**

```
with open("test.txt", "r") as file1:    data = file1.read().lower()words = data.split()result = {}for word in words:    if word in result:        result[word] += 1    else:        result[word] = 1print(result)
```

**3. Return a list of unique words**

```
with open("test.txt", "r") as file1:    data = file1.read().lower()words = data.split()result = []for word in words:    if word not in result:        result.append(word)print(result)
```

**4. Return lines containing only lowercase characters**

```
result = []with open("test.txt", "r") as file1:    for line in file1:        if line.strip() and line.strip().islower():            result.append(line)print(result)
```

Here, `islower()` checks that the line has at least one cased character and all its cased characters are lowercase.

**5. Count lines containing more than a specified number of characters**

```
count = 0with open("test.txt", "r") as file1:    for line in file1:        if len(line.rstrip("\n")) > 10:            count += 1print(count)
```

Here, the program counts lines containing more than 10 characters, excluding the newline character.

### **Q69. What is JSON in Python? Explain&#x20;**`json.load()`**,&#x20;**`json.dump()`**,&#x20;**`json.loads()`**&#x20;and&#x20;**`json.dumps()`**. How do you read and write JSON files?**

**Answer:**

JSON stands for JavaScript Object Notation.

It is a data format used to store and exchange information between systems.

Python provides the built-in `json` module to work with JSON data.

**Example JSON:**

```
{
    "name": "John",
    "age": 30,
    "city": "London"
}
```

**1.&#x20;**`json.load()`**:**

Reads JSON data from a file and converts it into Python objects.

```
import jsonwith open("data.json", "r") as file1:    data = json.load(file1)print(data)
```

**2.&#x20;**`json.dump()`**:**

Writes Python objects into a JSON file.

```
import jsondata = {    "name": "John",    "age": 30}with open("data.json", "w") as file1:    json.dump(data, file1)
```

**3.&#x20;**`json.loads()`**:**

Converts a JSON string into Python objects.

```
import jsondata = '{"name":"John","age":30}'result = json.loads(data)print(result)
```

**4.&#x20;**`json.dumps()`**:**

Converts Python objects into a JSON string.

```
import jsondata = {    "name": "John",    "age": 30}result = json.dumps(data)print(result)
```

**Difference:**

| Method    | Purpose                                 |
| --------- | --------------------------------------- |
| `load()`  | Reads JSON from a file                  |
| `dump()`  | Writes JSON to a file                   |
| `loads()` | Converts JSON string into Python object |
| `dumps()` | Converts Python object into JSON string |

# **Section 8 – Python Modules, OS and System Operations**

### **Q70. What is a Module in Python? What is the difference between a Module and a Package?**

**Answer:**

A Module is a reusable Python file containing functions, variables and classes.

For example, `test.py` can contain multiple functions and variables.

We can import and reuse those functions in another Python file.

**Example – test.py:**

```
def add(a, b):    return a + bdef sub(a, b):    return a - b
```

**Importing the Module:**

```
import testprint(test.add(10, 20))
```

**Package:**

A Package is a way of organizing related Python modules into a directory hierarchy.

**Difference:**

| Module                                    | Package                           |
| ----------------------------------------- | --------------------------------- |
| A single Python module file               | A collection of related modules   |
| Generally a `.py` file                    | Generally a directory             |
| Contains functions, variables and classes | Organizes modules and subpackages |

### **Q71. What are the different types of Python modules? Explain Built-in, User-Defined and External Modules.**

**Answer:**

According to my notes, there are three types of modules.

**1. Built-in Modules:**

These modules are provided with Python.

Examples:

- `math`
- `os`
- `sys`
- `time`
- `re`
- `datetime`

**2. User-Defined Modules:**

These are modules created by developers.

Example:

`test.py`

```
def add(a, b):    return a + b
```

**3. External Modules:**

These modules are installed separately using a package manager such as PIP.

Examples:

- PyTest.
- Paramiko.
- NumPy.
- Pandas.

### **Q72. How do you import modules and functions in Python? Explain&#x20;**`import`**,&#x20;**`from ... import`**&#x20;and&#x20;**`import ... as`**.**

**Answer:**

Python provides different ways to import modules and their functions.

**1. Import an entire module:**

```
import mathprint(math.sqrt(25))
```

**2. Import a particular function:**

```
from math import sqrtprint(sqrt(25))
```

**3. Import multiple functions:**

```
from math import sqrt, factorial
```

**4. Import all functions:**

```
from math import *
```

This is generally discouraged in larger programs because names can collide.

**5. Import using an alias:**

```
import math as mprint(m.sqrt(25))
```

**6. Import a user-defined module:**

```
import testprint(test.add(10, 20))
```

### **Q73. What is PIP in Python? Explain the commands used to install, list, uninstall and upgrade packages.**

**Answer:**

PIP stands for Pip Installs Packages.

It is the package installer used to install and manage external Python packages.

**1. Install a package:**

```
pip install pytest
```

**2. List installed packages:**

```
pip list
```

**3. Uninstall a package:**

```
pip uninstall pytest
```

**4. Upgrade a package:**

```
pip install --upgrade pytest
```

**5. Check PIP version:**

```
pip --version
```

**6. Show package details:**

```
pip show pytest
```

### **Q74. What is the purpose of the&#x20;**`os`**&#x20;module? Explain commonly used methods such as&#x20;**`getcwd()`**,&#x20;**`chdir()`**,&#x20;**`listdir()`**,&#x20;**`mkdir()`**,&#x20;**`makedirs()`**,&#x20;**`rmdir()`**,&#x20;**`remove()`**&#x20;and&#x20;**`rename()`**.**

**Answer:**

The `os` module is a built-in Python module used to interact with the operating system.

It allows us to perform file, directory and operating-system operations.

First, import the module:

```
import os
```

**Important OS Methods:**

| Method          | Purpose                               |
| --------------- | ------------------------------------- |
| `os.getcwd()`   | Gets the current working directory    |
| `os.chdir()`    | Changes the current working directory |
| `os.listdir()`  | Lists files and directories           |
| `os.mkdir()`    | Creates one directory                 |
| `os.makedirs()` | Creates nested directories            |
| `os.rmdir()`    | Removes an empty directory            |
| `os.remove()`   | Removes a file                        |
| `os.rename()`   | Renames a file or directory           |

**Examples:**

```
import osprint(os.getcwd())os.chdir("/home/user")print(os.getcwd())print(os.listdir())os.mkdir("test")os.makedirs("parent/child")os.rename("test", "new_test")os.rmdir("new_test")os.remove("file.txt")
```

### **Q75. Explain commonly used&#x20;**`os.path`**&#x20;methods such as&#x20;**`exists()`**,&#x20;**`isfile()`**,&#x20;**`isdir()`**,&#x20;**`join()`**,&#x20;**`abspath()`**&#x20;and&#x20;**`realpath()`**.**

**Answer:**

`os.path` provides methods for checking and manipulating file paths.

**1. exists():**

Checks whether a path exists.

```
os.path.exists("test.txt")
```

**2. isfile():**

Checks whether the given path is a file.

```
os.path.isfile("test.txt")
```

**3. isdir():**

Checks whether the path is a directory.

```
os.path.isdir("test")
```

**4. join():**

Combines multiple path components into one path using the platform's path separator.

```
path = os.path.join("home", "user", "test.txt")print(path)
```

**5. abspath():**

Returns the absolute path.

```
print(os.path.abspath("test.txt"))
```

**6. realpath():**

Returns the resolved path, including following symbolic links where applicable.

```
print(os.path.realpath("test.txt"))
```

### **Q76. Write Python programs using the&#x20;**`os`**&#x20;module for the following operations.**

**Answer:**

**1. Check whether a given path exists**

```
import ospath = "test.txt"if os.path.exists(path):    print("Path exists")else:    print("Path does not exist")
```

**2. Print the current working directory**

```
import osprint(os.getcwd())
```

**3. Change the current working directory**

```
import osos.chdir("/home/user")print(os.getcwd())
```

**4. Create and remove directories**

```
import osos.mkdir("test")os.rmdir("test")
```

**5. Count the number of files and folders in a directory**

```
import ospath = "test_folder"file_count = 0folder_count = 0for item in os.listdir(path):    full_path = os.path.join(path, item)    if os.path.isfile(full_path):        file_count += 1    elif os.path.isdir(full_path):        folder_count += 1print("Files:", file_count)print("Folders:", folder_count)
```

**6. Recursively list all files and directories**

```
import ospath = "test_folder"for root, dirs, files in os.walk(path):    for directory in dirs:        print("Directory:", os.path.join(root, directory))    for file in files:        print("File:", os.path.join(root, file))
```

**7. Print absolute paths of all files**

```
import ospath = "test_folder"for root, dirs, files in os.walk(path):    for file in files:        full_path = os.path.join(root, file)        print(os.path.abspath(full_path))
```

**8. Find all Python files in a directory**

```
import ospath = "test_folder"for root, dirs, files in os.walk(path):    for file in files:        if file.endswith(".py"):            print(os.path.join(root, file))
```

**9. Find the directory of the currently running script**

```
import osscript_dir = os.path.dirname(os.path.abspath(__file__))print(script_dir)
```

`__file__` represents the path of the current Python script.

### **Q77. What is the difference between&#x20;**`os.system()`**&#x20;and&#x20;**`os.popen()`**? What are their purposes?**

**Answer:**

Both functions are provided by the `os` module and are used to execute operating-system commands.

**1. os.system():**

Executes an operating-system command in a subshell.

It returns the command's exit status.

Example:

```
import osresult = os.system("ls")print(result)
```

**2. os.popen():**

Executes a command and provides a file-like object through which we can read its output.

Example:

```
import osresult = os.popen("ls")output = result.read()print(output)result.close()
```

**Difference:**

| os.system()                               | os.popen()                           |
| ----------------------------------------- | ------------------------------------ |
| Executes a system command                 | Executes a system command            |
| Returns command status                    | Returns a file-like object           |
| Does not directly provide captured output | Allows us to read command output     |
| Used for simple command execution         | Used when command output is required |

**Additional clarification:** The recommended modern approach for running external commands and managing output, errors and exit status is generally the `subprocess` module.

### **Q78. What is the&#x20;**`subprocess`**&#x20;module? How do you execute operating-system commands and capture their output using&#x20;**`subprocess.run()`**&#x20;and&#x20;**`subprocess.Popen()`**?**

**Answer:**

The `subprocess` module is used to execute external system commands from Python.

It supports interaction with operating-system processes.

**1. subprocess.run():**

Used to execute a command and wait for it to complete.

Example:

```
import subprocessresult = subprocess.run(    ["ls", "-l"],    capture_output=True,    text=True)print(result.stdout)print(result.returncode)
```

Here:

- `stdout` contains standard output.
- `stderr` contains standard error.
- `returncode` contains the exit status.

**2. subprocess.Popen():**

Used to start a process and interact with it while it is running.

Example:

```
import subprocessprocess = subprocess.Popen(    ["ping", "-c", "4", "127.0.0.1"],    stdout=subprocess.PIPE,    stderr=subprocess.PIPE,    text=True)stdout, stderr = process.communicate()print(stdout)print(stderr)print(process.returncode)
```

**Difference:**

| subprocess.run()                        | subprocess.Popen()                       |
| --------------------------------------- | ---------------------------------------- |
| Simpler high-level interface            | Lower-level process-control interface    |
| Waits for command completion by default | Starts process and returns immediately   |
| Suitable for normal command execution   | Suitable for ongoing process interaction |
| Returns CompletedProcess                | Returns Popen object                     |

### **Q79. What is the purpose of the&#x20;**`sys`**&#x20;module? Explain&#x20;**`sys.path`**,&#x20;**`sys.exit()`**,&#x20;**`sys.argv`**,&#x20;**`sys.platform`**,&#x20;**`sys.version`**,&#x20;**`sys.version_info`**&#x20;and&#x20;**`sys.getsizeof()`**.**

**Answer:**

The `sys` module is a built-in Python module used to interact with the Python interpreter and runtime environment.

Import it using:

```
import sys
```

**Important methods and attributes:**

| Method / Attribute | Purpose                                        |
| ------------------ | ---------------------------------------------- |
| `sys.path`         | Displays module search paths                   |
| `sys.exit()`       | Terminates the Python program                  |
| `sys.argv`         | Stores command-line arguments                  |
| `sys.platform`     | Provides platform identifier                   |
| `sys.version`      | Displays Python version information            |
| `sys.version_info` | Provides Python version components             |
| `sys.getsizeof()`  | Returns the shallow size of an object in bytes |

**Examples:**

Python version:

```
print(sys.version)
```

Platform information:

```
print(sys.platform)
```

Module paths:

```
print(sys.path)
```

Object size:

```
x = [1, 2, 3]print(sys.getsizeof(x))
```

Exit the program:

```
sys.exit()
```

### **Q80. What is the difference between&#x20;**`input()`**&#x20;and&#x20;**`sys.argv`**? How do you pass command-line arguments to a Python program?**

**Answer:**

Both are used to receive input in Python, but they work differently.

**input():**

Used to receive input from the user while the program is running.

Example:

```
name = input("Enter your name: ")print(name)
```

**sys.argv:**

Used to receive command-line arguments passed when executing the Python script.

Example file: `test.py`

```
import sysprint(sys.argv)
```

Execution:

```
python test.py 10 20
```

Output:

```
['test.py', '10', '20']
```

To access the values:

```
import sysa = int(sys.argv[1])b = int(sys.argv[2])print(a + b)
```

Output:

```
30
```

**Difference:**

| input()                              | sys.argv                                           |
| ------------------------------------ | -------------------------------------------------- |
| Reads input during program execution | Reads arguments supplied when launching the script |
| Interactive input                    | Command-line input                                 |
| Returns a string by default          | Stores arguments as strings in a list              |

### **Q81. What are the&#x20;**`time`**&#x20;and&#x20;**`datetime`**&#x20;modules? Explain how to obtain the current date/time, add delays and format date/time values.**

**Answer:**

Python provides `time` and `datetime` modules for working with time and dates.

**1. time Module:**

Used for time-related operations.

Example:

```
import timeprint(time.time())
```

This returns the current Unix timestamp.

**To introduce a delay:**

```
time.sleep(5)
```

This pauses program execution for five seconds.

**To display formatted time:**

```
print(time.ctime())
```

**2. datetime Module:**

Used to work with date and time objects.

Example:

```
import datetimedate1 = datetime.datetime.now()print(date1)
```

**To display the current date:**

```
print(datetime.date.today())
```

**To format the date:**

```
date1 = datetime.datetime.now()print(date1.strftime("%d-%m-%Y"))
```

**To convert a string into a datetime object:**

```
date1 = datetime.datetime.strptime(    "2026-11-23",    "%Y-%m-%d")print(date1)
```

**Important Formatting Codes:**

| Code | Purpose            |
| ---- | ------------------ |
| `%d` | Day                |
| `%m` | Month number       |
| `%b` | Short month name   |
| `%B` | Full month name    |
| `%y` | Two-digit year     |
| `%Y` | Four-digit year    |
| `%H` | 24-hour format     |
| `%I` | 12-hour format     |
| `%M` | Minutes            |
| `%S` | Seconds            |
| `%p` | AM/PM              |
| `%A` | Full weekday name  |
| `%a` | Short weekday name |

### **Q82. What is the Paramiko module? How do you establish an SSH connection to a remote Linux server and execute commands using Python?**

**Answer:**

Paramiko is an external Python module used to establish SSH connections to remote machines.

It allows us to:

1. Connect to remote Linux servers.
2. Execute commands remotely.
3. Retrieve command output.
4. Transfer files using supported SSH file-transfer functionality.

**Installation:**

```
pip install paramiko
```

**Example – Establish SSH Connection and Execute a Command:**

```
import paramikohostname = "192.168.0.103"port = 22username = "user"password = "password"ssh = paramiko.SSHClient()ssh.load_system_host_keys()ssh.connect(    hostname=hostname,    port=port,    username=username,    password=password)stdin, stdout, stderr = ssh.exec_command("ls -l")output = stdout.read().decode()error = stderr.read().decode()print("Output:")print(output)print("Error:")print(error)ssh.close()
```

**Explanation:**

1. Import the Paramiko module.
2. Create an SSHClient object.
3. Load trusted host keys.
4. Connect to the remote server.
5. Execute the required command.
6. Collect standard output and standard error.
7. Close the SSH connection.

**Example use case:**

In storage test automation, we can use Paramiko to connect to remote Linux servers and execute commands such as:

```
lsblk
lsscsi
nvme list
dmesg
```

**Security note:** Use trusted host keys rather than blindly accepting any server key. In production automation, credentials should be stored securely rather than hardcoded.

# **Section 9 – Regular Expressions**

### **Q83. What are Regular Expressions (Regex) in Python? Why do we use the&#x20;**`re`**&#x20;module?**

**Answer:**

Regular Expressions are patterns used to search, match, extract and validate information from strings.

Python provides the `re` module to work with regular expressions.

We import it using:

```
import re
```

**Why do we use Regex?**

1. To search for specific patterns.
2. To validate input.
3. To extract information.
4. To find matching strings.
5. To replace specific patterns.

**Example:**

```
import restr1 = "Python version 3.0"result = re.search(r"Python", str1)if result:    print("Match found")else:    print("No match")
```

### **Q84. What is the difference between&#x20;**`re.match()`**&#x20;and&#x20;**`re.search()`**?**

**Answer:**

Both methods are used to find matching patterns in a string.

**1. re.match():**

Checks for a match only at the beginning of the string.

Example:

```
import restr1 = "Python version 3.0"print(re.match("Python", str1))# Match objectprint(re.match("version", str1))# None
```

**2. re.search():**

Searches the entire string and returns the first matching occurrence.

Example:

```
import restr1 = "Python version 3.0"print(re.search("version", str1))# Match object
```

**Difference:**

| re.match()                                   | re.search()                           |
| -------------------------------------------- | ------------------------------------- |
| Checks from the beginning                    | Searches anywhere in the string       |
| Returns match only at the beginning          | Returns the first matching occurrence |
| Returns None if the beginning does not match | Returns None if no match is found     |

### **Q85. What is the purpose of&#x20;**`re.findall()`**&#x20;and&#x20;**`group()`**? How do you extract matching data from a string?**

**Answer:**

**1. re.findall():**

`findall()` returns all non-overlapping matches of a pattern in a string as a list.

Example:

```
import restr1 = "Error 100 Failed 200 Error 300"result = re.findall(r"\d+", str1)print(result)
```

Output:

```
['100', '200', '300']
```

**2. group():**

`group()` is used with a Match object to retrieve the matched text or captured groups.

Example:

```
import restr1 = "Python version 3.0"result = re.search(r"(\w+) version (\d+\.\d+)", str1)if result:    print(result.group())    print(result.group(1))    print(result.group(2))
```

Output:

```
Python version 3.0
Python
3.0
```

**Difference:**

- `findall()` returns all matching results.
- `group()` retrieves matched content from a Match object.

### **Q86. Explain common Regex metacharacters and special sequences such as&#x20;**`^`**,&#x20;**`$`**,&#x20;**`.`**,&#x20;**`*`**,&#x20;**`+`**,&#x20;**`?`**,&#x20;**`\d`**,&#x20;**`\D`**,&#x20;**`\w`**,&#x20;**`\W`**,&#x20;**`\s`**&#x20;and&#x20;**`\S`**.**

**Answer:**

Regular Expressions use special characters to define search patterns.

| Symbol  | Purpose                                                      |
| ------- | ------------------------------------------------------------ |
| `^`     | Matches the beginning of a string                            |
| `$`     | Matches the end of a string                                  |
| `.`     | Matches any character except newline by default              |
| `*`     | Matches zero or more repetitions                             |
| `+`     | Matches one or more repetitions                              |
| `?`     | Matches zero or one repetition                               |
| `{n}`   | Matches exactly n repetitions                                |
| `{n,}`  | Matches at least n repetitions                               |
| `{n,m}` | Matches between n and m repetitions                          |
| `()`    | Creates a capturing group                                    |
| `\`     | Escapes a special character or introduces a special sequence |
| `\d`    | Matches a digit                                              |
| `\D`    | Matches a non-digit                                          |
| `\w`    | Matches a word character                                     |
| `\W`    | Matches a non-word character                                 |
| `\s`    | Matches whitespace                                           |
| `\S`    | Matches non-whitespace                                       |

**Examples:**

Match digits:

```
re.findall(r"\d", "Python123")
```

Output:

```
['1', '2', '3']
```

Match words:

```
re.findall(r"\w+", "Python Programming")
```

Output:

```
['Python', 'Programming']
```

Match whitespace:

```
re.findall(r"\s", "Python Programming")
```

### **Q87. Write regular expressions for the following.**

**Answer:**

**1. Validate an IPv4 address**

An IPv4 address contains four numeric octets separated by dots.

Each octet must be between 0 and 255.

```
import reip = "192.168.0.100"pattern = (    r"^(?:(?:25[0-5]|2[0-4]\d|1\d\d|"    r"[1-9]?\d)\.){3}"    r"(?:25[0-5]|2[0-4]\d|1\d\d|[1-9]?\d)$")if re.match(pattern, ip):    print("Valid IPv4")else:    print("Invalid IPv4")
```

**2. Validate a basic email address**

```
import reemail = "user123@gmail.com"pattern = r"^[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Za-z]{2,}$"if re.match(pattern, email):    print("Valid email")else:    print("Invalid email")
```

This is a practical basic email pattern, not a complete implementation of every valid email format.

**3. Extract a Python version from a string**

```
import restr1 = "Python version 3.10"result = re.search(    r"Python version (\d+\.\d+)",    str1)if result:    print(result.group(1))
```

Output:

```
3.10
```

**4. Extract drive names or device paths such as&#x20;**`/dev/sda`**&#x20;and&#x20;**`/dev/sdb`

```
import restr1 = "/dev/sda /dev/sdb /dev/sdc1"result = re.findall(r"/dev/sd[a-z]\d*", str1)print(result)
```

Output:

```
['/dev/sda', '/dev/sdb', '/dev/sdc1']
```

**5. Extract specific information from a multiline string**

Example:

```
import restr1 = """Employee Name: JohnEmployee ID: 1234Department: Storage"""name = re.search(r"Employee Name:\s*(\w+)", str1)emp_id = re.search(r"Employee ID:\s*(\d+)", str1)department = re.search(r"Department:\s*(\w+)", str1)if name:    print(name.group(1))if emp_id:    print(emp_id.group(1))if department:    print(department.group(1))
```

Output:

```
John
1234
Storage
```

# **Section 10 – Exception Handling**

### **Q88. What are Errors and Exceptions in Python? Explain the difference between Syntax Errors and Runtime Exceptions.**

**Answer:**

Errors are problems that occur in a Python program and prevent it from executing correctly.

There are two important categories:

**1. Syntax Errors:**

Syntax Errors occur when Python code does not follow the correct language syntax.

Example:

```
if x > 10    print(x)
```

The colon is missing.

Python reports a `SyntaxError`.

Syntax errors generally cannot be handled by a `try-except` block surrounding the same invalid code because the code cannot be parsed successfully.

**2. Runtime Exceptions:**

Runtime Exceptions occur while a program is executing.

Examples:

```
print(10 / 0)
```

This raises `ZeroDivisionError`.

```
list1 = [10, 20]print(list1[5])
```

This raises `IndexError`.

We can handle runtime exceptions using `try-except`.

**Difference:**

| Syntax Error                                                   | Runtime Exception                  |
| -------------------------------------------------------------- | ---------------------------------- |
| Occurs when code violates Python syntax                        | Occurs during program execution    |
| Prevents the code from being parsed correctly                  | Occurs after execution has started |
| Examples: Missing colon, invalid syntax                        | ZeroDivisionError, ValueError      |
| Not normally caught by try-except around the same invalid code | Can be handled using try-except    |

### **Q89. What are common exceptions in Python? Explain&#x20;**`NameError`**,&#x20;**`TypeError`**,&#x20;**`ValueError`**,&#x20;**`ZeroDivisionError`**,&#x20;**`IndexError`**,&#x20;**`KeyError`**,&#x20;**`FileNotFoundError`**&#x20;and&#x20;**`AttributeError`**.**

**Answer:**

Python provides different built-in exceptions to identify specific runtime problems.

**1. NameError:**

Occurs when we try to use a variable or name that has not been defined.

```
print(x)
```

**2. TypeError:**

Occurs when an operation is performed using incompatible data types.

```
x = 10y = "Python"print(x + y)
```

**3. ValueError:**

Occurs when the data type is acceptable but the value is invalid for the operation.

```
x = int("abc")
```

**4. ZeroDivisionError:**

Occurs when we divide a number by zero.

```
print(10 / 0)
```

**5. IndexError:**

Occurs when we access an invalid sequence index.

```
list1 = [10, 20]print(list1[5])
```

**6. KeyError:**

Occurs when we access a dictionary key that does not exist.

```
dict1 = {"a": 10}print(dict1["b"])
```

**7. FileNotFoundError:**

Occurs when we try to open a file that does not exist.

```
file1 = open("unknown.txt", "r")
```

**8. AttributeError:**

Occurs when an object does not have the attribute or method being accessed.

```
x = 10x.append(20)
```

### **Q90. What is Exception Handling? Explain&#x20;**`try`**&#x20;and&#x20;**`except`**&#x20;blocks with examples.**

**Answer:**

Exception Handling is used to handle runtime exceptions in Python.

It prevents the program from terminating unexpectedly when a known exception occurs.

We use:

- `try`
- `except`

**try:**

Contains the main code that may raise an exception.

**except:**

Contains the code that handles an exception.

Example:

```
try:    a = 10    b = 0    result = a / b    print(result)except ZeroDivisionError:    print("Cannot divide by zero")
```

Output:

```
Cannot divide by zero
```

### **Q91. Can we define multiple&#x20;**`except`**&#x20;blocks for one&#x20;**`try`**&#x20;block? Why is the order of exception handling important?**

**Answer:**

Yes. We can define multiple `except` blocks for one `try` block.

It allows us to handle different exception types separately.

Example:

```
try:    x = int(input("Enter a number: "))    result = 10 / x    print(result)except ValueError:    print("Enter a valid integer")except ZeroDivisionError:    print("Cannot divide by zero")except Exception as err:    print("Unexpected error:", err)
```

**Why is order important?**

Specific exceptions should generally be handled before general exceptions.

For example, `ZeroDivisionError` should appear before `Exception`.

If we place a general `Exception` handler first, it may catch errors that should have been handled by more specific blocks.

### **Q92. What are the purposes of&#x20;**`else`**&#x20;and&#x20;**`finally`**&#x20;blocks in exception handling?**

**Answer:**

Python provides two additional blocks.

**1. else:**

The `else` block executes only when no exception occurs in the `try` block.

Example:

```
try:    result = 10 / 2except ZeroDivisionError:    print("Error")else:    print("Result:", result)
```

Output:

```
Result: 5.0
```

**2. finally:**

The `finally` block executes whether an exception occurs or not.

It is commonly used for cleanup operations.

Example:

```
try:    print(10 / 2)except ZeroDivisionError:    print("Error")else:    print("No error")finally:    print("Finally block executed")
```

**Difference:**

| else                                            | finally                                     |
| ----------------------------------------------- | ------------------------------------------- |
| Executes when no exception occurs               | Executes whether an exception occurs or not |
| Used for code dependent on successful execution | Used for cleanup operations                 |

### **Q93. What is the purpose of the&#x20;**`raise`**&#x20;keyword? How do you create and raise a custom exception in Python?**

**Answer:**

The `raise` keyword is used to generate an exception manually.

We use it when a particular condition should be treated as an error.

**Example:**

```
x = 50if x < 100:    raise Exception("Value should be greater than or equal to 100")
```

**Custom Exception:**

We can create our own exception class by inheriting from the built-in `Exception` class.

Example:

```
class InvalidAgeError(Exception):    passage = 16try:    if age < 18:        raise InvalidAgeError("Age must be 18 or above")except InvalidAgeError as err:    print(err)
```

Output:

```
Age must be 18 or above
```

Custom exceptions help us represent application-specific errors clearly.

# **Section 11 – Object-Oriented Programming (OOP)**

### **Q94. What is Object-Oriented Programming in Python? Explain its four fundamental principles.**

**Answer:**

OOP stands for Object-Oriented Programming.

It is a programming approach in which we organize code using classes and objects.

A class contains attributes and methods, and objects are created from classes.

**Advantages of OOP:**

1. Code reusability.
2. Better organization.
3. Data security through encapsulation.
4. Easier maintenance.
5. Helps represent real-world entities.

**Four Fundamental Principles:**

**1. Inheritance:**

Inheritance allows a child class to inherit properties and methods from a parent class.

**2. Encapsulation:**

Encapsulation is the process of combining data and methods within a class and controlling access to the data.

**3. Polymorphism:**

Polymorphism means one method or interface can behave differently depending on the object or input.

**4. Abstraction:**

Abstraction means hiding implementation details and exposing only the required functionality.

### **Q95. What is a Class and what is an Object? Explain their differences with examples.**

**Answer:**

**Class:**

A class is a blueprint used to create objects.

It contains attributes and methods.

We define a class using the `class` keyword.

**Object:**

An object is an instance of a class.

Using objects, we can access the attributes and methods defined inside the class.

Example:

```
class Student:    name = "John"    age = 25    def display(self):        print(self.name, self.age)obj1 = Student()obj1.display()
```

Output:

```
John 25
```

**Difference:**

| Class                                 | Object                                 |
| ------------------------------------- | -------------------------------------- |
| Blueprint for creating objects        | Instance of a class                    |
| Defines attributes and methods        | Uses class attributes and methods      |
| Defined using `class`                 | Created by calling the class           |
| One class can create multiple objects | Each object has its own instance state |

### **Q96. What are&#x20;**`__new__()`**&#x20;and&#x20;**`__init__()`**&#x20;methods in Python? What is the difference between them?**

**Answer:**

Both `__new__()` and `__init__()` are special methods involved in object creation.

**1.&#x20;**`__new__()`**:**

`__new__()` is responsible for creating and returning a new object instance.

It is called before `__init__()`.

**2.&#x20;**`__init__()`**:**

`__init__()` initializes the attributes of the newly created object.

It is called after `__new__()` successfully returns an instance.

Example:

```
class Student:    def __new__(cls):        print("Object creation")        return super().__new__(cls)    def __init__(self):        print("Object initialization")obj = Student()
```

Output:

```
Object creation
Object initialization
```

**Difference:**

| `__new__()`                                                   | `__init__()`                       |
| ------------------------------------------------------------- | ---------------------------------- |
| Creates the object                                            | Initializes the object             |
| Called first                                                  | Called after `__new__()`           |
| Takes `cls` as its first argument                             | Takes `self` as its first argument |
| Must return an instance for normal initialization to continue | Returns `None`                     |

### **Q97. Can we create a class without explicitly defining&#x20;**`__init__()`**&#x20;and&#x20;**`__new__()`**? Can we use&#x20;**`return`**&#x20;inside&#x20;**`__init__()`**?**

**Answer:**

**1. Can we create a class without&#x20;**`__init__()`**&#x20;and&#x20;**`__new__()`**?**

Yes.

Python automatically provides inherited object-creation and initialization behaviour through the base `object` class.

Example:

```
class Student:    passobj = Student()print(type(obj))
```

Output:

```
<class '__main__.Student'>
```

**2. Can we use&#x20;**`return`**&#x20;inside&#x20;**`__init__()`**?**

The `__init__()` method must return `None`.

We can use an empty `return` statement:

```
def __init__(self):    return
```

But we cannot return another value.

Incorrect example:

```
class Student:    def __init__(self):        return 100obj = Student()
```

This raises a `TypeError` because `__init__()` must return `None`.

### **Q98. What is&#x20;**`self`**&#x20;in Python? Why is it used in instance methods?**

**Answer:**

`self` represents the current object instance.

It is used to access the instance variables and instance methods inside a class.

It is passed automatically when we call an instance method through an object.

Example:

```
class Student:    def __init__(self, name):        self.name = name    def display(self):        print(self.name)obj1 = Student("John")obj1.display()
```

Output:

```
John
```

Here:

- `self.name` refers to the current object's name.
- `obj1` is passed as the instance to the method.

**Important:** `self` is a conventional parameter name, not a Python keyword.

### **Q99. What are Class Variables and Instance Variables? Explain their differences with examples.**

**Answer:**

**Class Variables:**

Class variables are defined inside a class but outside its instance methods.

They are shared by instances unless an instance overrides the attribute with its own value.

**Instance Variables:**

Instance variables are defined using `self` and belong to individual objects.

Example:

```
class Student:    college = "ABC College"    def __init__(self, name, age):        self.name = name        self.age = ageobj1 = Student("John", 20)obj2 = Student("Alice", 22)print(obj1.college)print(obj2.college)print(obj1.name)print(obj2.name)
```

**Difference:**

| Class Variable                     | Instance Variable               |
| ---------------------------------- | ------------------------------- |
| Defined at class level             | Defined using `self`            |
| Shared by instances by default     | Belongs to an individual object |
| Accessed through class or instance | Accessed through an instance    |
| Used for common data               | Used for object-specific data   |

### **Q100. What are the different types of methods in Python? Explain Instance Methods, Class Methods and Static Methods.**

**Answer:**

There are three major types of methods in Python classes.

1. Instance Method.
2. Class Method.
3. Static Method.

**1. Instance Method:**

An instance method operates on an individual object.

It uses `self` as its first argument.

```
class Student:    def display(self):        print("Instance Method")obj = Student()obj.display()
```

**2. Class Method:**

A class method operates on class-level data.

It uses `cls` as its first argument and is decorated using `@classmethod`.

```
class Student:    college = "ABC"    @classmethod    def display(cls):        print(cls.college)Student.display()
```

**3. Static Method:**

A static method is a method that does not require automatic access to the instance or class.

It is decorated using `@staticmethod`.

```
class Student:    @staticmethod    def add(a, b):        print(a + b)Student.add(10, 20)
```

**Difference:**

| Instance Method                      | Class Method          | Static Method                    |
| ------------------------------------ | --------------------- | -------------------------------- |
| Uses `self`                          | Uses `cls`            | Does not require `self` or `cls` |
| Works with instance data             | Works with class data | Independent utility method       |
| Uses no special decorator by default | Uses `@classmethod`   | Uses `@staticmethod`             |

### **Q101. What is Inheritance? Explain Single-Level, Multilevel, Multiple and Hierarchical Inheritance with examples.**

**Answer:**

Inheritance is an OOP concept in which a child class inherits properties and methods from a parent class.

It helps us reuse existing code.

According to my notes, important inheritance types include:

**1. Single-Level Inheritance:**

One child class inherits from one parent class.

```
class A:    def method1(self):        print("Parent class")class B(A):    def method2(self):        print("Child class")obj = B()obj.method1()obj.method2()
```

**2. Multilevel Inheritance:**

A class inherits from another child class, forming an inheritance chain.

```
class A:    def method1(self):        print("Grandfather")class B(A):    def method2(self):        print("Father")class C(B):    def method3(self):        print("Son")obj = C()obj.method1()obj.method2()obj.method3()
```

**3. Multiple Inheritance:**

One child class inherits from multiple parent classes.

```
class A:    def method1(self):        print("Parent A")class B:    def method2(self):        print("Parent B")class C(A, B):    def method3(self):        print("Child")obj = C()obj.method1()obj.method2()obj.method3()
```

**4. Hierarchical Inheritance:**

Multiple child classes inherit from the same parent class.

```
class A:    def display(self):        print("Parent class")class B(A):    passclass C(A):    passobj1 = B()obj2 = C()obj1.display()obj2.display()
```

### **Q102. What is Multiple Inheritance? Can a Python class inherit from multiple parent classes? Explain with a code example.**

**Answer:**

Multiple Inheritance is an inheritance mechanism in which one child class inherits from two or more parent classes.

Yes, Python supports Multiple Inheritance.

Example:

```
class Father:    def father_method(self):        print("Father method")class Mother:    def mother_method(self):        print("Mother method")class Child(Father, Mother):    passobj = Child()obj.father_method()obj.mother_method()
```

Output:

```
Father method
Mother method
```

The child class can access methods from both parent classes.

### **Q103. What is the purpose of the&#x20;**`super()`**&#x20;keyword? How do we use it to access parent-class methods and constructors?**

**Answer:**

`super()` is used to access methods from the next class in the Method Resolution Order.

It is commonly used to:

1. Call parent-class constructors.
2. Access inherited methods.
3. Extend parent-class functionality.
4. Avoid directly repeating parent initialization logic.

Example:

```
class Father:    def __init__(self, name):        self.name = name    def display(self):        print("Father method")class Son(Father):    def __init__(self, name, age):        super().__init__(name)        self.age = ageobj = Son("John", 25)print(obj.name)print(obj.age)obj.display()
```

Output:

```
John
25
Father method
```

### **Q104. What is MRO (Method Resolution Order)? How does Python determine which method to execute in Multiple Inheritance?**

**Answer:**

MRO stands for Method Resolution Order.

It defines the order in which Python searches parent classes for methods and attributes.

When a child class inherits from multiple parent classes and the same method exists in more than one parent, MRO determines which method is called.

Example:

```
class A:    def display(self):        print("Class A")class B:    def display(self):        print("Class B")class C(A, B):    passobj = C()obj.display()
```

Output:

```
Class A
```

Because class A appears before class B in the inheritance declaration.

**To check MRO:**

```
print(C.mro())
```

Output:

```
[<class '__main__.C'>,
 <class '__main__.A'>,
 <class '__main__.B'>,
 <class 'object'>]
```

Python uses the C3 Method Resolution Order algorithm to determine the order.

### **Q105. What is Encapsulation in Python? How does it protect data and organize methods within a class?**

**Answer:**

Encapsulation is an OOP concept in which data and methods are grouped together inside a class.

It also controls access to the data.

We can use methods such as getters and setters to access and update values instead of directly exposing internal state.

Example:

```
class Employee:    def __init__(self, salary):        self.__salary = salary    def get_salary(self):        return self.__salary    def set_salary(self, salary):        if salary > 0:            self.__salary = salaryobj = Employee(30000)print(obj.get_salary())obj.set_salary(40000)print(obj.get_salary())
```

Output:

```
30000
40000
```

The variable `__salary` is private by naming convention and name mangling.

**Advantages:**

1. Better data protection.
2. Controlled access to attributes.
3. Better code organization.
4. Easier maintenance.

### **Q106. What are Public, Protected and Private attributes in Python? Explain their naming conventions and accessibility.**

**Answer:**

Python supports naming conventions to indicate the intended accessibility of class attributes.

There are three common categories.

**1. Public Attributes:**

Public attributes can be accessed from inside and outside the class.

Example:

```
class Student:    def __init__(self):        self.name = "John"obj = Student()print(obj.name)
```

**2. Protected Attributes:**

Protected attributes are conventionally prefixed with a single underscore `_`.

They are intended for internal use by the class and its subclasses.

Example:

```
class Student:    def __init__(self):        self._marks = 90obj = Student()print(obj._marks)
```

Python does not enforce strict access restrictions on protected attributes.

**3. Private Attributes:**

Private attributes are conventionally prefixed with two underscores `__`.

Python applies name mangling to avoid accidental access or name collisions in subclasses.

Example:

```
class Student:    def __init__(self):        self.__marks = 90obj = Student()# print(obj.__marks)# Raises AttributeError
```

Internally, the name becomes similar to:

```
obj._Student__marks
```

**Difference:**

| Public                   | Protected                              | Private                                     |
| ------------------------ | -------------------------------------- | ------------------------------------------- |
| `name`                   | `_name`                                | `__name`                                    |
| No access restriction    | Intended for class/subclass use        | Name mangling is applied                    |
| Can be accessed directly | Can be accessed directly by convention | Accessed through its mangled name if needed |

### **Q107. What are Getter and Setter methods? Why are they important in Encapsulation?**

**Answer:**

Getter and Setter methods are used to access and modify private or controlled attributes.

**Getter:**

A Getter method returns the value of an attribute.

**Setter:**

A Setter method updates the value of an attribute after applying any required validation.

Example:

```
class Student:    def __init__(self, marks):        self.__marks = marks    def get_marks(self):        return self.__marks    def set_marks(self, marks):        if 0 <= marks <= 100:            self.__marks = marks        else:            print("Invalid marks")obj = Student(80)print(obj.get_marks())obj.set_marks(95)print(obj.get_marks())
```

Output:

```
80
95
```

**Why are they important?**

1. They provide controlled access to attributes.
2. They allow validation.
3. They help protect internal data.
4. They support Encapsulation.

### **Q108. What is Polymorphism in Python? Explain different ways of implementing polymorphism.**

**Answer:**

Polymorphism means many forms.

In OOP, it allows the same interface or method name to behave differently depending on the object or input.

My notes cover different ways to achieve polymorphism.

**1. Polymorphism using Built-in Functions:**

The same function can operate on different data types.

Example:

```
print(len("Python"))print(len([1, 2, 3]))print(len((10, 20, 30)))
```

Output:

```
6
3
3
```

**2. Method Overloading-like Behaviour:**

Python does not support traditional compile-time method overloading based on different parameter signatures in the same way as languages such as Java.

However, we can achieve similar behaviour using default arguments or variable-length arguments.

Example:

```
class Calculator:    def add(self, *args):        total = 0        for num in args:            total += num        return totalobj = Calculator()print(obj.add(10, 20))print(obj.add(10, 20, 30))
```

**3. Method Overriding:**

A child class can provide its own implementation of a method defined in the parent class.

Example:

```
class Animal:    def sound(self):        print("Animal sound")class Dog(Animal):    def sound(self):        print("Bark")class Cat(Animal):    def sound(self):        print("Meow")obj1 = Dog()obj2 = Cat()obj1.sound()obj2.sound()
```

Output:

```
Bark
Meow
```

### **Q109. What is the difference between Method Overloading and Method Overriding? Explain how Python supports both concepts.**

**Answer:**

**Method Overloading:**

Method overloading means defining methods with the same name but different parameter lists.

Python does not support traditional method overloading based only on different parameter signatures.

We can achieve similar behaviour using:

- Default arguments.
- `*args`.
- `**kwargs`.

Example:

```
class Calculator:    def add(self, *args):        total = 0        for num in args:            total += num        return totalobj = Calculator()print(obj.add(10, 20))print(obj.add(10, 20, 30))
```

**Method Overriding:**

Method overriding occurs when a child class defines a method with the same name as a method in its parent class.

Example:

```
class Parent:    def display(self):        print("Parent method")class Child(Parent):    def display(self):        print("Child method")obj = Child()obj.display()
```

Output:

```
Child method
```

**Difference:**

| Method Overloading                                          | Method Overriding                                          |
| ----------------------------------------------------------- | ---------------------------------------------------------- |
| Same method name with different argument patterns           | Child class provides a new implementation of parent method |
| Python uses flexible arguments to achieve similar behaviour | Python supports overriding directly                        |
| Commonly associated with one class                          | Involves inheritance                                       |
| Based on accepted arguments                                 | Based on the runtime object and MRO                        |

### **Q110. What is Abstraction in Python? What is the purpose of Abstract Classes and the&#x20;**`@abstractmethod`**&#x20;decorator?**

**Answer:**

Abstraction is an OOP concept used to hide internal implementation details and expose only the required functionality.

In Python, we can achieve Abstraction using Abstract Classes and Abstract Methods.

We use the `abc` module.

Example:

```
from abc import ABC, abstractmethodclass Vehicle(ABC):    @abstractmethod    def show_details(self):        passclass Car(Vehicle):    def show_details(self):        print("Car details")obj = Car()obj.show_details()
```

Output:

```
Car details
```

**Abstract Class:**

An Abstract Class is a class that cannot be instantiated directly while it contains unimplemented abstract methods.

**Abstract Method:**

An Abstract Method is a method declared using the `@abstractmethod` decorator.

The child class must implement the abstract methods before it can be instantiated.

**Purpose of&#x20;**`@abstractmethod`**:**

1. Defines methods that child classes must implement.
2. Provides a common interface.
3. Enforces required functionality.
4. Helps organize large applications.

### **Q111. How does Garbage Collection work in Python? How does Python manage memory and clean up unused objects?**

**Answer:**

Python automatically manages memory using its memory management system.

Objects are created in memory, and Python manages their allocation and cleanup.

One important mechanism is Reference Counting.

**Reference Counting:**

Python tracks how many references point to an object.

When an object's reference count becomes zero, it can generally be reclaimed.

**Garbage Collection:**

Python also uses a garbage collector to identify and collect unreachable reference cycles.

Example:

```
import gcgc.collect()
```

This requests garbage collection.

**Memory Management Process:**

1. We create variables and objects.
2. Python allocates memory.
3. References point to the objects.
4. When references are removed, reference counts can decrease.
5. Unreachable objects become eligible for cleanup.
6. Garbage collection handles cyclic references that reference counting alone cannot reclaim.

Python performs most memory-management operations automatically.

# **Section 12 – Advanced Python and Coding Standards**

### **Q113. What is a Decorator in Python? How does it extend the functionality of an existing function without modifying its original code?**

**Answer:**

A Decorator is a special type of function used to add additional functionality to another function without modifying its original source code.

A decorator takes a function as an argument and returns a wrapper function.

We use the `@` symbol to apply a decorator.

**Example:**

```
def my_decorator(func):    def wrapper():        print("Before function")        func()        print("After function")    return wrapper@my_decoratordef display():    print("Inside function")display()
```

Output:

```
Before function
Inside function
After function
```

**Working Process:**

1. The decorator receives the original function.
2. It defines a wrapper function.
3. The wrapper executes additional operations.
4. It calls the original function.
5. The wrapper is returned.
6. The decorated function executes with the additional behaviour.

### **Q114. Write a decorator to calculate the actual execution time of a function. Can we apply two different decorators to the same function? Explain with an example.**

**Answer:**

Yes, we can apply multiple decorators to the same function.

**1. Decorator to Calculate Execution Time:**

```
from datetime import datetimeimport timedef calculate_time(func):    def wrapper(*args, **kwargs):        start = datetime.now()        result = func(*args, **kwargs)        end = datetime.now()        print("Time taken:", end - start)        return result    return wrapper@calculate_timedef display():    for i in range(5):        print(i)        time.sleep(1)display()
```

The decorator records the start and end times and calculates the execution duration.

**2. Applying Two Different Decorators:**

```
def decorator1(func):    def wrapper():        print("Decorator 1 before")        func()        print("Decorator 1 after")    return wrapperdef decorator2(func):    def wrapper():        print("Decorator 2 before")        func()        print("Decorator 2 after")    return wrapper@decorator1@decorator2def display():    print("Original Function")display()
```

Output:

```
Decorator 1 before
Decorator 2 before
Original Function
Decorator 2 after
Decorator 1 after
```

Decorators are applied from the bottom upward.

The following:

```
@decorator1@decorator2def display():    pass
```

is equivalent to:

```
display = decorator1(decorator2(display))
```

### **Q115. What is the difference between a Generator and a normal function? Explain the&#x20;**`yield`**&#x20;keyword.**

**Answer:**

A Generator is a special type of function that uses the `yield` keyword to produce values one at a time.

It returns a generator object.

**Normal Function:**

A normal function generally returns a result using the `return` keyword.

Example:

```
def display():    return 10print(display())
```

**Generator Function:**

A generator uses `yield` to produce values.

Example:

```
def display():    yield 10    yield 20    yield 30result = display()print(next(result))print(next(result))print(next(result))
```

Output:

```
10
20
30
```

**Difference:**

| Normal Function                     | Generator                                    |
| ----------------------------------- | -------------------------------------------- |
| Uses `return` to return a result    | Uses `yield` to produce values               |
| Returns the result                  | Returns a generator object                   |
| A return ends function execution    | Yield suspends execution and preserves state |
| Usually returns the complete result | Produces values one at a time                |

**Advantages of Generators:**

1. Memory efficient.
2. Useful for large datasets.
3. Values are generated when requested.
4. Maintains execution state between yields.

### **Q116. What is an Iterator in Python? Explain&#x20;**`iter()`**&#x20;and&#x20;**`next()`**. What is the difference between an Iterator and a Generator?**

**Answer:**

An Iterator is an object that allows us to access elements one at a time.

It provides two important methods:

- `__iter__()`
- `__next__()`

**iter():**

Converts an iterable into an iterator.

**next():**

Returns the next element from an iterator.

Example:

```
list1 = [10, 20, 30]it = iter(list1)print(next(it))print(next(it))print(next(it))
```

Output:

```
10
20
30
```

After all elements are consumed, calling `next()` again raises `StopIteration`.

**Difference between Iterator and Generator:**

| Iterator                                   | Generator                                                |
| ------------------------------------------ | -------------------------------------------------------- |
| Any object implementing iterator behaviour | Special kind of iterator                                 |
| Implements `__iter__()` and `__next__()`   | Usually created using a generator function or expression |
| Can be implemented using a class           | Created conveniently using `yield`                       |
| May require more code to implement         | More concise                                             |
| Produces values one at a time              | Produces values one at a time                            |

### **Q117. What is Multithreading in Python? How do you create, start and join multiple threads using the&#x20;**`threading`**&#x20;module?**

**Answer:**

Multithreading is a programming technique that allows multiple threads to execute within one process.

Each thread performs an independent sequence of instructions.

Python provides the `threading` module to implement multithreading.

**Steps:**

1. Import the `threading` module.
2. Create functions for the tasks.
3. Create Thread objects.
4. Start the threads.
5. Use `join()` to wait for completion.

Example:

```
import threadingimport timedef task1():    for i in range(3):        print("Task 1:", i)        time.sleep(1)def task2():    for i in range(3):        print("Task 2:", i)        time.sleep(1)thread1 = threading.Thread(target=task1)thread2 = threading.Thread(target=task2)thread1.start()thread2.start()thread1.join()thread2.join()print("All tasks completed")
```

**Important Methods:**

| Method       | Purpose                                  |
| ------------ | ---------------------------------------- |
| `Thread()`   | Creates a thread                         |
| `start()`    | Starts the thread                        |
| `join()`     | Waits for the thread to complete         |
| `is_alive()` | Checks whether a thread is still running |

**Additional Interview Explanation:**

In standard CPython builds with the Global Interpreter Lock (GIL), threads are especially useful for I/O-bound tasks such as SSH operations, file operations and network communication.

For CPU-bound tasks, multiprocessing may be more suitable when true parallel execution is needed.

### **Q118. What is the&#x20;**`logging`**&#x20;module? How do you configure logging and write DEBUG, INFO, WARNING, ERROR and CRITICAL messages into a log file?**

**Answer:**

The `logging` module is a built-in Python module used to record application messages and execution information.

It helps us monitor programs and troubleshoot errors.

**Different Logging Levels:**

| Level    | Purpose                        |
| -------- | ------------------------------ |
| DEBUG    | Detailed debugging information |
| INFO     | General information            |
| WARNING  | Indicates a potential problem  |
| ERROR    | Indicates an error             |
| CRITICAL | Indicates a serious failure    |

**Example:**

```
import logginglogging.basicConfig(    filename="newfile.log",    level=logging.DEBUG,    format="%(asctime)s %(levelname)s %(message)s")logging.debug("Debug message")logging.info("Information message")logging.warning("Warning message")logging.error("Error message")logging.critical("Critical message")
```

The messages are written to `newfile.log`.

**Why do we use Logging?**

1. To record execution details.
2. To capture errors.
3. To debug automation scripts.
4. To monitor applications.
5. To maintain execution history.

### **Q119. What is the&#x20;**`argparse`**&#x20;module? How do you create command-line arguments and parse them in a Python script?**

**Answer:**

`argparse` is a built-in Python module used to handle command-line arguments.

It allows us to define arguments and parse the values supplied when executing a script.

Example:

```
import argparseparser = argparse.ArgumentParser(    description="Storage Test Script")parser.add_argument(    "--drive",    help="Drive name")parser.add_argument(    "--timeout",    type=int,    default=30,    help="Command timeout")args = parser.parse_args()print("Drive:", args.drive)print("Timeout:", args.timeout)
```

Execution:

```
python test.py --drive nvme0 --timeout 60
```

Output:

```
Drive: nvme0
Timeout: 60
```

**Advantages:**

1. Easy command-line input handling.
2. Supports optional and required arguments.
3. Supports argument validation.
4. Provides automatic help information.

### **Q120. What is PEP 8? Explain the important Python coding standards and naming conventions.**

**Answer:**

PEP stands for Python Enhancement Proposal.

PEP 8 is the Python style guide that defines coding conventions and formatting standards.

It helps maintain readable and consistent Python code.

**Important PEP 8 Guidelines:**

1. Use meaningful variable names.
2. Use four spaces for indentation.
3. Use lowercase letters with underscores for function names.
4. Use meaningful names for classes.
5. Separate functions and classes using blank lines.
6. Use proper spacing around operators.
7. Avoid unnecessarily long lines.
8. Use comments where required.
9. Follow standard Python import order.
10. Maintain consistent formatting.

**Naming Conventions:**

| Element  | Convention                 | Example           |
| -------- | -------------------------- | ----------------- |
| Variable | lowercase with underscores | `user_name`       |
| Function | lowercase with underscores | `get_details()`   |
| Class    | PascalCase                 | `StorageDevice`   |
| Constant | Uppercase                  | `MAX_LIMIT`       |
| Module   | Short lowercase name       | `storage_test.py` |

**Example:**

```
class StorageDevice:    def __init__(self, drive_name):        self.drive_name = drive_name    def display_details(self):        print(self.drive_name)
```

### **Q121. What is Unit Testing in Python? What are PyTest and&#x20;**`unittest`**&#x20;frameworks, and why do we use them?**

**Answer:**

Unit Testing is the process of testing individual units or components of a program independently.

A unit can be a function, method or small piece of logic.

Python provides testing frameworks to execute and manage test cases.

**1. unittest:**

`unittest` is Python's built-in unit testing framework.

Example:

```
import unittestdef add(a, b):    return a + bclass TestAddition(unittest.TestCase):    def test_add(self):        self.assertEqual(add(10, 20), 30)if __name__ == "__main__":    unittest.main()
```

**2. PyTest:**

PyTest is an external Python testing framework.

It provides a simple way to write and execute test cases.

Example:

```
def add(a, b):    return a + bdef test_add():    assert add(10, 20) == 30
```

Execution:

```
pytest
```

**Difference:**

| unittest                                       | PyTest                                            |
| ---------------------------------------------- | ------------------------------------------------- |
| Built into Python                              | Installed separately                              |
| Commonly uses test classes and methods         | Can use simple test functions                     |
| Uses assertion methods such as `assertEqual()` | Uses normal `assert` statements                   |
| Provides test fixtures                         | Provides fixtures and additional testing features |

**Why do we use testing frameworks?**

1. To validate individual functions.
2. To identify defects early.
3. To execute tests repeatedly.
4. To perform regression testing.
5. To automate testing activities.

### **Q122. What is Version Control? Explain Git and Bitbucket and why they are useful in Python development and automation projects.**

**Answer:**

Version Control is a system used to track and manage changes made to source code over time.

It allows developers to maintain different versions of their code and collaborate with other team members.

**Git:**

Git is a distributed version-control system.

It tracks changes made to files and allows developers to create branches, commit changes and merge code.

**Common Git Commands:**

Initialize a repository:

```
git init
```

Check repository status:

```
git status
```

Add files:

```
git add .
```

Commit changes:

```
git commit -m "Initial commit"
```

Create a branch:

```
git branch feature
```

Switch branches:

```
git checkout feature
```

Push changes:

```
git push
```

Pull changes:

```
git pull
```

**Bitbucket:**

Bitbucket is a Git-based source-code hosting and collaboration platform.

It provides a remote repository where teams can store and manage their code.

**Why do we use Git and Bitbucket?**

1. To maintain code history.
2. To track changes.
3. To collaborate with team members.
4. To manage different branches.
5. To review code changes.
6. To maintain automation scripts.
7. To roll back to previous code versions when required.

**Example:**

Suppose we develop a Python storage automation framework.

We can maintain the framework in a Git repository and push it to Bitbucket so that other team members can access and contribute to the code.

# **Python – Final Completion Summary**

## **Important Python concepts for interview revision**

| Topic              | Key point                                         |
| ------------------ | ------------------------------------------------- |
| Python             | High-level, interpreted, general-purpose language |
| PVM                | Executes Python bytecode                          |
| Dynamic Typing     | Variable type determined at runtime               |
| Mutable            | Object contents can be changed                    |
| Immutable          | Object contents cannot be changed                 |
| List               | Ordered, mutable collection                       |
| Tuple              | Ordered, immutable collection                     |
| Set                | Collection of unique elements                     |
| Dictionary         | Key-value collection                              |
| String             | Immutable sequence of characters                  |
| Function           | Reusable block of code                            |
| `*args`            | Variable positional arguments                     |
| `**kwargs`         | Variable keyword arguments                        |
| Lambda             | Anonymous single-expression function              |
| map()              | Applies a function to iterable elements           |
| filter()           | Selects elements based on a condition             |
| reduce()           | Accumulates values into a single result           |
| File Handling      | Read, write, append and manage files              |
| Module             | Reusable Python file                              |
| OS Module          | Interacts with operating-system functionality     |
| Regex              | Pattern matching and extraction                   |
| Exception Handling | Handles runtime exceptions                        |
| Class              | Blueprint for objects                             |
| Object             | Instance of a class                               |
| Inheritance        | Reuses parent-class functionality                 |
| Encapsulation      | Organizes data and controls access                |
| Polymorphism       | Same interface, different behaviour               |
| Abstraction        | Hides implementation details                      |
| Decorator          | Adds functionality to an existing function        |
| Generator          | Produces values using `yield`                     |
| Iterator           | Provides values one at a time                     |
| Threading          | Runs multiple threads within a process            |
| Logging            | Records execution information                     |
| Paramiko           | Supports SSH communication through Python         |
| PyTest             | Python testing framework                          |
| PEP 8              | Python coding style guidelines                    |

## **Overall Mock Interview Preparation – Completion**
