# [Snippet Name]

[Short description]

## Result

```
  // Show what result the snip will return (E.g. shuffleArray([1, 2, 3, 4]); // [2, 4, 3, 1])
```

## Snip Langauge

- [JavaScript](#javascript)

### JavaScript

```js
// Add your snip here
/**
 * Returns a random number between min (inclusive) and max (exclusive)
 */
function getRandomArbitrary(min, max) {
  return Math.random() * (max - min) + min;
}

/**
 * Returns a random integer between min (inclusive) and max (inclusive).
 * The value is no lower than min (or the next integer greater than min
 * if min isn't an integer) and no greater than max (or the next integer
 * lower than max if max isn't an integer).
 * Using Math.round() will give you a non-uniform distribution!
 */
function getRandomInt(min, max) {
  min = Math.ceil(min);
  max = Math.floor(max);
  return Math.floor(Math.random() * (max - min + 1)) + min;
}
```
