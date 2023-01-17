### Display
---
- Writing into an HTML element, using `innerHTML`.
- Writing into the HTML output using `document.write()`.
- Writing into an alert box, using `window.alert()`.
- Writing into the browser console, using `console.log()`.

> Never call document.write after the document has finished loading.
It will overwrite the whole document.
```html
<button type="button" onclick="document.write(5 + 6)">Try it</button>
```
>  The window object is the global scope object. This also means that specifying the window keyword is optional.
```js
alert(5 + 6);
```
> JavaScript does not have any print object or print methods.You cannot access output devices from JavaScript.

> The only exception is that you can call the window.print() method in the browser to print the content of the current window.

### Const Keyword
---
> The keyword const does not define a constant value. It defines a constant reference to a value.

Because of this you can NOT:

- Reassign a constant value
- Reassign a constant array
- Reassign a constant object
But you CAN:

- Change the elements of constant array
- Change the properties of constant object

### Data Type
---
JavaScript has 8 Datatypes
1. String
2. Number
3. Bigint
4. Boolean
5. Undefined
6. Null
7. Symbol
8. Object

The object data type can contain:

1. An object
2. An array
3. A date

### Objects
---
> Declare objects with the const keyword
> Avoid String, Number, and Boolean objects. They complicate your code and slow down execution speed.
```js
x = new String();        // Declares x as a String object
y = new Number();        // Declares y as a Number object
z = new Boolean();       // Declares z as a Boolean object
```
> Comparing two JavaScript objects always returns false.

### this Keyword
---
- In an object method, this refers to the object.
- Alone, this refers to the global object.
- In a function, this refers to the global object.
- In a function, in strict mode, this is undefined.
- In an event, this refers to the element that received the event.
- Methods like call(), apply(), and bind() can refer this to any object.
### String
---
> `substring()` is similar to slice(). The difference is that start and end values less than 0 are treated as 0 in `substring()`.

> `substr()` is similar to slice(). The difference is that the second parameter specifies the length of the extracted part.

> The `replace()` method does not change the string it is called on. The `replace()` method returns a new string. The `replace()` method replaces only the first match
```js

// case insensitive
let text = "Please visit Microsoft!";
let newText = text.replace(/MICROSOFT/i, "W3Schools");

// replaces all occurences
let text = "Please visit Microsoft and Microsoft!";
let newText = text.replace(/Microsoft/g, "W3Schools");

```
> The `replaceAll()` method allows you to specify a regular expression instead of a string to be replaced. If the parameter is a regular expression, the global flag (g) must be set set, otherwise a TypeError is thrown.

Property access might be a little unpredictable:

- It makes strings look like arrays (but they are not)
If no character is found, [ ] returns undefined, while charAt() returns an empty string.
It is read only. str[0] = "A" gives no error (but does not work!)
> The `lastIndexOf()` methods searches backwards (from the end to the beginning), meaning: if the second parameter is 15, the search starts at position 15, and searches to the beginning of the string.

> The `search()` method cannot take a second start position argument. The `indexOf()` method cannot take powerful search values (regular expressions).
### BigInt
---
> JavaScript integers are only accurate up to 15 digits.

> Up to 9007199254740991 +(253-1) and Down to -9007199254740991 -(253-1).

> Arithmetic between a BigInt and a Number is not allowed (type conversion lose information). Unsigned right shift (>>>) can not be done on a BigInt

> MAX_SAFE_INTEGER
MIN_SAFE_INTEGER

```js
let x = Number.MAX_SAFE_INTEGER;
let x = Number.MIN_SAFE_INTEGER;
```
### Number Method
> The valueOf() method is used internally in JavaScript to convert Number objects to primitive values.
All JavaScript data types have a valueOf() and a toString() method.

> Number() can also convert a date to a number.
The Number() method returns the number of milliseconds since 1.1.1970.
### Arrays
---
> Avoid using new Array(). The new keyword can produce some unexpected results.

`const points = new Array(40, 100);`
`result: ,,,,,,,,,,,`
