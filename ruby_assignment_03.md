# Assignment-03


### Q-1 Answer

In Ruby, an implicit block is a block of code that can be passed to a method without explicitly defining it using the `do..end` or curly braces `{}` syntax. It is a convenient way to pass a block of code to a method, making the code more concise and readable.

To use an implicit block, a method must accept a block as an argument. In Ruby, you can pass a block to a method by using the `yield` keyword inside the method, which will execute the code in the block at a specific point within the method.


```ruby
# Method that accepts a block and iterates over elements in a collection
def iterate_and_print(array)
  puts "Start of iteration"
  array.each do |element|
    yield(element) if block_given?  # Using `yield` to execute the implicit block
  end
  puts "End of iteration"
end

# Calling the method with an implicit block
iterate_and_print([1, 2, 3, 4, 5]) do |num|
  puts "Current number: #{num}"
end
```

---

### Q-2 Answer

```ruby
def execute_proc(proc_argument)
  puts "Start of the method"
  proc_argument.call
  puts "End of the method"
end
my_proc = Proc.new do
  puts "hello "
end
execute_proc(my_proc)
```

Output:

```
Start of the method
hello
End of the method
```
----

### Q-3 Answer 

In Ruby, blocks, procs, and lambdas are all related concepts that allow you to encapsulate and pass around blocks of code. However, there are some important differences between them in terms of syntax, behavior, and usage. Let's differentiate between blocks, procs, and lambdas in Ruby:

1. Blocks:
- A block is a chunk of code enclosed within either `{}` or `do..end`.
- Blocks are not objects and cannot be assigned to variables or passed as arguments directly.
- Blocks are used with methods that can implicitly accept them, like iterators (e.g., `each`, `map`, `times`).
- Blocks are one-time use; they are invoked immediately and cannot be reused.
- They are most commonly used for simple, short-lived code snippets.

2. Procs:
- A Proc is an object that contains a block of code.
- Procs can be assigned to variables, passed as arguments to methods, and returned from methods.
- They provide a way to store and reuse blocks of code.
- Procs do not enforce strict argument arity; if you pass the wrong number of arguments, any missing values will be set to `nil`.


3. Lambdas:
- A lambda is a special type of Proc object that enforces strict argument arity.
- Lambdas are created using the `lambda` keyword or the `->` (stabby lambda) syntax.
- Like Procs, lambdas can be assigned to variables, passed as arguments, and returned from methods.
- Lambdas behave more like methods in terms of argument handling; they require the correct number of arguments to be passed.

---

### Q-4 Answer

```ruby
def palindrome?(str)
  cleaned_str = str.downcase.gsub(/[^a-z0-9]/, '')
  cleaned_str == cleaned_str.reverse
end
```
---

### Q-5 Answer


```ruby
def sum_of_max_and_min(arr)
  return nil if arr.empty?  
  max = arr.max
  min = arr.min
  max + min
end

```
---
