**Everything in Python is an object including a [Class](https://www.pythontutorial.net/python-oop/python-class/).**
### Class Variables
- Python stores class variables in the `__dict__` attribute. The `__dict__` is a mapping proxy, which is a dictionary.
#### Aceess
- Dot (.) notation
- `getattr()`
	- If the class variable doesn’t exist, python will throw `AttributeError` exception. To avoid the exception, you can specify a default value if the class variable doesn’t exist like this:
		```python
		media_type = getattr(HtmlDocument, 'media_type', 'text/html')
		print(media_type) # text/html
		```
#### Set Value
- `setattr()`
#### Delete 
- `delattr()`
- `del`
### Class Function
- When a function is defined inside a class, it’s purely a function. However, that function is accessed via an object, the function becomes a **method**.
- Python always implicitly passes the **object to the method** as the first argument.
- When a method creates an instance of the class and returns it, the method is called a **factory method**.
### [Static Method](https://www.pythontutorial.net/python-oop/python-static-methods/)
- Static methods aren’t bound to an object so it cannot access and modify an object state.

- In addition, Python doesn’t implicitly pass the `cls` parameter (or the `self` parameter) to static methods. Therefore, static methods cannot access and modify the class’s state.

- In practice, you use static methods to define utility methods or group [functions](https://www.pythontutorial.net/python-basics/python-functions/) that have some logical relationships in a class.
### [Property](https://www.pythontutorial.net/python-oop/python-properties/)
* To define a getter and setter method while achieving backward compatibility, you can use the `property()` class.
```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def set_age(self, age):
        if age <= 0:
            raise ValueError('The age must be positive')
        self._age = age

    def get_age(self):
        return self._age

    age = property(fget=get_age, fset=set_age)
```

> [Cache calculated properties](https://www.pythontutorial.net/python-oop/python-readonly-property/)

### [Enumeration](https://www.pythontutorial.net/python-oop/python-enumeration/)
```python
from enum import Enum


class Color(Enum):
    RED = 1
    GREEN = 2
    BLUE = 3
```

- A member and its associated value are not equal. The following example returns `False`:
```python
if Color.RED == 1:
    print('Color.RED == 1')
else:
    print('Color.RED != 1')
```
- Enumeration members are always [hashable](https://www.pythontutorial.net/python-oop/python-__hash__/). It means that you can use the enumeration members as keys in a [dictionary](https://www.pythontutorial.net/python-basics/python-dictionary/) or as elements of a [Set](https://www.pythontutorial.net/python-basics/python-set/).
- An enumeration cannot be inherited unless it contains no members.
- By default, all members of an enumeration are truthy.
- When you define multiple members in an enumeration with the same values, Python does not create different members but [Enum aliases](https://www.pythontutorial.net/python-oop/python-enum-unique/)
- To standardize the status codes from different systems, we can use enumeration aliases.
```python
from enum import Enum


class ResponseStatus(Enum):
    # in progress
    IN_PROGRESS = 1
    REQUESTING = 1
    PENDING = 1

    # success
    SUCCESS = 2
    OK = 2
    FULFILLED = 2

    # error
    ERROR = 3
    NOT_OK = 3
    REJECTED = 3
code = 'OK'
if ResponseStatus[code] is ResponseStatus.SUCCESS:
    print('The request completed successfully')
```