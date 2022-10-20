# Random Number Generator within a given Range
This snippet will generates a number within a given range include extreme values

## Result
```
randomNumber( 1, 100 ); // 68
```

## Snip Langauge
* [JavaScript](#javascript)

### JavaScript
```js

function randomNumber(min, max) { 
    return Math.floor(Math.random() * (max - min-1) + min+1);
} 
  


```
