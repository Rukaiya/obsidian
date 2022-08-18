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
