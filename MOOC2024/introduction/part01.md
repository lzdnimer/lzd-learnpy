# MOOC - Introduction to Python

## Contents

1. I/O, Variables, Conditional Statements
2. Conditions, Loops
3. Loops, Strings
4. User Defined Functions
5. Lists and other data structures
6. Files
7. External Libraries

## Use cases for Python

### As a replacement or complementary tool to Excel
* Excel can be used for most tasks including advanced analysis, but Python can help in replication of work. When working on Excel, it's not easy to document all the analysis steps being performed especially intermediary steps (e.g., filtering data). In most situations, Python code can be shared and used easily across teams.
* Excel also has limits in size and compute time. It may be easier and cheaper (in terms of compute) to solve a business issue using Python

## Lesson 1: Getting started

### Variables
Assigning a variable twice means that the first variable is forgotten:
```
x = 123
print(x) # 123
x = 234
print(x) # 234
```
Concatenation: there are different ways to [concatenate string](https://stackoverflow.com/questions/21542694/difference-between-using-commas-concatenation-and-string-formatters-in-python)
## f-strings
Probably the best way to format printouts, with flexibility in using variables and easy syntax
```
result = 10 * 25
print(f"The result is {results}
```

NB: 
* 'f' is within the brackets (i.e., the function is still *print*, not *printf*)
* Triple quotation marks are compatible:
```
x = 27
y = 15

print(f"""{x} + {y} = {x+y}
{x} - {y} = {x-y}
{x} * {y} = {x*y}
{x} / {y} = {x/y}""")
```

## Arithmetic
Most are already familiar functions. Some new ones:
```
// -> division (integer)
/ -> division (floating point)
% -> modulo
** -> exponentiation
```

input() produces a string data type result. To use the input in arithmetic, cast it as your desired data type:
```
x = int(input("Please type in a number:"))
print(f"{x} times 5 is {x*5}")
```

You can use operator assignment shorthands to simplify code:
```
x += 4; is the same as x = x + 4;
x -= 4; is the same as x = x - 4;
```

NB:
* Operators (+, -, /, * etc.) work on an operand (2, 3, 4.5)
* The data type of an operand usually determines the resulting datatype
## Conditional Statements
Conditional statements are similar to ones in SQL, with a key exception being that `==` is used for the equality operator rather than `=`

Conditionals used in a conditional statement will result in a truth value: True or False. These are boolean values.