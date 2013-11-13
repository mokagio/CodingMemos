Ruby Memos
==========

####Absolute paths of a script/executable
	
```ruby
# Directory from where the file has been launched
Dir.pwd

# Directory in which the file is located
File.dirname(__FILE__)

# Relative path of the file
File.path(__FILE__)

# Absolute path
File.expand_path(File.path(__FILE__))
```

####Checking if an object is in an array

```ruby
['a', 'b', 'c'].include?('a')	#=> true
```

####Filter all whitespaces in a string

```ruby
"string with some spaces".gsub(/\s/, "_")
```

####Get user input

```ruby
puts "tell me something"
user_input	gets.chomp
```

####Home directory

```ruby
Dir.home
File.expand_path("~")
ENV["HOME"]
```

####Inspect directory recursively

```ruby
Dir["a_dir/**/*.rb"].each{|s| puts `ruby #{s}` }
```

####Loop on array elements

```ruby
["apple", "banana", "coconute"].each as |fruit| do
	fruit.eat
end
```

####Range operator

Inclusive operator `s..e`

```ruby	
(0..3).to_a		#=> [0, 1, 2, 3]
```
	
Exclusive operator `s...e`

```ruby
(0...3).to_a		#=> [0, 1, 2]
```

####Raw text

```ruby	
long_string = <<<EOF
Imagine a really
long string here
EOF
```
	
####Remove carriage return characters

```ruby
"hello\r\n".chomp	#=> "hello"
```
	
[`String.chomp` documentation](http://ruby-doc.org/core-2.0/String.html#method-i-chomp)

####Remove last characters from a string

```ruby
"now is the time"[0…-2]	#=> "now is the ti"
```

####Script arguments

```ruby
ARGV	# => ["arg1", "arg2", "arg3"]
ARGV[0] # => "arg1"
```
	
####Simple read from a file

```ruby
File.read("file.txt")	
```
	
####String search

* You can inspect the content of a string accessing it like a dictionary

```ruby
if (string_to_test['substring'])
	puts "the string contains the substring"
end
```
