# Notes from 'Learn Ruby the Hard Way'
Materials URL: https://learnrubythehardway.org/book/preface.html

# The Setup

`irb` - do some calculations

`quit` - get out of `irb`

# Numbers and Math

### `#{3+2}` - insert Ruby computations into text strings

```ruby
puts "Hens #{25 + 30 / 6}”
# Hens 30

puts "Is it true that 3 + 2 < 5 -  7?"
puts 3 + 2 < 5 - 7
# Is it true that 3 + 2 < 5 -  7?
# false
```

# Variables and Name

### `**=`  vs `==`:**

`=` - assigns the value on the right to a variable on the left. 

`==` - tests whether two things have the same value.

### Add values:

```ruby
my_age = 32  not a lie
my_height = 74 #inches
my_weight = 180 #pounds
puts "If I add {my_age}, #{my_height}, and #{my_weight} I get #{my_age + my_height + my_weight}.

# Output:
# If I add 32, 74, and 180 I get 286
```

# Strings and Texts

### Add strings:

```ruby
w = "This is the left side of..."
e = "a string with a right side."
puts w + e
# This is the left side of...a string with a right side.
```

### `'` instead of `"`？

```ruby
types_of_people = 10
x = "There are #{types_of_people} types of people."
binary = "binary"
do_not = "don't"
y = "Those who know #{binary} and those who #{do_not}."
puts x
puts y
puts 'I said:'#{x}'.'
puts "I also said: '#{y}'."

# There are 10 types of people.
# Those who know binary and those who don't.
# I said:
# I also said: 'Those who know binary and those who don't.'.
```

`"` - tells Ruby to replace variables it finds with #{}
`'` - tells Ruby to leave the string alone and ignore any variables inside it

# Printing

### `%{}` - apply the same format to multiple values

```ruby
formatter = "%{first} %{second} %{third} %{fourth}"
puts formatter % {first: 1, second: 2, third: 3, fourth: 4}
puts formatter % {first: "one", second: "two", third: "three", fourth: "four"}
puts formatter % {first: true, second: false, third: true, fourth: false}
puts formatter % {first: formatter, second: formatter, third: formatter, fourth: formatter}

puts formatter % {
first: "I had this thing.",
second: "That you could type up right.",
third: "But it didn't sing.",
fourth: "So I said goodnight."
}

# Output:
# 1 2 3 4
# one two three four
# true false true false
# %{first} %{second} %{third} %{fourth} %{first} %{second} %{third} %{fourth} %{first} %{second} %{third} %{fourth} %{first} %{second} %{third} %{fourth}
# I had this thing. That you could type up right. But it didn't sing. So I said goodnight.
```

### `\n` - **start on a new line**

```ruby
months = "\nJan\nFeb\nMar\nApr\nMay\nJun\nJul\nAug"
puts "Here are the months: #{months}"

# Output:
# Here are the months: 
#	Jan
#	Feb
#	Mar
#	Apr
#	May
#	Jun
#	Jul
#	Aug
```

### use `\` - *escape `“`* and `‘` so Ruby knows to include them in the string

```ruby
puts "I am 6'2\" tall."  # escape double-quote inside string
puts 'I am 6\'2" tall.'  # escape single-quote inside string

# I am 6'2" tall.
# I am 6'2" tall.
```

### `""”` - put as many lines of text as you want until type `"""`again

```ruby
fat_cat= """
I'll do a list:
\t* Cat food
\t* Fishies
\t* Catnip\n\t* Grass
"""
puts fat_cat

# Output:
# I'll do a list:
#				 	* Cat food
#					* Fishies
#					* Catnip
#					* Grass
```
