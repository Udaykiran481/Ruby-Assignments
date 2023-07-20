# Assignment-05

### Q-1 Answer 

```ruby
/\A[a-zA-Z]\w*@(\w+\.)[a-zA-Z]{1,4}\z/
```
### Q-2 Answer 

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
```
outputs:

```ruby
car = Car.new
car.max_speed   # Output: 100

rickshaw = Rickshaw.new
rickshaw.max_speed   # Output: 25
```
----

### Q-3 Answer

**Modules:**
1. A module is a container for methods, constants, and other module-level definitions.
2. Modules cannot be instantiated or directly used on their own. They are not designed to represent objects.
3. Modules are used as a way to group related methods or constants that can be included in classes.
4. Modules provide a form of multiple inheritance in Ruby, as a class can include multiple modules.
5. To include a module in a class, you use the `include` keyword followed by the module name. This action is called "mixing in" the module.

**Mixins:**
1. A mixin is a way of adding the behavior of a module into a class. It allows a class to "mix in" the methods and constants defined in one or more modules.
2. By including a module in a class, the methods and constants defined in the module become instance methods and can be called on instances of the class.
3. Mixins are a powerful way to achieve code reuse without having to create complex inheritance hierarchies.
4. Multiple mixins can be included in a class, enabling it to incorporate functionalities from multiple sources.
5. It is a common practice in Ruby to use mixins to enhance a class's capabilities with specific functionalities while keeping the class hierarchy simple and manageable.
---
### Q-4 Answer

In Ruby, both private and protected methods are used to control the visibility and accessibility of methods within a class. They serve different purposes and apply to how methods can be called and accessed by other parts of the program. Let's differentiate between private and protected methods in Ruby:

1. Private Methods:
   - Private methods can only be called from within the defining class itself and cannot be called from outside the class, even from its subclasses.
   - They are typically used for internal implementation details that should not be exposed to the outside world.
   - Private methods cannot be accessed using an explicit receiver (i.e., you can't call them using an object instance). Instead, they can only be called without an explicit receiver, which implies they are called on `self`.
   - To define a private method in Ruby, you use the `private` keyword before the method definition.

2. Protected Methods:
   - Protected methods can be called from within the defining class itself and its subclasses. Unlike private methods, they can also be called with an explicit receiver from other instances of the same class.
   - Protected methods are useful when you want to allow certain methods to be accessible only to instances of the same class and its subclasses, ensuring controlled access to specific functionality.
   - To define a protected method in Ruby, you use the `protected` keyword before the method definition.

----
