Python Strings:<br>
String is a built in class named 'str'<br>
Python strings are "immutable" so they cant be changed<br>
A double quoted string literal can contain single quotes <br>
Python uses zero-based indexing<br>
The "print" function normally prints out one or more python items followed by a newline<br>
A "raw" string literal is prefixed by an 'r'<br>
-
-
String Methods-<br>
s.lower(), s.upper() -- returns the lowercase or uppercase version of the string<br>
s.strip() -- returns a string with whitespace removed from the start and end<br>
s.isalpha()/s.isdigit()/s.isspace()... -- tests if all the string chars are in the various character classes<br>
s.startswith('other'), s.endswith('other') -- tests if the string starts or ends with the given other string<br>
s.find('other') -- searches for the given other string (not a regular expression) within s, and returns the first index where it begins or -1 if not found<br>
s.replace('old', 'new') -- returns a string where all occurrences of 'old' have been replaced by 'new'<br>
s.split('delim') -- returns a list of substrings separated by the given delimiter. The delimiter is not a regular expression, it's just text. 'aaa,bbb,ccc'.split(',') -> ['aaa', 'bbb', 'ccc']. As a convenient special case s.split() (with no arguments) splits on all whitespace chars.<br>
s.join(list) -- opposite of split(), joins the elements in the given list together using the string as the delimiter. e.g. '---'.join(['aaa', 'bbb', 'ccc']) -> aaa---bbb---ccc<br>

String Slices- The "slice" syntax is a way to refer to sub-parts of sequences <br>
s[1:4] is 'ell' -- chars starting at index 1 and extending up to but not including index 4
s[1:] is 'ello' -- omitting either index defaults to the start or end of the string
s[:] is 'Hello' -- omitting both always gives us a copy of the whole thing (this is the pythonic way to copy a sequence like a string or list)
s[1:100] is 'ello' -- an index that is too big is truncated down to the string length
s[-1] is 'o' -- last char (1st from the end)
s[-4] is 'e' -- 4th from the end
s[:-3] is 'He' -- going up to but not including the last 3 chars.
s[-3:] is 'llo' -- starting with the 3rd char from the end and extending to the end of the string.



Lists:Python has a great built-in list type named "list". List literals are written within square brackets[ ]<br>


List Build Up-One common pattern is to start a list a the empty list [], then use append() or extend() to add elements to it

List Slices-Slices work on lists just as with strings, and can also be used to change sub-parts of the list

Range-range(n) function yields the numbers 0, 1, ... n-1, and range(a, b) returns a, a+1, ... b-1 -- up to but not including the last number


While Loop-Python also has the standard while-loop<br>
while loop gives you total control over the index numbers<br>

Sorting:The easiest way to sort is with the sorted(list) function, which takes a list and returns a new list with those elements in sorted order. The original list is not changed.<br>
most common to pass a list into the sorted() function<br>
Custom Sorting With key- For more complex custom sorting, sorted() takes an optional "key=" specifying a "key" function that transforms each element before comparison <br>
You can also pass in your own MyFn as the key function<br>
complex sorting like sorting by last name then by first name, you can use the itemgetter or attrgetter functions<br>

sort() method: alternative to sorted(), the sort() method on a list sorts that list into ascending order, e.g. list.sort(). The sort() method changes the underlying list and returns None<br>
Tuples- fixed size grouping of elements, such as an (x, y) co-ordinate<br>



Dicts and Files:<br>
Dict Hash Table-key/value hash table structure. Can be written as a series of key:value pairs within braces { }, e.g. dict = {key1:value1, key2:value2, ... }. The "empty dict" is just an empty pair of curly braces {}<br>
-Tuples work as keys, and any type can be a value<br>
-Methods dict.keys() and dict.values() return lists of the keys or values explicitly
Dict Formatting- The % operator works conveniently to substitute values from a dict into a string by name<br>
Del- does deletions, it can remove the definition of a variable, as if that variable had not been defined. Can also be used on list elements or slices to delete that part of the list and to delete entries from a dictionary<br>


Files-open() function opens and returns a file handle that can be used to read or write a file in the usual way<br>
-code f = open('name', 'r') opens the file into the variable f<br>
-f.close() when finished<br>
-'a' for append
-A for loop allows you to look at all the lines in a text file<br>
Files Unicode-To read and write unicode encoded files use a `'t'` mode and explicitly specify an encoding<br>

Regular Expressions:<br>



Utilities: <br>
