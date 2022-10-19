# [Random Number Generator within a given Range]
[Its an snippet for a  function random number generator which whill generates a number within a given range]

## Result
```
  // Add final result
```

## Snip Langauge
* [JavaScript](#javascript)

### JavaScript
```js

function randomNumber(min, max) { 
    return Math.random() * (max - min) + min;
} 
  
document.write("Random Number between 1 and 100: ") 
document.write( randomNumber(1, 100) ); 

```
