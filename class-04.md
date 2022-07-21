#### Classes and Objects:<br>
Objects are an encapsulation of variables and functions into a single entity. Objects get their variables and functions from classes. Classes are essentially a template to create your objects.<br>
Class example: <br>
class MyClass:<br>
    variable = "blah"<br>

    def function(self):<br>
        print("This is a message inside the class.")<br>

So for instance the below would output the string "blah":<br>
class MyClass:<br>
    variable = "blah"<br>

    def function(self):<br>
        print("This is a message inside the class.")<br>

myobjectx = MyClass()<br>

print(myobjectx.variable)<br>
<br>
<br>

#### Thinking Recursively in Python:<br>
A recursive function is a function defined in terms of itself via self-referential expressions.<br>
the function will continue to call itself and repeat its behavior until some condition is met to return a result. All recursive functions share a common structure made up of two parts: base case and recursive case.<br>

*maintaining state*<br>
When dealing with recursive functions, keep in mind that each recursive call has its own execution context, so to maintain state during recursion you have to either:<br>
Thread the state through each recursive call so that the current state is part of the current call’s execution context<br>
Keep the state in global scope<br>

*Recursive Data Structures in Python*<br>
A data structure is recursive if it can be deﬁned in terms of a smaller version of itself. A list is an example of a recursive data structure.<br>

#### Bookark & Review:<br>
https://docs.pytest.org/en/latest/explanation/fixtures.html<br>
