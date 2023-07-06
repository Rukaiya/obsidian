- [Ruby](#ruby)
  - [Comments](#comments)
  - [Variables](#variables)
  - [Getting Input](#getting-input)
  - [Output](#output)
  - [Special Object](#special-object)
  - [Data Types](#data-types)
    - [Hash](#hash)
    - [Array](#array)
  - [Class](#class)

# Ruby

---

Ruby is an interpreted scripting language which means most of its implementations execute instructions directly and freely, without previously compiling a program into machine-language instructions.

- dynamic
- reflective
- object-oriented
- general-purpose programming language.

> Objects are created by classes

> `irb --simple-prompt` canbe used for more simplier view of the prompt

It is designed and developed in the mid-1990s by Yukihiro “Matz” Matsumoto in Japan.

## Comments

- `#` is called the pound character in ruby and it is used to add comments to your code.
- =begin, =end are used for multi-line comments

```ruby
# this is a comment and wont be executed
= begin
this is
a multi line
comment in ruby
= end
```

## Variables

- Local variables start with a lowercase letter or an underscore
- Instance variable can have one in the first position after the at-sign(@)
- Class variables start with two at-signs—for example, @@running_total.
- Global variables are recognizable by their leading dollar sign ( $ )—for example, $population

Type | Ruby convention | Nonconventional
:---:|:---:|:---:
Local | first_name |firstName, \_firstName, \_\_firstName, name1
Instance| @first_name |@First_name, @firstName
Class| @@first_name| @@First_name, @@firstName
Global| $FIRST_NAME| $first_name, $firstName, $name1

## Getting Input

- The `gets` method is used to read a line of text input from the user. When you use gets, it includes the newline character (`\n`) at the end of the input string.
- `gets.chomp` is used to take input from user.

```ruby
print "How old are you ? "
age = gets.chomp
print "How tall are you ?"
height = gets.chomp
puts " You are #{age} year old and your height is #{height} cms"
```

- gets.chomp.to_i is used to get integer input from user.
- gets.chomp.to_f

## Output

- `print` can be used instead for `puts` to print without a new line.
- `p` outputs an inspect string , which may contain extra information about what it’s printing.

## Special Object

- The object `nil` is a kind of “nonobject” indicating the absence of a value or result.
- The keyword `self` refers to the default object. `Self` is a role that different objects play, depending on the execu- tion context. Method calls that don’t specify a calling object are called on `self`.

## Data Types

- Numbers
- Boolean
- Strings
- Hashes
- Arrays
- Symbols

### Hash

```ruby
hsh = colors = { "red": 0xf00, "green": 0x0f0, "blue": 0x00f }
hsh.each do |key, value|
 print key, " is ", value, "\n"
end
```

### Array

```ruby
ary = [ "fred", 10, 3.14, "This is a string", "last element", ]
ary.each do |i|
 puts i
end
```

## Class

---

- Classes in Ruby are first-class objects—each is an instance of class `Class`.
- Defining a class lets you group behaviors (methods) into convenient bundles
- Classes are named with `Constants`. `Contants` can't be overwritten.
