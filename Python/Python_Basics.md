### [Data Types](https://www.w3schools.com/python/python_datatypes.asp)
---
- Text Type:	`str`
- Numeric Types:	`int`, `float`, `complex`
- Sequence Types:	`list`, `tuple`, `range`
- Mapping Type:	`dict`
- Set Types:	`set`, `frozenset`
- Boolean Type:	`bool`
- Binary Types:	`bytes`, `bytearray`, `memoryview`
- None Type:	`NoneType`
### global Keyword
---
- To create a global variable inside a function, you can use the global keyword.
```py
global x
```
### Random Number
- Python does not have a random() function to make a random number, but Python has a **built-in module** called `random` that can be used to make random numbers:
```py
import random
# range (1-9)
print(random.randrange(1, 10))
```

### Walrus-operator
---
Walrus-operator is another name for assignment expressions. It is a way to assign to variables within an expression using the notation `NAME := expr`. The Assignment expressions allow a value to be assigned to a variable, even a variable that doesn’t exist yet.
```py
sample_data = [
	{"userId": 1, "name": "rahul", "completed": False},
	{"userId": 1, "name": "rohit", "completed": False},
	{"userId": 1, "name": "ram", "completed": False},
	{"userId": 1, "name": "ravan", "completed": True}
]

print("With Python 3.8 Walrus Operator:")
for entry in sample_data:
	if name := entry.get("name"):
		print(f'Found name: "{name}"')

print("Without Walrus operator:")
for entry in sample_data:
	name = entry.get("name")
	if name:
		print(f'Found name: "{name}"')
```
```py
nums  = [1, 2, 3, 4]
c = 0
l2 = [c := c + x for x in nums]
print(l2)
# output: [1, 2, 6, 10]
```
### Input
---
There are a number of ways in which we can take input from stdin in [Python](https://www.geeksforgeeks.org/python-programming-language/). 
-   [sys](https://www.geeksforgeeks.org/python-sys-module/).stdin
	- The **sys** module in python helps us to access the variables maintained by the interpreter. It also provides functions to interact with the interpreter.
``` py
import sys

for line in sys.stdin:
	if 'q' == line.rstrip():
		break
	print(f'Input : {line}')

print("Exit")

```
-   [input()](https://www.geeksforgeeks.org/python-input-function/)
-   [fileinput.input()](https://www.geeksforgeeks.org/fileinput-input-in-python/)
#### Output
- stdout
```python
import sys

def print_to_stdout(*a):

	# Here a is the array holding the objects
	# passed as the argument of the function
	print(*a, file=sys.stdout)

print_to_stdout("Hello World")

```
- logging
```python
import logging

logging.basicConfig(format='%(message)s')
log = logging.getLogger(__name__)
log.warning('Error: Hello World')
print('GeeksforGeeks')

```
### reduce() Function
---
> reduce(fn,list)

``` python
from functools import reduce

scores = [75, 65, 80, 95, 50]

total = reduce(lambda a, b: a + b, scores)

print(total)

```
### [for-else](https://www.pythontutorial.net/python-basics/python-for-else/)
---
* By using the `for else` statement, the program doesn’t need to use a `flag` and an `[if]` statement after the loop.
```py
for x in range(6):
  print(x)
else:
  print("Finally finished!")
```
### [while-else](https://www.w3schools.com/python/python_while_loops.asp)
```py
i = 1
while i < 6:
  print(i)
  i += 1
else:
  print("i is no longer less than 6")
  ```
### [args paramereter](https://www.pythontutorial.net/python-basics/python-args/)
---
* By convention, Python uses the `*args` for a variadic parameter.
* `*args`returns a tuple, not a list.


### [kwargs Parameter](https://www.pythontutorial.net/python-basics/python-kwargs/)
---
* The `**kwargs` is called a keyword parameter.
* When a function has the `**kwargs` parameter, it can accept a variable number of [keyword arguments](https://www.pythontutorial.net/python-basics/python-keyword-arguments/) as a [dictionary](https://www.pythontutorial.net/python-basics/python-dictionary/).
### [Partial Functions](https://www.pythontutorial.net/python-basics/python-partial-functions/)
---
* Partial functions are used to reduce the number of arguments of a function to simplify the function’s signature.
* The `partial` function returns new `partial` object, which is a [callable](https://www.pythontutorial.net/python-built-in-functions/python-callable/).
```python
functools.partial(fn, /, *args, **kwargs)
```
### [Type Hints](https://www.pythontutorial.net/python-basics/python-type-hints/)
---
- Mypy package; type checker tool

```python
name: str = 'Hello'
# name: str specifites paramter's type and -> str return value
def say_hi(name: str) -> str:
    return f'Hi {name}'
```
- Multiple type
```python
from typing import Union
# with  Union function
def add(x: Union[int, float], y: Union[int, float]) -> Union[int, float]:
    return x + y

# with union operator
def add(x: int | float, y: int | float) -> int | float:
    return x + y
```
### [File](https://www.pythontutorial.net/python-basics/python-create-text-file/)
---
*  Creating file in 'w' mode won't throw an error if it already exists but will rewrite the texts. So if we want to show error use 'x' mode which will return FileExistsError.
* You can also check the existing of file with these [build in methods](https://www.pythontutorial.net/python-basics/python-check-if-file-exists/).
### Yield
---
- **return sends a specified value back to its caller whereas yield can produce a sequence of values**. We should use yield when we want to iterate over a sequence, but don't want to store the entire sequence in memory. Yield is used in Python generators.
###  String Method
---
Method| Syntax | Description
:--- | --- | :--- 
capitalize()| string.capitalize() | Converts the first character to upper case
casefold()| string.casefold() | Converts string into lower case
center() | string.center(length, character) | Returns a centered string. Default character is space
count() | string.count(value, start, end) | Returns the number of times a specified value occurs in a string
encode() | string.encode(encoding=encoding, errors=errors) | Returns an encoded version of the string
endswith() | string.endswith(value, start, end) | Returns true if the string ends with the specified value
expandtabs()|string.expandtabs(tabsize) | Sets the tab size of the string
find() | string.find(value, start, end) | Searches the string for a specified value and returns the position of where it was found
[format()](https://www.w3schools.com/python/ref_string_format.asp)| string.format(value1, value2...)| Formats specified values in a string
format_map()| | Formats specified values in a string
index() | string.index(value, start, end) | Searches the string for a specified value and returns the position of where it was found
isalnum() | string.isalnum() | Returns True if all characters in the string are alphanumeric
isalpha() | string.isalpha() | Returns True if all characters in the string are in the alphabet
isdecimal() | string.isdecimal() | Returns True if all characters in the string are decimals
isdigit() | string.isdigit() | Returns True if all characters in the string are digits
isidentifier() | string.isidentifier() | Returns True if the string is an identifier. A string is considered a valid identifier if it only contains alphanumeric letters (a-z) and (0-9), or underscores (_). A valid identifier cannot start with a number, or contain any spaces.
islower() | string.islower() | Returns True if all characters in the string are lower case
isnumeric() | string.isnumeric() | Returns True if all characters in the string are numeric. Exponents, like ² and ¾ are also considered to be numeric values. "-1" and "1.5" are NOT considered numeric values, because all the characters in the string must be numeric, and the - and the . are not.
isprintable() | string.isprintable() | Returns True if all characters in the string are printable
isspace() | string.isspace() | Returns True if all characters in the string are whitespaces
istitle() | string.istitle() | Returns True if the string follows the rules of a title
isupper() | string.isupper() | Returns True if all characters in the string are upper case
join() | string.join(iterable) | Joins the elements of an iterable to the end of the string
ljust() | string.ljust(length, character) | Returns a left justified version of the string. When using a **dictionary** as an iterable, the returned values are the **keys**, not the values.
lower() | string.lower() | Converts a string into lower case
lstrip() | string.lstrip(characters) | Returns a left trim version of the string
[maketrans()](https://www.w3schools.com/python/ref_string_maketrans.asp) | string.maketrans(x, y, z) | Returns a translation table(**dictionary**) to be used in translations
partition() | string.partition(value) | Returns a tuple where the string is parted into three parts(before the "match", the "match", after the "match"). If specified value is not found returns (string, '', '' )
replace() | string.replace(oldvalue, newvalue, count) | Returns a string where all occurrences of specified value is replaced with a specified value
rfind() | string.rfind(value, start, end) | Searches the string for a specified value and returns the last position of where it was found
rindex() | string.rindex(value, start, end) | Searches the string for a specified value and returns the last position of where it was found
rjust() | string.rjust(length, character) | Returns a right justified version of the string
rpartition() | Returns a tuple where the string is parted into three parts. If specified value is not found returns ( '', '',  the whole string )
rsplit() | string.rsplit(separator, maxsplit) |Splits the string at the specified separator, and returns a list
rstrip() | string.rstrip(characters) | Returns a right trim version of the string
split() | string.split(separator, maxsplit) | Splits the string at the specified separator, and returns a list
splitlines() | string.splitlines(keeplinebreaks) | Splits the string at line breaks and returns a list. Default value of keeplinebreaks is `False`. 
startswith() | string.startswith(value, start, end) | Returns true if the string starts with the specified value
strip() | string.strip(characters) | Returns a trimmed version of the string
swapcase() | string.swapcase() | swaps cases, lower case becomes upper case and vice versa
title() | string.title() | Converts the first character of each word to upper case. The first letter after a **non-alphabet letter** is converted into a upper case letter
translate() | string.translate(table) | Returns a translated string. If you use a **dictionary**, you must use **ascii codes** instead of characters.
upper() | string.upper() | Converts a string into upper case
zfill() | string.zfill(len) | Fills the string with a specified number of 0 values at the beginning

### [Format Method](https://www.w3schools.com/python/ref_string_format.asp)
---
Placeholder|Description
---|---
:<	| Left aligns the result (within the available space)
:>	| Right aligns the result (within the available space)
:^	| Center aligns the result (within the available space)
:=	| Places the sign to the left most position
:+	| Use a plus sign to indicate if the result is positive or negative
:-	| Use a minus sign for negative values only
:	| Use a space to insert an extra space before positive numbers (and a minus sign before negative numbers)
:,	| Use a comma as a thousand separator
:_	| Use a underscore as a thousand separator
:b	| Binary format
:c		Converts the value into the corresponding unicode character
:d	| Decimal format
:e	| Scientific format, with a lower case e
:E	| Scientific format, with an upper case E
:f	| Fix point number format
:F	| Fix point number format, in uppercase format (show inf and nan as INF and NAN)
:g	| General format
:G	| General format (using a upper case E for scientific notations)
:o	| Octal format
:x	| Hex format, lower case
:X	| Hex format, upper case
:n	| Number format
:%	| Percentage format

### Operators
---
- Arithmetic operators
- Assignment operators
- Comparison operators
- Logical operators
- Identity operators (`is` , `is not`)
- Membership operators (`in`, `not in`)
- Bitwise operators

### Collections (Arrays)
There are four collection data types in the Python programming language:

- **List** is a collection which is ordered and changeable. Allows duplicate members.
- **Tuple** is a collection which is ordered and unchangeable. Allows duplicate members.
- **Set** is a collection which is unordered, unchangeable*, and unindexed. No duplicate members.
- **Dictionary** is a collection which is ordered** and changeable. No duplicate members.

**Note**
- *Set items are unchangeable, but you can remove and/or add items whenever you like.

- **As of Python version 3.7, dictionaries are ordered. In Python 3.6 and earlier, dictionaries are unordered.

### List
---
- To check if an element is present without getting error try these -
	- `if item in list`
	- `list.__contains__(value)`
#### List Comprehension
> newlist = [expression for item in iterable if condition == True]
```py
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]

# Return the item if it is not banana, if it is banana return orange
newlist = [x if x != "banana" else "orange" for x in fruits]

print(newlist)
```
Output:
```py
['apple', 'orange', 'cherry', 'kiwi', 'mango']
```
### Dictionary
Method| Syntax | Description
:--- | --- | :---
clear() | dictionary.clear() | Removes all the elements from the dictionary
copy() | dictionary.copy() | Returns a copy of the dictionary
fromkeys() | dictionary.fromkeys(keys, value) | Returns a dictionary with the specified keys and value(default is None)
get() | dictionary.get(key) | Returns the value of the specified key
items() | dictionary.items() | Returns a list containing a tuple for each key value pair
keys() | dictionary.keys() | Returns a list containing the dictionary's keys
pop() | dictionary.pop(keyname, defaultvalue) | Removes the element with the specified key. If this parameter is not specified, and the no item with the specified key is found, an error is raised.
popitem() | dictionary.popitem() | Removes the last inserted key-value pair
setdefault() | dictionary.setdefault(keyname, value) | dictReturns the value of the specified key. If the key does not exist: insert the key, with the specified value
update() | dictionary.update(dict) | Updates the dictionary with the specified key-value pairs
values() | dictionary.values() | Returns a list of all the values in the dictionary