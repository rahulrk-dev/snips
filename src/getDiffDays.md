# GetDiffDays

Get difference count between two dates in days

## Result

```
  getDiffDays("2022-10-01", "2022-10-31"); // 30
```

## Snip Langauge

- [JavaScript](#javascript)

### JavaScript

```js
function getDiffDays(start, end) {
  start = new Date(start);
  end = new Date(end);
  const diff = Math.abs(end - start);
  return Math.ceil(diff / (1000 * 60 * 60 * 24));
}
```
