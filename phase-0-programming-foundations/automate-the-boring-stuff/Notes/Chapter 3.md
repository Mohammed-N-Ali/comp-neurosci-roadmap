# <u>Loops</u>

2 different types of loops:
* while - Make a block of code execute over and over again while the statements condition is true
* for - Makes a block of code execute as many times as you want

You can use a while loop like a for loop with the use of a counter in the while loop - adding one to the variable being compared in the while expression to make it become False and break the loop in a set time 


## Statements in loops
---
break Statement - Immediately exit the loop, breaking it

continue Statements - Immediately jumps program execution back to the beginning

- If you need to terminate code/continous loop, use Ctrl + C

## Truthy and Falsey
---
Conditions will consider some values from other data types as equivalent to true or false

- 0, 0.0, '' : All of these values are considered to False
- Any other value other than these is seen as True

If you want to know if a value is truthy or falsey, use the bool() function

e.g   bool(0) = False

## Importing Modules
---
Each module is a Python program that contains a related group of functions that can be embedded in your program

Module examples:
- random = Random number related functions
- sys = Manipulates different parts of Python environment
- os = Functions that interact directly with OS : files, directories, systems, etc
- math = Mathematic related functions

sys.exit() = Used to terminate a program ( have to import sys first)
random.randint(a,b) = Returns a random integer value that is between a and b

