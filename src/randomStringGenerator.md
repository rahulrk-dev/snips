# Random String Generator
Generate random strings using Javascript

## Result
```
generateString(5); // 50qkj
```

## Snip Langauge
* [JavaScript](#javascript)

### JavaScript
```js
function generateString(length) {
    const characters ='ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789';
    let result = '';
    const charactersLength = characters.length;
    for ( let i = 0; i < length; i++ ) {
        result += characters.charAt(Math.floor(Math.random() * charactersLength));
    }
    return result;
}
```
