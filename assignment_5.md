## Question 1: Answer
```ruby
def valid_email?(email)
  email_regex = /^[A-Za-z]\w*@\w+\.[A-Za-z]{1,4}$/
  !!(email =~ email_regex)
end

puts valid_email?('yashbarman@kreeti.com')

```
```
true
```
## Question 2: Answer
```ruby
class Vehicle
  def initialize
    puts "I am a vehicle"
  end

  def max_speed
    puts "10"
  end
end

class Car < Vehicle
  def max_speed
    puts "100"
  end
end

class Rickshaw < Vehicle
  def max_speed
    puts "25"
  end
end


car = Car.new
car.max_speed

rickshaw = Rickshaw.new
rickshaw.max_speed

```
```
I am a vehicle
100
I am a vehicle
25
```
## Question 2: Answer
```ruby
class Vehicle
  def initialize
    puts "I am a vehicle"
  end

  def max_speed
    puts "10"
  end
end

class Car < Vehicle
  def max_speed
    puts "100"
  end
end

class Rickshaw < Vehicle
  def max_speed
    puts "25"
  end
end


car = Car.new
car.max_speed

rickshaw = Rickshaw.new
rickshaw.max_speed

```
```
I am a vehicle
100
I am a vehicle
25
```
## Question 3: Answer
| **Module**                                            | **Mixin**                                                              |
|-------------------------------------------------------|------------------------------------------------------------------------|
| Modules are containers for methods, constants, etc.  | Mixins are modules that are included in classes to add functionalities. |
| Modules cannot be instantiated directly.             | Mixins are not instantiated separately; they are included in classes.  |
| Modules cannot have instances or state.              | Mixins can add behavior and state to classes when included.            |
| Modules promote code organization and reusability.   | Mixins enable class composition and code sharing.                      |
| Modules use the `module` keyword in their definition.| Mixins are achieved by including modules using the `include` keyword.  |
| Modules can be used as namespaces to avoid conflicts.| Mixins help avoid duplicating code in multiple classes.                |
| Modules cannot be inherited; they don't have a hierarchy.  | Mixins are used in multiple classes, allowing for multiple inheritance. |

## Question 4: Answer
| **Private Methods**                                        | **Protected Methods**                                                |
|------------------------------------------------------------|----------------------------------------------------------------------|
| Private methods can only be called from within the class where they are defined. | Protected methods can be called from within the defining class and its subclasses.|
| Private methods cannot be accessed from outside the class, not even from its subclasses. | Protected methods can be accessed by the class itself and its subclasses. They cannot be called by instances of the class. |
| Private methods are generally used for internal implementation details of the class. | Protected methods are typically used when a class wants to share certain behaviors with its subclasses without exposing them publicly. |
| Private methods are declared using the `private` keyword in Ruby. | Protected methods are declared using the `protected` keyword in Ruby. |
| An attempt to call a private method from outside the class results in a `NoMethodError`. | An attempt to call a protected method from outside the class or its subclasses also results in a `NoMethodError`. |
| Private methods cannot be overridden by subclasses. | Protected methods can be overridden by subclasses, but they still remain protected. |
| Private methods are not inherited by subclasses. | Protected methods are inherited by subclasses and maintain their protected status in the subclass. |