## Question 1: Answer
In Ruby, an implicit block is a block of code that can be passed to a method without explicitly using the `do..end` or curly braces `{}` syntax. Implicit blocks are commonly used in Ruby, especially with methods that expect a block as an argument.

Here's an example of using an implicit block with the `each` method:

```ruby
fruits = ["apple", "banana", "orange"]

fruits.each { |fruit| puts "I love #{fruit}" }
```

Output:
```
I love apple
I love banana
I love orange
```

## Question 2: Answer
```ruby
def greet(name, message_proc)
  greeting = message_proc.call(name)
  puts greeting
end

custom_message = Proc.new { |name| "Hello, #{name}! How are you?" }
greet("Yash", custom_message)

```
```
Hello, Yash! How are you?

```

## Question 3: Answer

|                  | Blocks               | Procs              | Lambdas                |
|------------------|----------------------|--------------------|------------------------|
| **Type**         | Anonymous           | Objects            | Objects                |
| **Creation**     | Used with methods   | Using `Proc.new` or `proc` method | Using `lambda` keyword or `->` syntax (stabby lambda) |
| **Arity**        | Less strict         | More strict        | More strict            |
| **Binding**      | Looser binding      | Retains context    | Retains context        |
| **Assignment**   | Cannot be assigned to variables | Can be assigned to variables | Can be assigned to variables |
| **Return**       | Returns from the method it's in | Returns from the Proc | Returns from the Lambda |
| **Syntax**       | `do..end` or `{}`    | `Proc.new { }` or `proc { }` | `lambda { }` or `-> { }` |


## Question 4: Answer
```ruby
def palindrome?(str)
  str == str.reverse
end

puts palindrome?("racecar")

```
```
true
```

## Question 5: Answer
```ruby
def sum_of_max_and_min(arr)
  max_value = arr.max
  min_value = arr.min
  sum = max_value + min_value
  puts "Sum of the maximum and minimum elements: #{sum}"
end

array = [12, 45, 7, 23, 6, 78, 10]
sum_of_max_and_min(array)

```
```
Sum of the maximum and minimum elements: 84
```