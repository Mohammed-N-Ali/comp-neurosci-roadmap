# <u>Debugging</u>

try and except statements - Allows a program to recover from exceptions you anticipated and handle them

raise statement - Allows us to create our own error/exception

If no try and except statements cover the raise statement that raised the exception, the program crashes as displays the exception error message

## Assertions
---

Assertion - Checks to make sure your code isnt doing something obviously wrong

If the assertation fails, the code raises an AssertionError.

assert keyword, then condition to check

assert statements should not be resolved using try and except statements - the program should crash so you can find th original cause of the bug.

## Logging
---
logging module - Used to track and record events when an application runs

Log messages will descrive when the program execution has reached the logging function call and will lst any variables youve specified, providing a trail to check for errors. If a log message is missing, than you know a part of the code was skipped

The logging module’s basicConfig() function lets you specify what details you want to see and how you want those details displayed.

We use the logging.debug() function to print log information. This debug() function calls basicConfig(), which prints a line of information in the format we specified in the function call, along with the messages we passed to debug().

logging and logging.basicConfig(level=logging.DEBUG, format= '%(asctime)s - %(levelname)s - %(message)s')

You set the logging to open in a text file to avoid clutter: 
    logging.basicConfig(filename='myProgramLog.txt', level=logging.DEBUG,
    format=' %(asctime)s -  %(levelname)s -  %(message)s')

After you’ve debugged your program, you probably don’t want all these log messages cluttering the screen. The logging.disable() function disables these so that you don’t have to remove the logging calls by hand

# Logging Levels
---

* DEBUG

logging.debug()

The lowest level, used for small details. Usually, you’ll care about these messages only when diagnosing problems.

* INFO

logging.info()

Used to record information about general events in your program or to confirm that it’s working at various points.

* WARNING

logging.warning()

Used to indicate a potential problem that doesn’t prevent the program from working but might do so in the future.

* ERROR

logging.error()

Used to record an error that caused the program to fail to do something.

* CRITICAL

logging.critical()

The highest level, used to indicate a fatal error that has caused, or is about to cause, the program to stop running entirely.

# Breakpoint:
---
A breakpoint is an intentional pausing place put into a program for debugging purposes

* Pause button: Tells the computer to stop executing code at a specific line.
* Inspection tool: Allows you to view variable values while the program is frozen.
* Step-by-step control: Lets you run code one single line at a time to find bugs.