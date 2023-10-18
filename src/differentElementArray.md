# Different Element in Array
This snip returns different elements between two arrays.

## Result
```
 differentElemArray([1, 2, 3, 4, 5],[3, 4, 5, 6, 7]); //[1, 2, 6, 7]
```

## Snip Langauge
* [JavaScript](#javascript)
* [Python](#python)
* [Java](#java)

### JavaScript
```js
function differentElemArray(array1, array2) {
    const diff = array1.filter((element) => !array2.includes(element)); 
    return diff;
}

```
### Python
```python
def differentElemArray(arr1, arr2):
  res = list(set(arr1) - set(arr2))
  return res
```

### Java
```java
public static Integer[] differentElemArray(int[] arr1, int[] arr2){
    Integer[] res = new Integer[Math.max(arr1.length, arr2.length)]; 
    for (int i : arr1) {
        boolean contains = false;
        for (int j : arr2) {
            if (i == j) {
              contains = true;
              break;
              }
         }
         if (!contains){
            res[x] = i;
            x+=1;
         }
    }
    for (int i : arr2) {
        boolean contains = false;
            for (int j : arr1) {
                if (i == j) {
                    contains = true;
                    break;
                }
            }
        if (!contains){
            res[x] = i;
            x+=1;
        }
    }
    return res;
}
```
