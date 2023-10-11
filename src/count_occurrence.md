# Count Occurrence
To Count The Occurrence of particular value or element in an array

## Result

```Py
   count_occurrences([2,2,4,5,6], target_value) // '2'
```

## Snip Langauge

- [Python](#python)
- [JavaScript](#javascript)
- [C++](#c++)
- [PHP](#php)

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

### C++

```c++
int countOccurrences(const std::vector<int>& arr, int valueToCount) {
    int count = 0;
    for (int element : arr) {
        if (element == valueToCount) {
            count++;
        }
    }
    return count;
}
```

```php
### PHP

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
