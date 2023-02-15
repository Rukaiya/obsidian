## Array Methods
Method| Syntax | Description
:--- | --- | :---
append() | list.append(element) | Adds an element at the end of the list
clear() | list.clear() | Removes all the elements from the list
copy() | list.copy() | Returns a copy of the list
count() | list.count(value) | Returns the number of elements with the specified value
extend() | list.extend(iterable) | Add the elements of a list (or any iterable), to the end of the current list. More suitable for Multiple element than `append()`.
index() | list.index(element) | Returns the index of the first element with the specified value
insert() | list.insert(pos, element) | Adds an element at the specified position
pop() | list.pop(pos) | Removes the element at the specified position
remove() | list.remove(element) | Removes the first item with the specified value
reverse() | list.reverse() | Reverses the order of the list
sort() | list.sort(reverse=True|False, key=myFunc) | Sorts the list

## Set
---
Method| Syntax | Description
:--- | --- | :--- 
add() | set.add(value) | Adds an element to the set
clear() | set.clear() | Removes all the elements from the set
copy() | set.copy() | Returns a copy of the set
difference() | set.difference(set) | Returns a new set containing the difference between two or more sets
difference_update() | set.difference_update(set) | Removes the items in this set that are also included in another, specified set
discard() | set.discard(value) | Remove the specified item
intersection() | set.intersection(set) | Returns a new set, that is the intersection of two other sets
intersection_update() | set.intersection_update(set) | Removes the items in this set that are not present in other, specified set(s)
isdisjoint() | set.isdisjoint(set) | Returns whether two sets have a intersection or not
issubset() | set.issubset(set) | Returns whether another set contains this set or not
issuperset() | set.issuperset(set) | Returns whether this set contains another set or not
pop() | set.pop() | Removes an element from the set. The `pop()` method returns removed item.
remove() | set.remove(item) | Removes the specified element. the `remove()` method will raise an error if the specified item does not exist
symmetric_difference() | set.symmetric_difference(set) | Returns a new set with the symmetric differences of two sets
symmetric_difference_update() | set.symmetric_difference_update(set) | inserts the symmetric differences from this set and another
union() | set.union(set1, set2...) | Return a set containing the union of sets
update() | set.update(set) | Update the set with the union of this set and others

## Dictionary Methods
---
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

## Tuple Method
---
Method| Syntax | Description
:--- | --- | :--- 
count()| tuple.count(value) | Returns the number of times a specified value occurs in a tuple
index()| tuple.index(value) | Searches the tuple for a specified value and returns the position of where it was found

## [Format Method](https://www.w3schools.com/python/ref_string_format.asp)
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

##  String Method
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
## strftime() Methods
---

- strftime() formates date objects into readable strings.

Directive| Description | Example
:--- | --- | :---
Directive | Description | Example
%a | Weekday, short version | Wed	
%A | Weekday, full version | Wednesday	
%w | Weekday as a number 0-6, 0 is Sunday | 3	
%d | Day of month 01-31	31	
%b | Month name, short version | Dec	
%B | Month name, full version | December	
%m | Month as a number 01-12 | 12	
%y | Year, short version, without century | 18	
%Y | Year, full version | 2018	
%H | Hour 00-23 | 17	
%I | Hour 00-12 | 05	
%p | AM/PM | PM	
%M | Minute 00-59 | 41	
%S | Second 00-59 | 08	
%f | Microsecond 000000-999999 | 548513	
%z | UTC offset | +0100	
%Z | Timezone | CST	
%j | Day number of year 001-366 | 365	
%U | Week number of year, Sunday as the first day of week, 00-53 | 52	
%W | Week number of year, Monday as the first day of week, 00-53 | 52	
%c | Local version of date and time | Mon Dec 31 17:41:00 2018	
%C | Century | 20	
%x | Local version of date | 12/31/18	
%X | Local version of time | 17:41:00	
%% | A % character | %	
%G | ISO 8601 year | 2018	
%u | ISO 8601 weekday (1-7) | 1	
%V | ISO 8601 weeknumber (01-53) | 01