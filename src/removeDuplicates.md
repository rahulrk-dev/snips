# Remove duplicates
Remove Duplicate from an Array

## Result
```
  removeDuplicate([1,2,1,3]); // [1,2,3]
```

## Snip Langauge
* [JavaScript](#javascript)

### JavaScript
```js
const removeDuplicate = (arr) => {
    return Array.from(new Set(arr));
}
```
