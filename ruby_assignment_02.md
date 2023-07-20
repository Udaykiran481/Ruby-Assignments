# Assignment-02

### Q-1 Answer

```ruby
def print_odd_numbers(n)
  if n < 1 || n > 100
    puts "n should be between 1 and 100."
    return
  end

  odd_numbers = (1..(2 * n)).select { |num| num.odd? }.first(n)
  puts "First #{n} odd numbers are: #{odd_numbers.join(', ')}"
end

print_odd_numbers(10)
```

----

### Q-2 Answer

```ruby
def print_days(arr)
  day_map = {
    1 => "monday",
    2 => "tuesday",
    3 => "wednesday",
    4 => "thursday",
    5 => "friday",
    6 => "saturday",
    7 => "sunday"
  }

  day_names = arr.map { |num| "#{num}-#{day_map[num]}" }
  puts day_names.join(", ")
end

arr = [1, 5, 7, 4, 2, 6, 1, 4, 2, 7]
print_days(arr)
```
output:

```
1-monday, 5-friday, 7-sunday, 4-thursday, 2-tuesday, 6-saturday, 1-monday, 4-thursday, 2-tuesday, 7-sunday
```
---

### Q-3 Answer

```ruby
def selection_sort(arr)
  n = arr.length
  for i in 0..n-2
    min_index = i
    for j in i+1..n-1
      min_index = j if arr[j] < arr[min_index]
    end
    arr[i], arr[min_index] = arr[min_index], arr[i] if i != min_index
  end
  arr
end

arr = [12, 15, 9, 4, 30, 3, 7]
sorted_arr = selection_sort(arr)
puts sorted_arr.inspect
```

Output:

```
[3, 4, 7, 9, 12, 15, 30]
```
----
