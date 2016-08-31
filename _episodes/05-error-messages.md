---
title: "Error Messages"
teaching: 5
exercises: 10
questions:
- "What kind of errors can occur in programs?"
- "How can I identify errors when they occur?"
objectives:
- "Read a traceback and determine the file, function, and line number on which the error occurred, the type of error, and the error message."
- "Correctly describe situations in which SyntaxError, IndentationError, NameError, IndexError, and FileNotFoundError occur."
keypoints:
- "Use comments to add documentation to programs."
- "Python reports a syntax error when it can't understand the source of a program."
- "Indentation is meaningful in Python."
- "Python reports a runtime error when something goes wrong while a program is executing."
- "Fix syntax errors by reading the source code, and runtime errors by tracing the program's execution."
---
## Use comments to add documentation to programs.

It is good practise to explain what our code is doing so that future users of our code can better understand how our code works. Some things to document include: 

* Who wrote the code.
* What the code does.
* What information the variables store.

In the notebook, we can use markup to document our code. However, python has a way of documenting our code as well called commenting. There are two ways to comment in python. 

* single line comment. This is indicated by the `#` operator. In python anything after the `#` symbol is ignored for the rest of the line. 
* multi line comment. This is indicated by `/*` to start the comment and `/*` to end it. 
~~~
# This sentence isn't executed by Python.
adjustment = 0.5   # Neither is this - anything after '#' is ignored.
/* This code is also not executed even though it spans multiple lines. That's because it's a multi-line comment. All code is ignored up to here because the closing symbol follows.  */
~~~
{: .python}

## Python reports a syntax error when it can't understand the source of a program.

*   Won't even try to run the program if it can't be parsed.

~~~
# Forgot to close the quotation marks around the string.
name = 'Feng
~~~
{: .python}
~~~
SyntaxError: EOL while scanning string literal
~~~
{: .error}

~~~
# An extra '=' in the assignment.
age = = 52
~~~
{: .python}
~~~
SyntaxError: invalid syntax
~~~
{: .error}

*   Look more closely at the error message:

~~~
print("hello world"
~~~
{: .python}
~~~
  File "<ipython-input-6-d1cc229bf815>", line 1
    print ("hello world"
                        ^
SyntaxError: unexpected EOF while parsing
~~~
{: .error}

*   The message indicates a problem on first line of the input ("line 1").
    *   In this case the "ipython-input" section of the file name tells us that
        we are working with input into IPython,
        the Python interpreter used by the Jupyter Notebook.
*   The `-6-` part of the filename indicates that
    the error occurred in cell 6 of our Notebook.
*   Next is the problematic line of code,
    indicating the problem with a `^` pointer.

## Indentation is meaningful in Python.

*   Python uses indentation to group sections of code together
    (which we will discuss [later]({{ site.github.url }}/09-for-loops)).
*   If the indentation changes in a way that Python does not expect,
    it reports an `IndentationError`
    (which is a more specific kind of syntax error).

~~~
firstName="Jon"
  lastName="Smith"
~~~
{: .python}
~~~
  File "<ipython-input-7-f65f2962bf9c>", line 2
    lastName="Smith"
    ^
IndentationError: unexpected indent
~~~
{: .error}

*   This error can be fixed by removing the extra spaces
    at the beginning of the second line.

## Python reports a runtime error when something goes wrong while a program is executing.

~~~
age = 53
remaining = 100 - aege # mis-spelled 'age'
~~~
{: .python}
~~~
NameError: name 'aege' is not defined
~~~
{: .error}

## Fix syntax errors by reading the source and runtime errors by tracing execution.

FIXME: diagram of where each type of error occurs.

FIXME: this entire episode needs to move later (we can't do IndentationError yet, or 
talk about the tracebacks until we've written functions).

> ## Reading Error Messages
>
> Read the traceback below, and identify the following:
>
> 1. How many levels does the traceback have?
> 2. What is the file name where the error occurred?
> 3. What is the function name where the error occurred?
> 4. On which line number in this function did the error occurr?
> 5. What is the type of error?
> 6. What is the error message?
>
> ~~~
> ---------------------------------------------------------------------------
> KeyError                                  Traceback (most recent call last)
> <ipython-input-2-e4c4cbafeeb5> in <module>()
>       1 import errors_02
> ----> 2 errors_02.print_friday_message()
>
> /Users/ghopper/thesis/code/errors_02.py in print_friday_message()
>      13
>      14 def print_friday_message():
> ---> 15     print_message("Friday")
>
> /Users/ghopper/thesis/code/errors_02.py in print_message(day)
>       9         "sunday": "Aw, the weekend is almost over."
>      10     }
> ---> 11     print(messages[day])
>      12
>      13
>
> KeyError: 'Friday'
> ~~~
> {: .error}
{: .challenge}

> ## Identifying Syntax Errors
>
> 1. Read the code below and try to identify what the errors are
>    *without* running it.
> 2. Run the code and read the error message.
>    Is it a `SyntaxError` or an `IndentationError`?
> 3. Fix the error.
> 4. Repeat steps 2 and 3 until you have fixed all the errors.
>
> ~~~
> def another_function
>   print("Syntax errors are annoying.")
>    print("But at least python tells us about them!")
>   print("So they are usually not too hard to fix.")
> ~~~
> {: .source}
{: .challenge}

> ## Identifying Variable Name Errors
>
> 1. Read the code below and try to identify what the errors are
>    *without* running it.
> 2. Run the code and read the error message.
>    What type of `NameError` do you think this is?
>    Is it a string with no quotes, a misspelled variable, or a 
>    variable that should have been defined but was not?
> 3. Fix the error.
> 4. Repeat steps 2 and 3, until you have fixed all the errors.
>
> ~~~
> for number in range(10):
>     # use a if the number is a multiple of 3, otherwise use b
>     if (Number % 3) == 0:
>         message = message + a
>     else:
>         message = message + "b"
> print(message)
> ~~~
> {: .source}
{: .challenge}

> ## Identifying Item Errors
>
> 1. Read the code below and try to identify what the errors are
>    *without* running it.
> 2. Run the code, and read the error message. What type of error is it?
> 3. Fix the error.
>
> ~~~
> seasons = ['Spring', 'Summer', 'Fall', 'Winter']
> print('My favorite season is ', seasons[4])
> ~~~
> {: .source}
{: .challenge}
