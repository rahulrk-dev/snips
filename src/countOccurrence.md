# Count Occurrence

To Count The Occurrence of particular value or element in an array

## Result

```Py
   count_occurrences([2,2,4,5,6], target_value) // '2'
```

## Snip Langauge

- [Python](#python)
- [JavaScript](#javascript)
- [TypeScript](#typescript)
- [PHP](#php)
- [Rust](#rust)
- [CPP](#cpp)
- [Lua](#lua)

### Python

```python
def count_occurrences(arr, value):
    count = 0
    for element in arr:
        if element == value:
            count += 1
    return count
```

### JavaScript

```js
const countOccurrences = (arr, valueToCount) => {
  let count = 0;
  for (const element of arr) {
    if (element === valueToCount) {
      count++;
    }
  }
  return count;
};
```

### TypeScript

```ts
const countOccurrences = <T extends unknown>(
  arr: Array<T>,
  valueToCount: T,
): Number => {
  let count = 0;
  for (const element of arr) {
    if (element === valueToCount) {
      count++;
    }
  }
  return count;
};
```

### PHP

```php
function countOccurrences($arr, $valueToCount) {
    $count = 0;
    foreach ($arr as $element) {
        if ($element == $valueToCount) {
            $count++;
        }
    }
    return $count;
}
```

### Rust

```rust
fn count_occurrences<A: Eq>(arr: Vec<A>, value_to_count: A) -> usize {
    let mut count: usize = 0;
    for element in arr {
        if element == value_to_count {
            count += 1;
        }
    }
    return count;
}
```

### CPP

```cpp
template <typename T>
int count_occurrences(T* arr, T value_to_count) {
  if(sizeof(arr) == 0) return 0;

  int count = 0;
  int size = sizeof(arr) / sizeof(arr[0]);
  for(int i = 0; i < size; i++) {
    if(arr[i] == value_to_count) count += 1;
  }
  return count;
}
```

### Lua

```lua
function count_occurrences(arr, value_to_count) 
  local count = 0
  for _,  element in ipairs(arr) do
    if element == value_to_count then
      count = count + 1
    end
  end
  return count
end
```
