# Bubblesort
Uses bubblesort to sort the array

## Result
```
// bubbleSort([6, 4, 2, 5, 7]);
// [ 2, 4, 5, 6, 7 ]
```

## Snip Langauge

- [JavaScript](#javascript)

### JavaScript

```js
function bubbleSort(A) {
  var i, j;
  var len = A.length;
  var isSwapped = false;
  for (i = 0; i < len; i++) {
    isSwapped = false;
    for (j = 0; j < len; j++) {
      if (A[j] > A[j + 1]) {
        var temp = A[j];
        A[j] = A[j + 1];
        A[j + 1] = temp;
        isSwapped = true;
      }
    }
    if (!isSwapped) {
      break;
    }
  }
  return A;
}
```
