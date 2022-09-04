#### Input
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

#### List
- To check if an element is present without getting error try these -
	- `if item in list`
	- `list.__contains__(value)`

#### reduce() Function
> reduce(fn,list)

``` python
from functools import reduce

scores = [75, 65, 80, 95, 50]

total = reduce(lambda a, b: a + b, scores)

print(total)

```
#### [for-else](https://www.pythontutorial.net/python-basics/python-for-else/)
* By using the `for else` statement, the program doesn’t need to use a `flag` and an `[if]` statement after the loop.

#### [args paramereter](https://www.pythontutorial.net/python-basics/python-args/)
* By convention, Python uses the `*args` for a variadic parameter.
* `*args`returns a tuple, not a list.


#### [kwargs Parameter](https://www.pythontutorial.net/python-basics/python-kwargs/)
* The `**kwargs` is called a keyword parameter.
* When a function has the `**kwargs` parameter, it can accept a variable number of [keyword arguments](https://www.pythontutorial.net/python-basics/python-keyword-arguments/) as a [dictionary](https://www.pythontutorial.net/python-basics/python-dictionary/).
#### [Partial Functions](https://www.pythontutorial.net/python-basics/python-partial-functions/)
* Partial functions are used to reduce the number of arguments of a function to simplify the function’s signature.
* The `partial` function returns new `partial` object, which is a [callable](https://www.pythontutorial.net/python-built-in-functions/python-callable/).
```python
functools.partial(fn, /, *args, **kwargs)
```
#### [Type Hints](https://www.pythontutorial.net/python-basics/python-type-hints/)
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
#### [File](https://www.pythontutorial.net/python-basics/python-create-text-file/)
*  Creating file in 'w' mode won't throw an error if it already exists but will rewrite the texts. So if we want to show error use 'x' mode which will return FileExistsError.
* You can also check the existing of file with these [build in methods](https://www.pythontutorial.net/python-basics/python-check-if-file-exists/).
#### Yield
- **return sends a specified value back to its caller whereas yield can produce a sequence of values**. We should use yield when we want to iterate over a sequence, but don't want to store the entire sequence in memory. Yield is used in Python generators.