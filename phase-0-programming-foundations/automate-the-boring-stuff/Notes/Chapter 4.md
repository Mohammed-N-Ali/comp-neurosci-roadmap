# <u>Functions</u>

Functions = Mini programs within a program

def name() - Defines a function that when called, causes the code embedded in the block to execute

Major purpose of a function is to group code that gets executed together and avoid duplicating it

## Arguments and Parameters
---
- Arguments = a value or object that you pass into a function or method when you call it
- Parameter = a variable name listed inside the parentheses of a function definition, acting as a placeholder for the argument

## None value and named parameters
---
None value = Abscence of a value and is the only value of the NoneType data type represented by letter N

The print() function uses the optional parameters end and sep to specify separator characters to print at the end of its arguments and between its arguments, respectively:

* sep = Determines the character or string used to seperate multiple string values
* end = Determines what character or string is printed at the very end of your output

## Call stack
---
Call stack is how Python remembers where to return the execution after each function call ( the orginal function call)

Call stack isnt stored in a variable, rather, its a section of computer memory that python handles automatically. Python creates a frame object on top of the call stack. If function makes another function call, Python adds another frame object above the other one in a call stack. When function returns, frame object is removed and moves onto next one.

Frame object = Store the line number of the orginal function call so Python can remember where to return execution to.

Top of frame stack = Currently executing function

## Local and Global Scopes
---
* Local variable -  A variable created inside a function that can only be used in that function
* Global variable - A variable created outside a function that can be used anywehere in the code

Scope = Container for variables

## Scope rules
---
* Code that is in the global scope, outside all functions, can’t use local variables.
* Code that is in one function’s local scope can’t use variables in any other local scope.
* Code in a local scope can access global variables.
* You can use the same name for different variables if they are in different scopes. That is, there can be a local variable named spam and a global variable also named spam.

If you need to modify global variable within a function, use global statement.

## Errors
---
* ZeroDivisionError: occurs when you try dividing a number by zero
* FileNotFoundError: occurs if you specify a filename for a file that doesnt exist

Errors can be handled with try and except clauses
- try: The try block lets you test a block of code for errors
- except: The except block lets you handle the error