- [Class](#class)
  - [Instance Method](#instance-method)
  - [Overriding Method](#overriding-method)
  - [Reopening Class](#reopening-class)
- [Instance Variables \& Object State](#instance-variables--object-state)
- [Inheritance](#inheritance)
# Class

- Classes in Ruby are first-class objects—each is an instance of class `Class`.
- Defining a class lets you group behaviors (methods) into convenient bundles
- Classes are named with `Constants`. `Contants` can't be overwritten.
- Classes are special objects: they’re the only kind of object that has the power to spawn new objects (instances)

## Instance Method
- Methods defined inside a class and intended for use by all instances of the class, are called `instance methods`.
## Overriding Method
We can override an instance method, the new version takes precedence.
## Reopening Class
- It’s possible to reopen a class and make additions or changes.

# Instance Variables & Object State
- Information and data associated with a particular object embodies the state of the object.
- We need to be able to do the following:
  - Set, or reset, the state of an object
  - Read back the state
- `Instance variable` enables individual objects to remember state.
  - Instance variable names always start with a single @ (at sign).
  - Instance variables are only visible to the object to which they belong.
  - An instance variable initialized in one method inside a class can be used by any instance method defined within that class.
- Unlike a `local variable`, a `instance variable` retains the value assigned to it even after the method in which it was initialized has terminated. This property of instance vari- ables—their survival across method calls—makes them suitable for maintaining state in an object.

# Inheritance
- Ruby doesn’t allow multiple inheritance;
- Ruby provides modules, which are bundles of programming functionality similar to classes (except that they don’t have instances)
