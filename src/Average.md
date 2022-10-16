# Find Average
To Calculate The Avg of Two or More Numbers

## Result

```js
    Avg([1,2,2,3,3,4]); // '2.5'
```

## Snip Langauge

- [JavaScript](#javascript)
- [Python](#python)

### Python

```python
    def Avg(arr):
        Avg=0
        for i in arr:
            Avg+=i
        return Avg/len(arr)
```

### JavaScript

```js
    function Avg(arr) {
    Avg = 0;
    for (let i = 0; i < arr.length; i++) {
        Avg += arr[i];
    }
    return Avg / arr.length;
    }
```


