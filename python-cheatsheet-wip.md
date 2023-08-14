# Python3

**Author:** David Boyd<br>
**Date:** 2023-08-14

## Table of Contents

- [Code Blocks](#code-blocks)
  - [Try Except](#try-except)
- [Built-in functions](#built-in-functions)
- [String Methods](#string-methods)
- [List Methods](#list-methods)
- [Dictionary Methods](#dictionary-methods)
- [Tuple Methods](#tuple-methods)
- [Set Methods](#set-methods)
- [File Methods](#file-methods)
- [RegEx](#regex)

## Code Blocks

### Try Except

| Code      | Description                                                                         |
|-----------|-------------------------------------------------------------------------------------|
| `try`     | block lets you test a block of code for errors.                                     |
| `except`  | block lets you handle the error.                                                    |
| `else`    | block lets you execute code when there is no error.                                 |
| `finally` | block lets you execute code, regardless of the result of the try-and-except blocks. |
| `raise`   | block lets you throw an exception (on your choosing) if a condition occurs          |

Try except example:

``` python3
try:
  f = open("demofile.txt")
  try:
    f.write("Lorum Ipsum")
  except:
    print("Something went wrong when writing to the file")
  finally:
    f.close()
except:
  print("Something went wrong when opening the file")
```

Raise an exception example:

``` python3
 x = -1

if x < 0:
  raise Exception("Sorry, no numbers below zero")
```

## Built-in functions

| Function         | Description                                                                                   |
|------------------|-----------------------------------------------------------------------------------------------|
| `abs()`          | Returns the absolute value of a number                                                        |
| `all()`          | Returns True if all items in an iterable object are true                                      |
| `any()`          | Returns True if any item in an iterable object is true                                        |
| `ascii()`        | Returns a readable version of an object. Replaces none-ascii characters with escape character |
| `bin()`          | Returns the binary version of a number                                                        |
| `bool()`         | Returns the boolean value of the specified object                                             |
| `bytearray()`    | Returns an array of bytes                                                                     |
| `bytes()`        | Returns a bytes object                                                                        |
| `callable()`     | Returns True if the specified object is callable, otherwise False                             |
| `chr()`          | Returns a character from the specified Unicode code.                                          |
| `classmethod()`  | Converts a method into a class method                                                         |
| `compile()`      | Returns the specified source as an object, ready to be executed                               |
| `complex()`      | Returns a complex number                                                                      |
| `delattr()`      | Deletes the specified attribute (property or method) from the specified object                |
| `dict()`         | Returns a dictionary (Array)                                                                  |
| `dir()`          | Returns a list of the specified object's properties and methods                               |
| `divmod()`       | Returns the quotient and the remainder when argument1 is divided by argument2                 |
| `enumerate()`    | Takes a collection (e.g. a tuple) and returns it as an enumerate object                       |
| `eval()`         | Evaluates and executes an expression                                                          |
| `exec()`         | Executes the specified code (or object)                                                       |
| `filter()`       | Use a filter function to exclude items in an iterable object                                  |
| `float()`        | Returns a floating point number                                                               |
| `format()`       | Formats a specified value                                                                     |
| `frozenset()`    | Returns a frozenset object                                                                    |
| `getattr()`      | Returns the value of the specified attribute (property or method)                             |
| `globals()`      | Returns the current global symbol table as a dictionary                                       |
| `hasattr()`      | Returns True if the specified object has the specified attribute (property/method)            |
| `hash()`         | Returns the hash value of a specified object                                                  |
| `help()`         | Executes the built-in help system                                                             |
| `hex()`          | Converts a number into a hexadecimal value                                                    |
| `id()`           | Returns the id of an object                                                                   |
| `import()`       | This function is invoked by the import statement.                                             |
| `input()`        | Allowing user input                                                                           |
| `int()`          | Returns an integer number                                                                     |
| `isinstance()`   | Returns True if a specified object is an instance of a specified object                       |
| `issubclass()`   | Returns True if a specified class is a subclass of a specified object                         |
| `iter()`         | Returns an iterator object                                                                    |
| `len()`          | Returns the length of an object                                                               |
| `list()`         | Returns a list                                                                                |
| `locals()`       | Returns an updated dictionary of the current local symbol table                               |
| `map()`          | Returns the specified iterator with the specified function applied to each item               |
| `max()`          | Returns the largest item in an iterable                                                       |
| `memoryview()`   | Returns a memory view object                                                                  |
| `min()`          | Returns the smallest item in an iterable                                                      |
| `next()`         | Returns the next item in an iterable                                                          |
| `object()`       | Returns a new object                                                                          |
| `oct()`          | Converts a number into an octal                                                               |
| `open()`         | Opens a file and returns a file object                                                        |
| `ord()`          | Convert an integer representing the Unicode of the specified character                        |
| `pow()`          | Returns the value of x to the power of y                                                      |
| `print()`        | Prints to the standard output device                                                          |
| `property()`     | Gets, sets, deletes a property                                                                |
| `range()`        | Returns a sequence of numbers, starting from 0 and increments by 1 (by default)               |
| `repr()`         | Returns a readable version of an object                                                       |
| `reversed()`     | Returns a reversed iterator                                                                   |
| `round()`        | Rounds a numbers                                                                              |
| `set()`          | Returns a new set object                                                                      |
| `setattr()`      | Sets an attribute (property/method) of an object                                              |
| `slice()`        | Returns a slice object                                                                        |
| `sorted()`       | Returns a sorted list                                                                         |
| `staticmethod()` | Converts a method into a static method                                                        |
| `str()`          | Returns a string object                                                                       |
| `sum()`          | Sums the items of an iterator                                                                 |
| `super()`        | Returns an object that represents the parent class                                            |
| `tuple()`        | Returns a tuple                                                                               |
| `type()`         | Returns the type of an object                                                                 |
| `vars()`         | Returns the __dict__ property of an object                                                    |
| `zip()`          | Returns an iterator, from two or more iterators                                               |

## String Methods

| Method           | Description                                                                                   |
|------------------|-----------------------------------------------------------------------------------------------|
| `capitalize()`   | Converts the first character to upper case                                                    |
| `casefold()`     | Converts string into lower case                                                               |
| `center()`       | Returns a centered string                                                                     |
| `count()`        | Returns the number of times a specified value occurs in a string                              |
| `encode()`       | Returns an encoded version of the string                                                      |
| `endswith()`     | Returns true if the string ends with the specified value                                      |
| `expandtabs()`   | Sets the tab size of the string                                                               |
| `find()`         | Searches the string for a specified value and returns the position of where it was found      |
| `format()`       | Formats specified values in a string                                                          |
| `format_map()`   | Formats specified values in a string                                                          |
| `index()`        | Searches the string for a specified value and returns the position of where it was found      |
| `isalnum()`      | Returns True if all characters in the string are alphanumeric                                 |
| `isalpha()`      | Returns True if all characters in the string are in the alphabet                              |
| `isascii()`      | Returns True if all characters in the string are ascii characters                             |
| `isdecimal()`    | Returns True if all characters in the string are decimals                                     |
| `isdigit()`      | Returns True if all characters in the string are digits                                       |
| `isidentifier()` | Returns True if the string is an identifier                                                   |
| `islower()`      | Returns True if all characters in the string are lower case                                   |
| `isnumeric()`    | Returns True if all characters in the string are numeric                                      |
| `isprintable()`  | Returns True if all characters in the string are printable                                    |
| `isspace()`      | Returns True if all characters in the string are whitespaces                                  |
| `istitle()`      | Returns True if the string follows the rules of a title                                       |
| `isupper()`      | Returns True if all characters in the string are upper case                                   |
| `join()`         | Converts the elements of an iterable into a string                                            |
| `ljust()`        | Returns a left justified version of the string                                                |
| `lower()`        | Converts a string into lower case                                                             |
| `lstrip()`       | Returns a left trim version of the string                                                     |
| `maketrans()`    | Returns a translation table to be used in translations                                        |
| `partition()`    | Returns a tuple where the string is parted into three parts                                   |
| `replace()`      | Returns a string where a specified value is replaced with a specified value                   |
| `rfind()`        | Searches the string for a specified value and returns the last position of where it was found |
| `rindex()`       | Searches the string for a specified value and returns the last position of where it was found |
| `rjust()`        | Returns a right justified version of the string                                               |
| `rpartition()`   | Returns a tuple where the string is parted into three parts                                   |
| `rsplit()`       | Splits the string at the specified separator, and returns a list                              |
| `rstrip()`       | Returns a right trim version of the string                                                    |
| `split()`        | Splits the string at the specified separator, and returns a list                              |
| `splitlines()`   | Splits the string at line breaks and returns a list                                           |
| `startswith()`   | Returns true if the string starts with the specified value                                    |
| `strip()`        | Returns a trimmed version of the string                                                       |
| `swapcase()`     | Swaps cases, lower case becomes upper case and vice versa                                     |
| `title()`        | Converts the first character of each word to upper case                                       |
| `translate()`    | Returns a translated string                                                                   |
| `upper()`        | Converts a string into upper case                                                             |
| `zfill()`        | Fills the string with a specified number of 0 values at the beginning                         |

### List Methods

| Method      | Description                                                                  |
|-------------|------------------------------------------------------------------------------|
| `append()`  | Adds an element at the end of the list                                       |
| `clear()`   | Removes all the elements from the list                                       |
| `copy()`    | Returns a copy of the list                                                   |
| `count()`   | Returns the number of elements with the specified value                      |
| `extend()`  | Add the elements of a list (or any iterable), to the end of the current list |
| `index()`   | Returns the index of the first element with the specified value              |
| `insert()`  | Adds an element at the specified position                                    |
| `pop()`     | Removes the element at the specified position                                |
| `remove()`  | Removes the first item with the specified value                              |
| `reverse()` | Reverses the order of the list                                               |
| `sort()`    | Sorts the list                                                               |

## Dictionary Methods

| Method         | Description                                                                                                 |
|----------------|-------------------------------------------------------------------------------------------------------------|
| `clear()`      | Removes all the elements from the dictionary                                                                |
| `copy()`       | Returns a copy of the dictionary                                                                            |
| `fromkeys()`   | Returns a dictionary with the specified keys and value                                                      |
| `get()`        | Returns the value of the specified key                                                                      |
| `items()`      | Returns a list containing a tuple for each key value pair                                                   |
| `keys()`       | Returns a list containing the dictionary's keys                                                             |
| `pop()`        | Removes the element with the specified key                                                                  |
| `popitem()`    | Removes the last inserted key-value pair                                                                    |
| `setdefault()` | Returns the value of the specified key. If the key does not exist: insert the key, with the specified value |
| `update()`     | Updates the dictionary with the specified key-value pairs                                                   |
| `values()`     | Returns a list of all the values in the dictionary                                                          |

## Tuple Methods

| Method    | Description                                                                             |
|-----------|-----------------------------------------------------------------------------------------|
| `count()` | Returns the number of times a specified value occurs in a tuple                         |
| `index()` | Searches the tuple for a specified value and returns the position of where it was found |

## Set Methods

| Method                          | Description                                                                    |
|---------------------------------|--------------------------------------------------------------------------------|
| `add()`                         | Adds an element to the set                                                     |
| `clear()`                       | Removes all the elements from the set                                          |
| `copy()`                        | Returns a copy of the set                                                      |
| `difference()`                  | Returns a set containing the difference between two or more sets               |
| `difference_update()`           | Removes the items in this set that are also included in another, specified set |
| `discard()`                     | Remove the specified item                                                      |
| `intersection()`                | Returns a set, that is the intersection of two or more sets                    |
| `intersection_update()`         | Removes the items in this set that are not present in other, specified set(s)  |
| `isdisjoint()`                  | Returns whether two sets have a intersection or not                            |
| `issubset()`                    | Returns whether another set contains this set or not                           |
| `issuperset()`                  | Returns whether this set contains another set or not                           |
| `pop()`                         | Removes an element from the set                                                |
| `remove()`                      | Removes the specified element                                                  |
| `symmetric_difference()`        | Returns a set with the symmetric differences of two sets                       |
| `symmetric_difference_update()` | inserts the symmetric differences from this set and another                    |
| `union()`                       | Return a set containing the union of sets                                      |
| `update()`                      | Update the set with another set, or any other iterable                         |

## File Methods

| Method         | Description                                                                          |
|----------------|--------------------------------------------------------------------------------------|
| `close()`      | Closes the file                                                                      |
| `detach()`     | Returns the separated raw stream from the buffer                                     |
| `fileno()`     | Returns a number that represents the stream, from the operating system's perspective |
| `flush()`      | Flushes the internal buffer                                                          |
| `isatty()`     | Returns whether the file stream is interactive or not                                |
| `read()`       | Returns the file content                                                             |
| `readable()`   | Returns whether the file stream can be read or not                                   |
| `readline()`   | Returns one line from the file                                                       |
| `readlines()`  | Returns a list of lines from the file                                                |
| `seek()`       | Change the file position                                                             |
| `seekable()`   | Returns whether the file allows us to change the file position                       |
| `tell()`       | Returns the current file position                                                    |
| `truncate()`   | Resizes the file to a specified size                                                 |
| `writable()`   | Returns whether the file can be written to or not                                    |
| `write()`      | Writes the specified string to the file                                              |
| `writelines()` | Writes a list of strings to the file                                                 |

## RegEx

| `import re` | `re` module offers a set of functions that allows us to search a string for a match |
|-------------|-------------------------------------------------------------------------------------|

- [RegEx Functions](#regex-functions)
- [RegEx Metacharacters](#regex-metacharacters)
- [RegEx Special Sequences](#regex-specials-sequences)
- [RegEx Sets](#regex-sets)

### RegEx Functions

The re module offers a set of functions that allows us to search a string for a match:

| Method    | Description                                                       |
|-----------|-------------------------------------------------------------------|
| `findall` | Returns a list containing all matches                             |
| `search`  | Returns a Match object if there is a match anywhere in the string |
| `split`   | Returns a list where the string has been split at each match      |
| `sub`     | Replaces one or many matches with a string                        |

## RegEx Metacharacters

Metacharacters are characters with a special meaning:

| Character | Description                                                                | Example        |
|-----------|----------------------------------------------------------------------------|----------------|
| `[]`      | A set of characters                                                        | "[a-m]"        |
| `\`       | Signals a special sequence<br>(can also be used to escape special characters) | "\d"           |
| `.`       | Any character (except newline character)                                   | "he..o"        |
| `^`       | Starts with                                                                | "^hello"       |
| `$`       | Ends with                                                                  | "planet$"      |
| `*`       | Zero or more occurrences                                                   | "he.*o"        |
| `+`       | One or more occurrences                                                    | "he.+o"        |
| `?`       | Zero or one occurrences                                                    | "he.?o"        |
| `{}`      | Exactly the specified number of occurrences                                | "he.{2}o"      |
| `\|`      | Either or                                                                  | "falls\|stays" |
| `()`      | Capture and group                                                          |                |

## RegEx Special Sequences

A special sequence is a `\` (backslash) followed by >=1 characters in the list
below and has a speial meaning:

| Character | Description                                                                                                                                                                                                    | Example              |
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| `\A`      | Returns a match if the specified characters are at the beginning of the string                                                                                                                                 | "\AThe"              |
| `\b`      | Returns a match where the specified characters are at the beginning or at the end of a word<br>(the "r" in the beginning is making sure that the string is being treated as a "raw string")                    | r"\bain"<br>r"ain\b" |
| `\B`      | Returns a match where the specified characters are present, but NOT at the beginning (or at the end) of a word<br>(the "r" in the beginning is making sure that the string is being treated as a "raw string") | r"\Bain"<br>r"ain\B" |
| \d        | Returns a match where the string contains digits (numbers from 0-9)                                                                                                                                            | "\d"                 |
| \D        | Returns a match where the string DOES NOT contain digits                                                                                                                                                       | "\D"                 |
| \s        | Returns a match where the string contains a white space character                                                                                                                                              | "\s"                 |
| \S        | Returns a match where the string DOES NOT contain a white space character                                                                                                                                      | "\S"                 |
| \w        | Returns a match where the string contains any word characters (characters from a to Z, digits from 0-9, and the underscore _ character)                                                                        | "\w"                 |
| \W        | Returns a match where the string DOES NOT contain any word characters                                                                                                                                          | "\W"                 |
| \Z        | Returns a match if the specified characters are at the end of the string                                                                                                                                       | "Spain\Z"            |

### RegEx Sets

A set is a set of characters inside a pair of square brackets `[]` with a
special meaning:

| Set          | Description                                                                                |
|--------------|--------------------------------------------------------------------------------------------|
| `[arn]`      | Returns a match where one of the specified characters (a, r, or n) is present              |
| `[a-n]`      | Returns a match for any lower case character, alphabetically between a and n               |
| `[^arn]`     | Returns a match for any character EXCEPT a, r, and n                                       |
| `[0123]`     | Returns a match where any of the specified digits (0, 1, 2, or 3) are present              |
| `[0-9]`      | Returns a match for any digit between 0 and 9                                              |
| `[0-5][0-9]` | Returns a match for any two-digit numbers from 00 and 59                                   |
| `[a-zA-Z]`   | Returns a match for any character alphabetically between a and z, lower case OR upper case |
| `[+]`        | In sets, +, *, .,                                                                          | , (), $,{} has no special meaning, so [+] means: return a match for any + character in the string |

<!-- References -->

