# Different Element in Array
This snip returns different elements between two arrays.

## Result
```
 differentElemArray([1, 2, 3, 4, 5],[3, 4, 5, 6, 7]); //[1, 2]
```

## Snip Langauge
* [JavaScript](#javascript)
* [Python](#python)
* [Java](#java)

### JavaScript
```js
function arrayDiff(array1, array2) {
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
    import java.util.*;

    class JavaExample{
        
    
        public static void diffElem(List list1,List list2){
          Set<Integer> union = new HashSet<Integer>(list1);
          union.addAll(list2);
          Set<Integer> intersection = new HashSet<Integer>(list1);
          intersection.retainAll(list2);
          union.removeAll(intersection);
          for (Integer n : union) {
              System.out.println(n);
            }
        }
        public static void main(String[] args) {
            List<Integer> arr1 = Arrays.asList(1, 2, 3, 4, 4, 5, 6);
             List<Integer> arr2 = Arrays.asList(5, 6, 7, 8);
            diffElem(arr1,arr2);
        }
    }
```
