# Filter Duplicate Values
Filters Duplicate Values From An Array.

## Result
```js
  removeDuplicate([1,2,2,3,3,4]); // '[1,2,3,4]'
```

## Snip Langauge
* [JavaScript](#javascript)
* [Python](#python)

### JavaScript
```js
  function removeDuplicate(arr){
    var uniqArr = [...new Set(arr)];
    return uniqArr;
  }
```
### Python
```python
  def removeDuplicate(arr):
    newArr = set(arr)
    return newArr
```
