# [random integer]

- generate random integer in given range.

## Result

```js
  -returns any random integer between min and max range ex(1,676,999...etc).
```

### JavaScript

```js
let max = 9999999;
let min = -9999999;

function getRandomInt() {
  return Math.floor(Math.random() * (max - min + 1)) + min;
}
```
