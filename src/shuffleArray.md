# ShuffleArray 
Randomly shuffles the elements of the given array

## Result
```Javascript
shuffle([3,4,5,6,7,8,9]))
// [9, 7, 6, 5, 4, 8, 3];
```

## Snip Langauge
* [JavaScript](#javascript)

### JavaScript
```js
function shuffle(array) {
  const newArray = [...array]
  const length = newArray.length

  for (let start = 0; start < length; start++) {
    const randomPosition = Math.floor((newArray.length - start) * Math.random())
    const randomItem = newArray.splice(randomPosition, 1)

    newArray.push(...randomItem)
  }
  return newArray
}
```
