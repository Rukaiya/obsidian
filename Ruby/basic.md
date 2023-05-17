### Ruby
---
Ruby is an interpreted scripting language which means most of its implementations execute instructions directly and freely, without previously compiling a program into machine-language instructions.
- dynamic
- reflective
-object-oriented
- general-purpose programming language.

It is designed and developed in the mid-1990s by Yukihiro “Matz” Matsumoto in Japan.
### Comments

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
### Variables
- Don’t need to mention its type
### Getting Input
- ‘gets.chomp’ is used to take input from user.
- ‘print’ can be used instead for ‘puts’to print without a new line.
```ruby
print "How old are you ? "
age = gets.chomp
print "How tall are you ?"
height = gets.chomp
puts " You are #{age} year old and your height is #{height} cms"
```
- gets.chomp.to_i is used to get integer input from user.
- gets.chomp.to_f
### Data Types
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