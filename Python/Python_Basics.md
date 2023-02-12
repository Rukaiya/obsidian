## [Data Types](https://www.w3schools.com/python/python_datatypes.asp)
---
- Text Type:	`str`
- Numeric Types:	`int`, `float`, `complex`
- Sequence Types:	`list`, `tuple`, `range`
- Mapping Type:	`dict`
- Set Types:	`set`, `frozenset`
- Boolean Type:	`bool`
- Binary Types:	`bytes`, `bytearray`, `memoryview`
- None Type:	`NoneType`
## global Keyword
---
- To create a global variable inside a function, you can use the global keyword.
```py
global x
```
## Random Number
- Python does not have a random() function to make a random number, but Python has a **built-in module** called `random` that can be used to make random numbers:
```py
import random
# range (1-9)
print(random.randrange(1, 10))
```

## Walrus-operator
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
## Input
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
### Output
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
## reduce() Function
---
> reduce(fn,list)

``` python
from functools import reduce

scores = [75, 65, 80, 95, 50]

total = reduce(lambda a, b: a + b, scores)

print(total)

```
## [for-else](https://www.pythontutorial.net/python-basics/python-for-else/)
---
* By using the `for else` statement, the program doesn’t need to use a `flag` and an `[if]` statement after the loop.
```py
for x in range(6):
  print(x)
else:
  print("Finally finished!")
```
## [while-else](https://www.w3schools.com/python/python_while_loops.asp)
```py
i = 1
while i < 6:
  print(i)
  i += 1
else:
  print("i is no longer less than 6")
  ```
## [args paramereter](https://www.pythontutorial.net/python-basics/python-args/)
---
* By convention, Python uses the `*args` for a variadic parameter.
* `*args`returns a tuple, not a list.


## [kwargs Parameter](https://www.pythontutorial.net/python-basics/python-kwargs/)
---
* The `**kwargs` is called a keyword parameter.
* When a function has the `**kwargs` parameter, it can accept a variable number of [keyword arguments](https://www.pythontutorial.net/python-basics/python-keyword-arguments/) as a [dictionary](https://www.pythontutorial.net/python-basics/python-dictionary/).
## [Partial Functions](https://www.pythontutorial.net/python-basics/python-partial-functions/)
---
* Partial functions are used to reduce the number of arguments of a function to simplify the function’s signature.
* The `partial` function returns new `partial` object, which is a [callable](https://www.pythontutorial.net/python-built-in-functions/python-callable/).
```python
functools.partial(fn, /, *args, **kwargs)
```
## [Type Hints](https://www.pythontutorial.net/python-basics/python-type-hints/)
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
## [File](https://www.pythontutorial.net/python-basics/python-create-text-file/)
---
*  Creating file in 'w' mode won't throw an error if it already exists but will rewrite the texts. So if we want to show error use 'x' mode which will return FileExistsError.
* You can also check the existing of file with these [build in methods](https://www.pythontutorial.net/python-basics/python-check-if-file-exists/).
## Yield
---
- **return sends a specified value back to its caller whereas yield can produce a sequence of values**. We should use yield when we want to iterate over a sequence, but don't want to store the entire sequence in memory. Yield is used in Python generators.

## Operators
---
- Arithmetic operators
- Assignment operators
- Comparison operators
- Logical operators
- Identity operators (`is` , `is not`)
- Membership operators (`in`, `not in`)
- Bitwise operators

## Collections (Arrays)
There are four collection data types in the Python programming language:

- **List** is a collection which is ordered and changeable. Allows duplicate members.
- **Tuple** is a collection which is ordered and unchangeable. Allows duplicate members.
- **Set** is a collection which is unordered, unchangeable*, and unindexed. No duplicate members.
- **Dictionary** is a collection which is ordered** and changeable. No duplicate members.

**Note**
- *Set items are unchangeable, but you can remove and/or add items whenever you like.

- **As of Python version 3.7, dictionaries are ordered. In Python 3.6 and earlier, dictionaries are unordered.

## List
---
- To check if an element is present without getting error try these -
	- `if item in list`
	- `list.__contains__(value)`
### List Comprehension
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
## Tuple
---
- One item tuple
```py
# must use comma otherwise it'll be a string
thistuple = ("apple",)
print(type(thistuple))
```
## Array
---

```py
# A function that returns the length of the value:
def myFunc(e):
  return len(e)

cars = ['Ford', 'Mitsubishi', 'BMW', 'VW']

cars.sort(reverse=True, key=myFunc)
```
## Iterator
--- 
- An iterator is an object which implements the iterator protocol, which consist of the methods `__iter__()` and `__next__()`.
- Lists, tuples, dictionaries, and sets are all iterable objects. They are iterable containers which you can get an iterator from. All these objects have a `iter()` method which is used to get an iterator:
- The for loop actually creates an iterator object and executes the next() method for each loop.
- The `__iter__()` method acts similar, you can do operations (initializing etc.), but must always **return** the iterator object itself.
- The `__next__()` method also allows you to do operations, and must **return** the next item in the sequence.
```py
class MyNumbers:
  def __iter__(self):
    self.a = 1
    return self

# to stop the iteration StopIteration is used
  def __next__(self):
    if self.a <= 20:
      x = self.a
      self.a += 1
      return x
    else:
      raise StopIteration

myclass = MyNumbers()
myiter = iter(myclass)

for x in myiter:
  print(x)
```