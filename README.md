# Python-week2 & 3

WEEK 2 Python

Control Flow.

Day 1

Control flow statements.

Control flow statements in Python are used to determine the order in which a program's instructions are executed. They allow you to make decisions, create loops, and control the flow of your program.

· Programs control flow is the order in which the programs code executes.

· The control flow of a python program is regulated by conditional statements, loops and functions.

Python has 3 types of control structure.

· Sequential-default mode

· Selection- used for decisions and branching.

· Repetition- used for looping example repeating a piece of code multiple times.

Python provides several control flow statements, including:

1. Conditional Statements (if, elif, else):

- `if` statement: Allows you to execute a block of code if a specified condition is true.

- `elif` (short for "else if") statement: Used to check additional conditions if the initial `if` condition is false.

- `else` statement: Provides a block of code to execute when the `if` and `elif` conditions are false.

Example:

```python

x = 10

if x > 5:

print("x is greater than 5")

elif x == 5:

print("x is equal to 5")

else:

print("x is less than 5")

```

2. Loops (for and while):

- `for` loop: Iterates over a sequence (e.g., a list, tuple, string) or a range of values and executes a block of code for each element in the sequence.

- `while` loop: Repeats a block of code if a specified condition is true.

Example (for loop):

```python

fruits = ["apple", "banana", "cherry"]

for fruit in fruits:

print(fruit)

```

Example (while loop):

```python

count = 0

while count < 5:

print(f"Count is {count}")

count += 1

```

3. Control Statements (break and continue):

- `break` statement: Terminates the current loop prematurely and continues with the next code outside the loop.

- `continue` statement: Skips the current iteration of a loop and moves on to the next iteration.

Example (break):

```python

for num in range(1, 10):

if num == 5:

break

print(num)

```

Example (continue):

```python

for num in range(1, 6):

if num == 3:

continue

print(num)

```

These control flow statements are fundamental for building complex programs and making decisions based on conditions or iterating through data structures. They provide the necessary flexibility to create dynamic and responsive Python programs.

Day 2

Intro to functions

In Python, a function is a reusable block of code that performs a specific task or a set of tasks. Functions are a fundamental concept in programming, as they allow you to encapsulate functionality, make your code more modular, and promote code reusability. Functions in Python are defined using the `def` keyword, followed by the function name and a set of parentheses. Here's an introduction to functions in Python:

1. Function Definition:

· To define a function, you use the `def` keyword, followed by the function name, a set of parentheses, and a colon.

· The function's code block is indented beneath the definition. You can also include parameters in the parentheses if your function requires input values.

Example of a simple function without parameters:

```python

def greet():

print("Hello, world!")

```

2. Function Invocation:

To execute a function, you simply call it by its name followed by parentheses. If the function has parameters, you provide the required values within the parentheses.

Example of calling the `greet` function:

```python

greet()

```

3. **Return Statement**:

Functions can return values using the `return` statement. This allows a function to produce a result that can be used in other parts of your code.

Example of a function with a return statement:

```python

def add(a, b):

result = a + b

return result

```

You can store the returned value in a variable or use it directly:

```python

sum_result = add(3, 4)

print(sum_result) # Outputs: 7

4. **Function Parameters**:

Functions can take parameters (input values) to perform operations based on the provided values. You define these parameters within the function's parentheses.

Example of a function with parameters:

```python

def multiply(x, y):

result = x * y

return result

```

Call the function with arguments:

```python

product = multiply(5, 2)

print(product) # Outputs: 10

5. Docstrings:

It's good practice to include a docstring (a multi-line string enclosed in triple-quotes) at the beginning of your function to provide a description of what the

function does. This helps document your code and makes it easier for others (and yourself) to understand the function's purpose.

Example with a docstring:

```python

def subtract(a, b):

"""

This function subtracts 'b' from 'a' and returns the result.

"""

result = a - b

return result

```

Functions are a powerful way to structure your code, making it more organized, readable, and maintainable. They allow you to break your program into smaller, manageable pieces that perform specific tasks, which can be called as needed. This modularity is a key aspect of writing clean and efficient Python code.

Using Functions

· We create functions by providing three pieces of information. The name of the function, a list of zero or more parameters, and, optionally, a block of code which provides the return value (a function can return nothing).

· We normally define functions in script files for the simple reason that we do not want to type them more than once, we just want to edit a function (if necessary).

We must make a firm distinction between an argument value and a parameter:

· Argument

The argument is the object used in an application of a function; it may be referenced by other variables or objects.

· Parameter

The parameter is a variable name that is part of the function and is a local variable within the function body

We define a function by using the following syntax:

def function_name(parameter <,...>):

#suite

There are three types of functions in Python.

· Ordinary function

· Procedure function

· Factory functions.

· Ordinary functions are functions that follow mathematical procedures. They will receive an argument, perform a specific calculation with the argument, and return a result.

· Procedure functions normally do not return a result; they are called to execute a procedure. For example, a function can, be created to set up a connection to a database.

· Factory functions do not take parameters. The function generates values. Some factory functions work by accessing an object encapsulated in a module. For example, you will access the random number generator encapsulated in the random module.

The following is an example of how programs use functions to be more efficient:

def calculateTax(salary):

"""Calculates and prints a given salary’s tax"""

if salary > 30000 :

rate = 0.2

elif salary > 10000 :

rate = 0.15

else:

rate = 0.1

tax = salary * rate

print (tax)

print ("Enter the amount on which you want to calculate tax:")

calculateTax(int(input()));

The provided code defines a Python function called `calculateTax(salary)` and then demonstrates how to use this function to calculate and print the tax on a given salary. Here's a step-by-step explanation of the code:

1. `def calculateTax(salary):`:

- This line defines a function called `calculateTax` that takes one parameter, `salary`. The parameter is enclosed in parentheses.

- The docstring `"""Calculates and prints a given salary’s tax"""` is a comment or description of what the function does. It is good practice to include docstrings to explain the purpose of your function.

2. Inside the function, there is an if-elif-else statement:

- `if salary > 30000:` checks if the `salary` is greater than 30,000.

- If the condition is true, it sets the `rate` variable to 0.2, indicating a tax rate of 20%.

- `elif salary > 10000:` checks if the salary is greater than 10,000 but not greater than 30,000.

- If the condition is true, it sets the `rate` variable to 0.15, indicating a tax rate of 15%.

- If neither of the above conditions is true (i.e., the salary is less than or equal to 10,000), it sets the `rate` variable to 0.1, indicating a tax rate of 10%.

3. `tax = salary * rate` calculates the tax amount by multiplying the `salary` by the determined `rate`.

4. `print(tax)` prints the calculated tax amount to the console.

5. Outside of the function, there is a `print("Enter the amount on which you want to calculate tax:")` statement, which displays a message to the user, prompting them to enter a salary amount.

6. `calculateTax(int(input()))`:

- `input()` reads a line of text from the user (the salary amount), and `int()` converts that input to an integer. This is necessary because `input()` returns a string, and you need to perform numerical calculations on the input.

- `calculateTax(...)` calls the `calculateTax` function, passing the entered salary as an argument.

Overall, the code defines a function to calculate and print the tax based on the given salary. It determines the tax rate based on the salary amount and then calculates the tax amount using that rate. The user is prompted to enter a salary, and the function is called with the entered salary to calculate and print the tax.

The random module

· The basic random function generates a random floating point as output.

· Python uses the Mersenne twister as the core generator.

· The Mersenne Twister is an algorithm for generating random numbers. It has a very long period before its sequence of numbers will repeat (219937 – 1). It is also a very fast.

· The functions supplied by the random module are actually bound methods of a hidden instance of the random.

The following example is an example of a function with the use of the random module:

Example 3 – Random module:

import random

def lotto_number():

"""The result from a lotto number draw is returned."""

num = random.randrange(1,47)

return str(num)

for n in range(1,6):

print (lotto_number())

Recursive functions

· It’s a function that keeps calling itself until it reaches its goal.

· In the Fibonacci sequence of numbers, each number is the sum of the previous two numbers, starting with 0 and 1. This sequence begins 0, 1, 1, 2, 3, 5, 8, 13, 21, 34…

Fibonacci recursive function:

def Fibonacci(num):

if num <= 1: # base case

return 1

else:

return num * Fibonacci(num - 1) # recursive call

for i in range(11):

print ("%2d = %d" % (i, Fibonacci(i)))

Output: 0 = 1

1 = 1

2 = 2

3 = 6

4 = 24

5 = 120
6 = 720

7 = 5040

8 = 40320

9 = 362880

10 = 3628800

A recursive function in Python is a function that calls itself, either directly or indirectly, to solve a problem by breaking it down into smaller, more manageable subproblems. It follows a concept called recursion, which is a fundamental technique in computer science and mathematics. Here's a summary of key points about recursive functions in Python:

1. Base Case: A recursive function must have one or more base cases. These are specific conditions that stop the recursion and provide a result without further recursive calls. Base cases prevent the function from running indefinitely.

2. Recursive Case: In addition to the base case, a recursive function includes one or more recursive cases. In a recursive case, the function calls itself with modified arguments, typically making the problem smaller in some way.

3. Example: A classic example of a recursive function is the factorial function, which calculates the factorial of a non-negative integer. The base case for the factorial function is when the input is 0, and the recursive case is to multiply the input by the factorial of (input - 1).

```python

def factorial(n):

if n == 0:

return 1 # Base case

else:

return n * factorial(n - 1) # Recursive case

```

4. Recursion Depth: Recursive functions can lead to a call stack, and if the recursion depth becomes too deep, it may result in a "RecursionError." Python has a default recursion depth limit,

which can be modified, but it's important to use recursion judiciously and ensure that it doesn't lead to excessive function calls.

5. Advantages and Disadvantages: Recursive functions can provide elegant and concise solutions to certain problems, making the code easier to understand and maintain. However, they may have performance overhead due to function call overhead and may be less efficient for very large inputs compared to iterative solutions.

6. Tail Recursion: Some programming languages offer tail call optimization, which optimizes recursive functions to avoid the accumulation of call stack frames. Python doesn't provide native tail call optimization, so large recursive functions can lead to a "RecursionError."

7. Indirect Recursion: In some cases, multiple functions call each other in a circular manner, which is called indirect recursion. Care must be taken to define base cases correctly in such scenarios to prevent infinite loops.

Recursive functions are a powerful tool in Python and can be used to solve a wide range of problems, particularly those that exhibit a recursive structure. However, it's important to use them wisely, considering the base cases, termination conditions, and potential performance implications.

Day 3

Modules

· A file containing python code, typically functions, classes and variables that can be imported and used in other python script.

· Modules in Python are a fundamental concept that allows you to organize and reuse code.

· Modules help break down a program into smaller, manageable parts, promoting code reusability and organization.

· Definition: A module in Python is a file containing Python code, typically functions, classes, and variables, that can be imported and used in other Python scripts. Modules help break down a program into smaller, manageable parts, promoting code reusability and organization.

· Usage: You can use modules to structure your code logically and make it more maintainable. Python's standard library is a collection of modules that provide a wide range of functionality, from file manipulation to web development, mathematics, and more.

· Creating Modules: To create your own module, you can write a Python script and save it with a .py file extension. This file can contain functions, classes, and variables that you want to reuse in other parts of your program.

· Importing Modules: To use a module in your Python script, you import it using the import statement.

For example:

import mymodule # Import a module named "mymodule"

· Accessing Module Members: Once a module is imported, you can access its functions, classes, and variables using dot notation.

For example,

if mymodule has a function named my_function, you can call it like this:

mymodule.my_function()

· Aliasing: You can alias a module or its members to give them shorter or more convenient names when using them in your code.

For example:

import mymodule as mm # Alias the module from mymodule import my_function as mf # Alias a specific function

· Standard Library: Python comes with a vast standard library that includes modules for tasks like file I/O, math, networking, regular expressions, and more. These modules are readily available for use in your programs without the need for additional installation.

· Third-Party Modules: Python's ecosystem benefits from a rich collection of third-party modules and packages that extend its capabilities. You can install and use these modules using package managers like pip.

· Module Search Path: Python searches for modules in directories defined by the sys.path variable. By default, it includes the current directory and the standard library paths. You can add custom paths to this list to find your own modules.

· __name__ and Module Execution: Python modules have a built-in __name__ attribute. When a module is executed, its __name__ is set to '__main__'. This allows you to include code that should only run when the module is the main program.

· Packages: Packages are a way to organize related modules into directories and subdirectories. They include a special __init__.py file that marks a directory as a package. Packages help manage large codebases by providing a hierarchical structure.

· Modules are a fundamental part of Python's modular and extensible design, making it easier to develop and maintain Python applications and libraries. They promote code reuse, encapsulation, and separation of concerns, making your code more organized and maintainable.

Mechanism of Python Modules

· There's a thing called program directory where the python modules are located its called PYTHONPATH.

Listing of Modules

· The list of available modules in Python can be found out by executing the following command in the command prompt (interpreter shell).

When you want to see the lsit of available modules on python you execute

Help(“module”) on the console.

The mechanism of Python modules involves several steps that Python follows to locate, import, and use modules in your code. Here's a summary of the key aspects of how Python's module system works:

1. Module Structure: A module in Python is a file containing Python code, typically with the `.py` extension. Modules can include functions, classes, variables, and even executable code.

2. Module Search Path: Python uses a list of directories to search for modules. This list is defined in the `sys.path` variable and includes the following directories in this order:

- The directory containing the script that was executed (if applicable).

- Directories in the `PYTHONPATH` environment variable (if set).

- Standard library directories.

- Site-specific directories.

- User-specific directories.

3. Importing Modules: To use a module in your Python script, you import it using the `import` statement. For example:

```python

import mymodule # Import a module named "mymodule"

```

4. Dot Notation: Once imported, you can access the functions, classes, and variables from the module using dot notation. For instance:

```python

mymodule.my_function()

```

5. Module Caching: Python caches imported modules to improve performance. When a module is imported, it's executed only once, and subsequent imports reuse the cached module.

6. Module Initialization: When you import a module, Python executes the code in the module from top to bottom. However, it only does this once per module, even if the module is imported multiple times.

7. `__name__` Attribute: Modules have a built-in attribute called `__name__`. When a module is executed as the main program, its `__name__` is set to `'__main__'`. You can use this to include code that should only run when the module is executed directly.

8. Packages: Packages are a way to organize related modules into directories. A package directory includes a special `__init__.py` file, which marks it as a package. Packages help manage large codebases by providing a hierarchical structure.

9. Relative Imports: Modules can be organized into packages, and you can use relative imports to refer to modules within the same package. Relative imports use dot notation to specify the module's location within the package.

```python

from . import submodule # Relative import within a package

```

10. Standard Library and Third-Party Modules: Python's standard library provides a vast collection of modules for various tasks. In addition to the standard library, you can also install and use third-party modules and packages to extend Python's functionality.

Python's module mechanism is a fundamental feature of the language that promotes code organization, reusability, and maintainability. It allows you to create modular and well-structured code by separating functionality into distinct units that can be easily imported and used in your programs.

Importing modules

The syntax of importing modules for python standard path is below,

Import module_name

· To fetch and use modules from other and new sources, we need to install Python PIP.

· Python pip is a software that installs python modules from an index or using a manager like Anaconda.

· Run the following command to install modules from new sources using python pip:

· python -m pip3 install module_name

· Run the following command to install modules from new sources using Ananconda:

· conda install module_name

· Example: Steps to install NumPy

· python -m pip3 install numpy conda install numpy sudo apt install python3-numpy

To import modules from an external source in Python, you typically use a package manager like `pip`, which allows you to download and install packages (collections of modules) from external sources such as the Python Package Index (PyPI). Here are the steps to import modules from an external source:

1. **Install the Package Manager**:

If you don't have `pip` installed, you can install it by following the instructions provided on the official Python website or the package manager's documentation.

2. **Search for the Desired Package**:

Use the package manager to search for the module or package you want to import. For example, to search for a package named "requests," you can run:

```bash

pip search requests

```

3. **Install the Package**:

Once you've identified the package you want to use, you can install it using `pip`. For example, to install the "requests" package:

```bash

pip install requests

```

This command will download and install the "requests" package and its associated modules.

4. **Import the Module in Your Python Code**:

After installation, you can import the module(s) in your Python code as usual. For example:

```python

import requests

```

5. **Use the Imported Module**:

You can then use the imported module and its functions, classes, and variables in your Python code. For example:

```python

response = requests.get('https://www.example.com')

```

By following these steps, you can import modules from external sources in Python. The process is the same for most external packages, but you may need to consult the specific package's documentation or PyPI page for any additional installation or usage instructions. Keep in mind that using a virtual environment for your project is recommended to manage package dependencies and avoid conflicts between different projects.

[11:27 PM] Sisanda Manjanja
Day4


Regular expressions, often referred to as “regexes,” are a concise way of specifying patterns in text. They are a powerful tool in Python, thanks to the `re` module, and serve several key purposes:


1. Parsing: Regular expressions are used to identify and extract specific pieces of text that match certain criteria within a larger text or data.


2. Searching: They help locate substrings that may have multiple forms, such as finding various image file extensions like ‘pet.png,’ ‘pet.gif,’ and ‘pet.mpg’ while excluding ‘carpet.gif.’



3. Searching and Replacing: You can find substrings and replace specific words within the matched string or strings, such as replacing a local phone number format like ‘071 234 5678’ with an international format like ‘+2771 234 5678.’


4. Splitting Strings: Regular expressions are handy for splitting a string at specific delimiters. For example, you can split a comma-separated list into individual items by using a regex that matches ‘,’.



5. Validation: They are used to check whether a string adheres to certain criteria, like validating whether an email address is in the standard format.

However, regular expressions do have limitations:

- They are suitable for handling recursive (repeating) structured text only if the maximum number of repetitions is known in advance.

- Large and complex regex patterns can become challenging to maintain and understand.



As a best practice, when dealing with highly structured data formats like XML, it’s often better to use specialized parsers tailored to that format. In simpler terms, a basic regular expression consists of a character followed by a quantifier, while more complex expressions can involve combinations of quantified expressions to match intricate patterns in text data.

Regular expression syntax

This section provides an overview of regular expressions (regex) and their syntax. It covers key functions from the Python re module and presents a table of commonly used functions and their descriptions.


1. **Introduction to Regular Expressions: **

- Regular expressions are a powerful tool for text pattern matching.

- The section is divided into four subsections:


- Matching individual characters or character groups.

- Quantifying matches (e.g., matching zero or more occurrences).


- Creating and grouping sub-expressions.

- Using language assertions and flags.



2. **Table of re Module Functions (commonly used):**

- `compile`: Compiles a regex pattern.

- `findall`: Returns a list of all non-overlapping matches in a string.


- `finditer`: Returns an iterator over all matches.

- `match`: Tries to apply the pattern at the start of the string.


- `search`: Scans through a string looking for a match.

- `split`: Splits a string by pattern occurrences.


- `sub`: Replaces occurrences of the pattern in the string.

- `subn`: Returns a 2-tuple with the new string and the number of replacements.


- `template`: Compiles a template pattern.


3. **Regular Expression Syntax:**

- This part explains various regex syntax elements:

- `.` (Dot): Matches any character (except newline).


- `^`: Matches the start of the string.

- `$`: Matches the end of the string.


- `*`: Matches zero or more occurrences.

- `+`: Matches one or more occurrences.


- `?`: Matches zero or one occurrence.

- `{m}`: Matches exactly m occurrences.


- `{m,n}`: Matches from m to n occurrences.

- `{m,n}?`: Matches as few occurrences as possible.


- `\`: Escapes special characters or signals a special sequence.

- `[]`: Indicates a set of characters.


- `|`: Represents alternation (matches X or Y).


4. **Raw Strings in Python:**

- Explains the importance of using raw strings in regex.

- In raw strings, backslashes are treated as literal characters, making regex patterns cleaner.



6. **Example – Validating Input Format:**

- Demonstrates the use of regex to validate input.

- Shows two equivalent regex patterns: one using a raw string and one without.


- Validates input in the format of three numbers enclosed in brackets.


The provided code example shows how to validate input in a specific format (three numbers enclosed in brackets) using regular expressions and demonstrates the use of raw strings for cleaner pattern definition.


Overall, this section provides a comprehensive introduction to regular expressions and their syntax, with a focus on Python’s re module and the importance of using raw strings to simplify regex pattern creation.


Character and character classes:

In this section on regular expressions and escape characters, the following key points are discussed:


1. Basic Regex Expressions:

- A single character, like ‘5’ or ‘b’, matches one occurrence by default.

- Special characters in regex, like ‘+’, ‘*’, and ‘?’, need a backslash (\) as a prefix if they are to be treated as literals.



2. Escape Characters in Python and Regex:

- Escape characters in Python include ‘\’, ‘\n’, ‘\t’, and more. They are used to represent special characters or control characters.

- To use special regex characters as literals, they must be preceded by a backslash (\).



3. Example – Matching Special Characters:

- A Python example is given where regular expressions are used to match the presence of a ‘+’ character and a newline character (‘\n’) in a sentence.

- The ‘^’ symbol matches the start of the text, ‘.*’ matches zero or more characters (including newlines), ‘[\+]+’ matches one or more ‘+’ characters, and ‘$’ matches the end of the line.



4. Character Classes and Ranges:

- Character classes, like [ea], match either ‘e’ or ‘a’.

- Ranges, like [0-9], match any digit from 0 to 9.


- Negating a character class, like [^0-9], matches any character except digits.


5. Handling Special Characters within Character Classes:

- Dashes (-) and some other characters are metacharacters by default. However, if they are the first character within a character class (e.g., [-abc]), they are treated as literals and do not require a backslash.

- Other metacharacters, like ‘.’, ‘^’, ‘?’, ‘+’, ‘*’, are always treated as literals within character classes.



7. Shortcuts in Character Classes:

- Python offers shortcuts for character classes, such as ‘\d’ (matches any digit) and ‘\s’ (matches whitespace).

- The ASCII flag can modify the behavior of these shortcuts.



8. Example – Using Shortcuts in Character Classes:

- A Python example illustrates how to count the number of words in a sentence using shortcuts like ‘\w’ and ‘\W’.

- The regular expression ‘^[\W]*[\w]*[\W]*’ is used to identify words in a sentence.



In summary, this section covers the basics of regular expressions, escape characters, character classes, and shortcuts within character classes. It provides practical examples to demonstrate the use of these concepts in Python.


Quantifies and flags:

Quantifies:

This section explains quantifiers in regular expressions and provides shorthand notations for simplifying the use of quantifiers. The key points covered are as follows:


1. Quantifiers in Regex:

- A quantifier in regex has the form {m, n}, specifying the minimum and maximum number of times an expression must match.

- For example, e{1,1}e{1,1} and e{2,2} both match “feelings” but not “belt.”



2. Shorthand Notations for Quantifiers:

- Regex provides shorthand notations to simplify quantifiers.

- If only one number is supplied, it’s assumed that the minimum and maximum are the same. For example, e{4} is equivalent to e{4, 4}.


- Different minimum and maximum values can be convenient. For instance, to match both “travelled” and “traveled,” you can use “travel{1,2}ed” or “travell{0,1}ed.”

- The ‘?’ symbol is used to represent {0,1}, meaning the preceding character is optional.



3. Examples of Using Quantifiers:

- An example in Python demonstrates the use of quantifiers to match words like “travelled” and “traveled” with the pattern ‘travell?ed’ (where ‘?’ is a shorthand for {0,1}).

- This allows for flexibility in matching words with different numbers of ‘l’ characters.



In summary, this section clarifies the concept of quantifiers in regular expressions and shows how shorthand notations like ‘?’ can be used to make regex patterns more concise and flexible. It provides a practical example in Python to illustrate the application of these quantifiers.


Flags:

Flags are used to tell the regex how to behave when looking for expressions.

This section introduces various regex flags and their functions in Python. The key points covered include:


1. Regex Flags:

- Python offers several flags to modify the behavior of regex patterns.

- Flags, like re.IGNORECASE or re.VERBOSE, can be used to make regex matching more flexible and readable.



2. Examples of Flags:

- An example demonstrates the use of the IGNORECASE flag (re.IGNORECASE or re.I) for case-insensitive matching. It removes all vowels (both uppercase and lowercase) from a string.

- Another example uses the VERBOSE flag (re.VERBOSE or re.X) to make a complex regex pattern more readable. It checks whether a string is a valid octal or hexadecimal number.



3. IGNORECASE Flag:

- The IGNORECASE flag is used to make regex matching case-insensitive, reducing the need to specify both uppercase and lowercase characters explicitly.


4. VERBOSE Flag:

- The VERBOSE flag allows comments and white spaces to be included in a regex pattern, making complex expressions more readable.

- It can be especially useful for explaining longer and more intricate regular expressions.



In summary, this section covers the use of regex flags, specifically the IGNORECASE (case-insensitive) and VERBOSE (readable) flags, and provides practical examples to illustrate their application in Python.
