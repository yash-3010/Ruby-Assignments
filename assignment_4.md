## Question 1: Answer
```ruby
arr = [1, 2, 3, 2, 5, 6, 9, 6, 5, 3, 2, 2, 1, 8, 10, 10, 7]

frequency_hash = Hash.new(0)

arr.each do |element|
  frequency_hash[element] += 1
end

puts frequency_hash

```
```
{1=>2, 2=>4, 3=>2, 5=>2, 6=>2, 9=>1, 8=>1, 10=>2, 7=>1}

```
## Question 2: Answer
```ruby
start_num = 100
end_num = 200

sum = 0

(start_num..end_num).each do |num|
  sum += num
end

puts "The sum of numbers from #{start_num} to #{end_num} is: #{sum}"

```
```
The sum of numbers from 100 to 200 is: 15150

```
## Question 3: Answer
```ruby
def divide(a, b)
  if b == 0
    raise ZeroDivisionError.new("Division by zero is not allowed.")
  else
    a / b
  end
end

begin
  result = divide(10, 0)
  puts "Result: #{result}"
rescue ZeroDivisionError => e
  puts "Error: #{e.message}"
end
begin
  result = divide(100, 2)
  puts "Result: #{result}"
rescue ZeroDivisionError => e
  puts "Error: #{e.message}"
end

```
```
Error: Division by zero is not allowed.
Result: 50
```
## Question 4: Answer
```ruby
def find_and_replace(input_string, target_char, replacement_char)
  new_string = input_string.gsub(target_char, replacement_char)
  puts "Original String: #{input_string}"
  puts "Modified String: #{new_string}"
end

input_string = "I love Ruby."
target_char = "o"
replacement_char = "i"

find_and_replace(input_string, target_char, replacement_char)

```
```
Original String: I love Ruby.
Modified String: I live Ruby.
```