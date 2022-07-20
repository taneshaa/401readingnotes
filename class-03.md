#### Reading and Writing Files in Python <br>
https://realpython.com/read-write-files-python/ <br>
#### Video for readning and writing files in python: <br>
https://realpython.com/courses/reading-and-writing-files-python/<br>
a file is a contiguous set of bytes used to store data. This data is organized in a specific format and can be anything as simple as a text file or as complicated as a program executable. In the end, these byte files are then translated into binary 1 and 0 for easier processing by the computer.<br>
File system contents made of three main parts:<br>
Header: metadata about the contents of the file (file name, size, type, and so on)<br>
Data: contents of the file as written by the creator or editor<br>
End of file (EOF): special character that indicates the end of the file<br>


File paths: When you access a file on an operating system, a file path is required. The file path is a string that represents the location of a file. It’s broken up into three major parts:

Folder Path: the file folder location on the file system where subsequent folders are separated by a forward slash / (Unix) or backslash \ (Windows)<br>
File Name: the actual name of the file<br>
Extension: the end of the file path pre-pended with a period (.) used to indicate the file type<br>

#### Python Exceptions: An Introduction<br>
https://realpython.com/python-exceptions/<br>

-Syntax errors occur when the parser detects an incorrect statement.The arrow indicates where the parser ran into the syntax error.<br>

-Exception error occurs whenever syntactically correct Python code results in an error.The last line of the message indicates what type of exception error you ran into.<br>

-Instead of showing the message exception error, Python details what type of exception error was encountered.<br>

-Instead of waiting for a program to crash midway, you can also start by making an assertion in Python. We assert that a certain condition is met
The 'try' and 'except' Block: Handling Exceptions  is used to catch and handle exceptions. Python executes code following the try statement as a “normal” part of the program. <br>

#### Takeaways + Summary:<br>
-A try clause is executed up until the point where the first exception is encountered.<br>
-Inside the except clause, or the exception handler, you determine how the program responds to the exception.<br>
-You can anticipate multiple exceptions and differentiate how the program should respond to them.<br>
-Avoid using bare except clauses.<br>
-'raise' allows you to throw an exception at any time.<br>
-'assert' enables you to verify if a certain condition is met and throw an exception if it isn’t.<br>
-In the 'try' clause, all statements are executed until an exception is encountered.<br>
-'except' is used to catch and handle the exception(s) that are encountered in the try clause.<br>
-'else' lets you code sections that should run only when no exceptions are encountered in the try clause.<br>
-'finally' enables you to execute sections of code that should always run, with or without any previously encountered exceptions.<br>
