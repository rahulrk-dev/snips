# Filter Duplicate Values
Filters Duplicate Values From An Array.

## Result
```js
  removeDuplicate([1,2,2,3,3,4]); // '[1,2,3,4]'
```

## Snip Langauge
* [JavaScript](#javascript)
* [Python](#python)
* [C++](#c)
* [Java](#java)
* [Dart](#dart)
* [Go](#go)

### JavaScript
```js
  function removeDuplicate(arr){
    var uniqArr = [...new Set(arr)];
    return uniqArr;
  }
```
### Python
```python
  def removeDuplicate(arr):
    newArr = set(arr)
    return newArr
```
### C++
```cpp
  int* removeDuplicate(int arr[], int size) {
    unordered_map<int,int> set;
    int *b = new int[10], j=0;
    for(int i=0; i<size; i++){
        if (set[arr[i]]==0){
            set[arr[i]]++;
            b[j++] = arr[i];
        }
    }
    return b;
  }
```
### Java
```java
  public static int[] removeDuplicate(int[] arr) {
      LinkedHashSet<Integer> set = new LinkedHashSet<Integer>();
      for (int i = 0; i < arr.length; i++)
          set.add(a[i]);
      int n = set.size(), i=0; 
      String uniqueArr[] = new String[n]; 
      for (int x: set)
          uniqueArr[i++] = x; 
      return uniqueArr;
  }
```

### Dart
```dart
  List<Int> removeDuplicate(List<int> arr) {
    List<int> uniqueList; 
    uniqueList = arr.toSet().toList();
    return uniqueList;
  }
```

### Go
```go
  func removeDuplicates(values []int) []int {
    var uniques []int
    seenValues := map[int]struct{}{}

    for _, v := range values {
      if _, seen := seenValues[v]; !seen {
        unique = append(unique, v)
        seenValues[v] = struct{}{}
      }
    }

    return uniques
  }
```
