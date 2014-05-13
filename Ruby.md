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
["apple", "banana", "coconut"].each as |fruit| do
	fruit.eat
end

# or even better

["apple", "banana", "coconut"].each do |fruit|
	fruit.eat
end

# on one line

["apple", "banana", "coconut"].each { |fruit| fruit.eat |
```

#### Paste into clipboard

_quite useful when writing text formatting scripts_

```ruby
IO.popen('pbcopy', 'w').puts "Text that will be available to paste"
````

####Parse a JSON directly from the web

```ruby
require 'json'
require 'net/http'

response = Net::HTTP.get_response "example.com", "/json_api_call"
json = JSON.parse response.body
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
