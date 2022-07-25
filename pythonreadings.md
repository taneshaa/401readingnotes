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


Lists:<br>



Sorting:<br>



Dicts and Files:<br>



Regular Expressions:<br>



Utilities: <br>
