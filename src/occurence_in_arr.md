# count_occurrence
To Count The Occurrence of value in an array

## Result

```Py
   count_occurrences([2,2,4,5,6], target_value) // '2'
```

```JavaScript
   count_occurrences(myArray, targetValue);
```

```C++
   count_ocurrences({4,5,8,6,8,1,8}, 8); // '3'
```

```PHP
   count_ocurrences({4,5,8,6,8,1,8}, 8); // '3'
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

int countOccurrences(const std::vector<int>& arr, int valueToCount) {
    int count = 0;
    for (int element : arr) {
        if (element == valueToCount) {
            count++;
        }
    }
    return count;
}

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
