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

Regular Expressions:used for matching text patterns<br>
Basic Patterns-
-a, X, 9, < -- ordinary characters just match themselves exactly. The meta-characters which do not match themselves because they have special meanings are: . ^ $ * + ? { [ ] \ | ( ) (details below)<br>
-. (a period) -- matches any single character except newline '\n'<br>
-\w -- (lowercase w) matches a "word" character: a letter or digit or underbar [a-zA-Z0-9_]. Note that although "word" is the mnemonic for this, it only matches a single word char, not a whole word. \W (upper case W) matches any non-word character.<br>
-\b -- boundary between word and non-word<br>
-\s -- (lowercase s) matches a single whitespace character -- space, newline, return, tab, form [ \n\r\t\f]. \S (upper case S) matches any non-whitespace character.
-\t, \n, \r -- tab, newline, return<br>
-\d -- decimal digit [0-9] (some older regex utilities do not support \d, but they all support \w and \s)<br>
-^ = start, $ = end -- match the start or end of the string<br>
-\ -- inhibit the "specialness" of a character. So, for example, use \. to match a period or \\ to match a slash. If you are unsure if a character has special meaning, such as '@', you can try putting a slash in front of it, \@. If its not a valid escape sequence, like \c, your python program will halt with an error.<br>

Repetition-
+ -- 1 or more occurrences of the pattern to its left, e.g. 'i+' = one or more i's<br>
* -- 0 or more occurrences of the pattern to its left<br>
? -- match 0 or 1 occurrences of the pattern to its left<br>

Group Extraction:regular expression allows you to pick out parts of the matching text<br>

Options:
-IGNORECASE -- ignore upper/lowercase differences for matching, so 'a' matches both 'a' and 'A'.<br>
-DOTALL -- allow dot (.) to match newline -- normally it matches anything but newline. This can trip you up -- you think .* matches everything, but by default it does not go past the end of a line. Note that \s (whitespace) includes newlines, so if you want to match a run of whitespace that may include a newline, you can just use \s*<br>
-MULTILINE -- Within a string made of many lines, allow ^ and $ to match the start and end of each line. Normally ^/$ would just match the start and end of the whole string.<br>

Utilities: <br>
File System -- os, os.path, shutil: The *os* and *os.path* modules include many functions to interact with the file system. The *shutil* module can copy files.<br>
-os module docs<br>
-filenames = os.listdir(dir) -- list of filenames in that directory path (not including . and ..). The filenames are just the names in the directory, not their absolute paths.<br>
-os.path.join(dir, filename) -- given a filename from the above list, use this to put the dir and filename together to make a path<br>
-os.path.abspath(path) -- given a path, return an absolute form, e.g. /home/nick/foo/bar.html<br>
-os.path.dirname(path), os.path.basename(path) -- given dir/foo/bar.html, return the dirname "dir/foo" and basename "bar.html"<br>
-os.path.exists(path) -- true if it exists<br>
-os.mkdir(dir_path) -- makes one dir, os.makedirs(dir_path) makes all the needed dirs in this path<br>
-shutil.copy(source-path, dest-path) -- copy a file (dest path directories should exist)<br>


Running External Processes -- subprocess:
The *subprocess* module is a simple way to run an external command and capture its output.<br>
-subprocess module docs<br>
-output = subprocess.check_output(cmd, stderr=subprocess.STDOUT) -- runs the command, waits for it to exit, and returns its output text. The command is run with its standard output and standard error combined into the one output text. -If it fails, it throws a CalledProcessError.<br>
-If you want more control over the running of the sub-process, see the subprocess.popen class<br>
-There is also a simple subprocess.call(cmd) which runs the command and dumps its output onto your output and returns its error code. This works if you want to run the command but do not need to capture its output into your python data structures.<br>

Exceptions: represents a run-time error that halts the normal execution at a particular line and transfers control to error handling code. Without any error handling code (as we have done thus far), a run-time exception just halts the program with an error message. You can add a "try/except" structure to your code to handle exceptions.<br>


HTTP -- urllib and urlparse:<br>
-The module *urllib.request* provides url fetching -- making a url look like a file you can read from. The *urlparse* module can take apart and put together urls.<br>

-urllib.request module docs<br>
-ufile = urllib.request.urlopen(url) -- returns a file like object for that url<br>
-text = ufile.read() -- can read from it, like a file (readlines() etc. also work)<br>
-info = ufile.info() -- the meta info for that request. info.gettype() is the mime type, e.g. 'text/html'<br>
-baseurl = ufile.geturl() -- gets the "base" url for the request, which may be different from the original because of redirects<br>
-urllib.request.urlretrieve(url, filename) -- downloads the url data to the given file path<br>
-urllib.parse.urljoin(baseurl, url) -- given a url that may or may not be full, and the baseurl of the page it comes from, return a full url. Use geturl() above to provide the base url.<br>
-All of exceptions are in urllib.error.<br>

