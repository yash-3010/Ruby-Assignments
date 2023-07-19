## Question 1: Answer
```ruby
def print_odd_numbers(n)
  if n < 1 || n > 100
    puts "Please enter a value of 'n' between 1 and 100."
    return
  end

  odd_numbers = []
  current_number = 1

  while odd_numbers.length < n
    odd_numbers << current_number if current_number.odd?
    current_number += 1
  end

  puts "The first #{n} odd numbers are: #{odd_numbers.join(', ')}"
end

print_odd_numbers(10)

```
```
The first 10 odd numbers are: 1, 3, 5, 7, 9, 11, 13, 15, 17, 19

```
## Question 2: Answer
```ruby
def map_to_day(arr)
  days = {
    1 => "monday",
    2 => "tuesday",
    3 => "wednesday",
    4 => "thursday",
    5 => "friday",
    6 => "saturday",
    7 => "sunday"
  }

  result = arr.map { |num| "#{num}-#{days[num]}" }
  puts result.join(', ')
end


arr = [1, 5, 7, 4, 2, 6, 1, 4, 2, 7]
map_to_day(arr)

```
```
1-monday, 5-friday, 7-sunday, 4-thursday, 2-tuesday, 6-saturday, 1-monday, 4-thursday, 2-tuesday, 7-sunday

```
## Question 3: Answer
```ruby
def selection_sort(arr)
  n = arr.length
  (0...n).each do |i|
    min_index = i
    (i + 1...n).each do |j|
      min_index = j if arr[j] < arr[min_index]
    end
    arr[i], arr[min_index] = arr[min_index], arr[i] if min_index != i
  end
  arr
end


arr = [12, 15, 9, 4, 30, 3, 7]
sorted_arr = selection_sort(arr)
puts sorted_arr.join(', ')

```
```
3, 4, 7, 9, 12, 15, 30

```
