# Average of n numbers

To calculate the average of n numbers

## Result

```js
    Average of n numbers([1,2,2,3,3,4]); // '2.5'
```

## Snip Langauge

- [Python](#python)
- [JavaScript](#javascript)
- [Cpp / C](#Cpp/C)
- [java](#java)

### Python

```python
  def Average(arr):
    Avg=0
    for i in arr:
        Avg+=i
    return Avg/len(arr)
```

### JavaScript

```js
function Average(arr) {
  Avg = 0;
  for (let i = 0; i < arr.length; i++) {
    Avg += arr[i];
  }
  return Avg / arr.length;
}
```

### Cpp/C

```cpp
    float Average(int *arr, int len)
    {
        float Average = 0;
        for (int i = 0; i < len; i++)
        {
            Average = Average + arr[i];
        }
        Average = Average / len;
        return Average;
    }
```
### Java

```cpp
    public static float FindAverage(int arr[]){
        float avg=0;
        for (int i = 0; i < arr.length; i++) {
            avg=avg+arr[i];
        }
        avg =avg /arr.length ;
        return avg;
    }
```

