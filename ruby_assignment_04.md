# Assignment-04


### Q-1 Answer

```ruby
array = [1, 2, 3, 2, 5, 6, 9, 6, 5, 3, 2, 2, 1, 8, 10, 10, 7]
frequency_hash = Hash.new(0)
array.each { |element| frequency_hash[element] += 1 }
puts frequency_hash
```
output:

```
{1=>2, 2=>4, 3=>2, 5=>2, 6=>2, 9=>1, 8=>1, 10=>2, 7=>1}
```
---
### Q-2 Answer


```ruby
start = 100
end = 200
sum = 0

(start..end).each do |num|
  sum += num
end

puts "The sum of numbers from #{start} to #{end} is: #{sum}"
```
output:
```
The sum of numbers from 100 to 200 is: 15150
```
----

### Q-3 Answer


```ruby
begin
  numerator = 26
  denominator = 0

  result = numerator / denominator

  puts result
rescue ZeroDivisionError => e
  puts "Error: #{e.message}"
end
```
output:

```
Error: divided by 0
```
----

### Q-4 Answer


```ruby
def find_and_replace(str, find_char, replace_char)
  new_str = str.gsub(find_char, replace_char)
  return new_str
end

original_string = "Hello, world!"
find_char = "o"
replace_char = "X"

result_string = find_and_replace(original_string,find_char, replace_char)
puts "Original string: #{original_string}"
puts "After replacement: #{result_string}"
```
output:

```
Original string: Hello, world!
After replacement: HellX, wXrld!
```
---
