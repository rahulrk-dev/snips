# Bubblesort

Uses bubblesort to sort the array

## Result

```
// bubbleSort([6, 4, 2, 5, 7]);
// [ 2, 4, 5, 6, 7 ]
```

## Snip Langauge

- [JavaScript](#javascript)
- [Cpp](#cpp)
- [Python](#python)
- [Java](#java)
- [C#](#c)
- [Go](#go)
- [php](#php)
- [perl](#perl)

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

### Cpp

```cpp
void bubbleSort(int arr[]) {
    int size = sizeof(arr) / sizeof(arr[0]);
    for (int i = 0; i < size - 1; ++i) {
        bool swapped = false;
        for (int j = 0; j < size - i - 1; ++j) {
            if (arr[j] > arr[j + 1]) {
                int temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
                swapped = true;
            }
        }
        if (!swapped) {
            break;
        }
    }
}
```

### python

```py
def bubbleSort(arr):
    n = len(arr)

    for i in range(n):
        for j in range(0, n-i-1):
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]
```

### java

```java
public class BubbleSort {
    public static void bubbleSort(int[] arr) {
        int n = arr.length;
        boolean swapped;

        do {
            swapped = false;
            for (int i = 1; i < n; i++) {
                if (arr[i - 1] > arr[i]) {
                    // Swap arr[i-1] and arr[i]
                    int temp = arr[i - 1];
                    arr[i - 1] = arr[i];
                    arr[i] = temp;
                    swapped = true;
                }
            }
        } while (swapped);
    }
}
```

### C#

```cs
static void bubbleSort(int[] arr)
    {
       int n = arr.Length;
        bool swapped;
        for (int i = 0; i < n - 1; i++)
        {
            swapped = false;
            for (int j = 0; j < n - i - 1; j++)
            {
                if (arr[j] > arr[j + 1])
                {
                    // Swap arr[j] and arr[j + 1]
                    int temp = arr[j];
                    arr[j] = arr[j + 1];
                    arr[j + 1] = temp;
                    swapped = true;
                }
            }

            // If no two elements were swapped in the inner loop, the array is already sorted
            if (!swapped)
                break;
        }
    }
```

### Go

```go
func bubbleSort(arr []int) {
    n := len(arr)
    swapped := true

    for swapped {
        swapped = false
        for i := 1; i < n; i++ {
            if arr[i-1] > arr[i] {
                arr[i-1], arr[i] = arr[i], arr[i-1]
                swapped = true
            }
        }
    }
}
```

### php

```php
function bubbleSort($array) {
    $n = count($array);
    for ($i = 0; $i < $n - 1; $i++) {
        for ($j = 0; $j < $n - $i - 1; $j++) {
            if ($array[$j] > $array[$j + 1]) {
                $temp = $array[$j];
                $array[$j] = $array[$j + 1];
                $array[$j + 1] = $temp;
            }
        }
    }
    return $array;
}
```

### perl

```perl
sub bubbleSort {
    my @arr = @_;
    my $n = scalar(@arr);

    for my $i (0 .. $n - 1) {
        my $swapped = 0;

        for my $j (0 .. $n - $i - 2) {
            if ($arr[$j] > $arr[$j + 1]) {
                ($arr[$j], $arr[$j + 1]) = ($arr[$j + 1], $arr[$j]);
                $swapped = 1;
            }
        }
        last unless $swapped;
    }

    return @arr;
}
```
