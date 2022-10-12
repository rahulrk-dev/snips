# Filter Duplicate Values
Filters Duplicate Values From An Array.

## Result
```js
  filterDups[1,2,2,3,4]; // '[1,2,3,4]'
```

## Snip Langauge
* [JavaScript](#javascript)
* [Python](#python)

### JavaScript
```js
  function removeDuplicate(arr){
    var uniqArr = [...new Set(arr)];
  }
```
### Python
```python
  def removeDuplicate(arr):
    newArr = set(arr)
```
