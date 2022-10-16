# Transpose of 2-D Array 
Returns Transpose of given Two Dimensional Array

## Result
```
TransposeArray([[1,2,3] ,[4,5,6] ,[7,8,9]]); // [[1,4,7] ,[2,5,8] ,[3,6,9]]
```

## Snip Langauge
* [C++](#C++)
* [Python](#python)
* [Java](#java)
* [JavaScript](#javascript)
* [Bash](#bash)

### C++
```cpp
int** transposeArray(int (&A)[rows][cols]){
    int m = sizeof(A) / sizeof(A[0]);
    int n = sizeof(A[0]) / sizeof(int);
    int **ptr = new int*[m];
    for(int i=0; i<m; i++){
        ptr[i]=new int[n];
        for(int j=0; j<n; j++){
            ptr[i][j] = A[j][i];
        }
    }
    return ptr;
}
```

### Python
```python
def transposeList(A):
    B=[]
    for i in range(len(A[0])):
        temp=[]
        for j in range(len(A)):
            temp.append(A[j][i])
        B.append(temp)
    return B

```

### Java
```java
public int[][] transposeArray(int[][] A)) {
    int[][] B = new int[A.length][A[0].length];
    for (int i=0; i<A.length; i++) 
    {
        for(int j=0; j<A[0].length; j++) 
        {
            B[i][j]=A[j][i];
        }
    }
    return B;
}

```


### JavaScript
```js
function transposeArray(A) {
    var B = Array(N);
    for(i=0; i<N; i++){
        B[i] = Array(N).fill(0);
    }
    for (i = 0; i < A.length; i++)
            for (j = 0; j < A[0].length; j++)
                B[i][j] = A[j][i];
    return B;
}
```

### Bash
```bash
transposeArray(){
    A=(1 2 3 4 5 6 7 8 9)
    rows=3
    cols=3    
    for((i=0; i<rows; i++))
    do
        for((j=i+1; j<cols; j++))
        do
            index1=$((rows*i + j))
            index2=$((rows*j + i))
            temp=${A[index1]}
            A[index1]=${A[index2]}
            A[index2]=$temp
        done
    done        
}
```
