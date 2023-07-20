# Assignment-01

### Q-1 Answer


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
```
----

### Q-2 Answer

```ruby
f = 9.312482
s = "$" + sprintf("%.2f", f)
puts s # Output: "$9.31"
```
---

### Q-3 Answer

```ruby
class Temperature
  def convertFahrenheit(celsius)
    fahrenheit = (celsius * 9/5) + 32
    puts "#{celsius} Celsius is equal to #{fahrenheit} Fahrenheit."
  end

  def convertCelsius(fahrenheit)
    celsius = (fahrenheit - 32) * 5/9
    puts "#{fahrenheit} Fahrenheit is equal to #{celsius} Celsius."
  end
end

# Example usage:
temp_converter = Temperature.new
temp_converter.convertFahrenheit(30) # Output: 30 Celsius is equal to 86 Fahrenheit.
temp_converter.convertCelsius(75)    # Output: 75 Fahrenheit is equal to 23 Celsius.
```
---
