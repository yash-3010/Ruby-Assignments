## Question 1: Answer
```ruby
class Circle
  def initialize(radius)
    @radius = radius
  end

  def getArea
    Math::PI * @radius**2
  end

  def getCircumference
    2 * Math::PI * @radius
  end
end

circle = Circle.new(5)
puts "Area: #{circle.getArea}"
puts "Circumference: #{circle.getCircumference}"
```
```
Area: 78.53981633974483
Circumference: 31.41592653589793
```
## Question 2: Answer
```ruby
f = 9.312482
s = "$#{'%.2f' % f}"
puts s

```
```
$9.31

```
## Question 3: Answer
```ruby
class Temperature
  def convertFahrenheit(celsius)
    fahrenheit = (celsius * 9/5) + 32
    puts "#{celsius}°C is equal to #{fahrenheit}°F"
  end

  def convertCelsius(fahrenheit)
    celsius = (fahrenheit - 32) * 5/9
    puts "#{fahrenheit}°F is equal to #{celsius}°C"
  end
end

temperature = Temperature.new
temperature.convertFahrenheit(25)
temperature.convertCelsius(98.6)

```
```
25°C is equal to 77°F
98.6°F is equal to 37°C

```