# Remove duplicates
Remove Duplicate from an Array

## Result
```
  removeDup([1,2,1,3]); // [1,2,3]
```

## Snip Langauge
* [JavaScript](#javascript)

### JavaScript
```js
const removeDup = (arr) => {
    return Array.from(new Set(arr));
}
```
