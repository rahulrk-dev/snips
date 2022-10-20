# Random Number Generator
Generates a random number within a given range

## Result
```js
  randomNumber(1, 100); // 68
```

## Snip Langauge
* [JavaScript](#javascript)

### JavaScript
```js
  function randomNumber(min, max) { 
      return Math.floor(Math.random() * (max - min-1) + min+1);
  } 
```
