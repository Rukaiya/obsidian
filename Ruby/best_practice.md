- [Format Specifier within String Interpolation](#format-specifier-within-string-interpolation)

## Format Specifier within String Interpolation
```ruby
price = 19.99
quantity = 3
total = price * quantity

puts "The total cost is $#{'%.2f' % total}."
# for multiple value
puts "the cost %.2f %.3f" %[price price]
```

