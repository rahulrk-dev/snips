# Capitalize
Capitalizes the first letter of every word in a string.

## Result
```js
  capitalize('hello world!'); // 'Hello World!'
```

## Snip Langauge
* [JavaScript](#javascript)
* [Python](#python)
* [Java](#java)

### JavaScript
```js
  function capitaliz(str) {
    return str.replace(/\b[a-z]/g, char => char.toUpperCase());
  }
```
