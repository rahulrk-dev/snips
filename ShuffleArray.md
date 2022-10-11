# [Shuffle Array]

## Result
```
  shuffle([1, 2, 3, 4]); ---> [2, 4, 3, 1]
```

## Snip Langauge
* [C++](#c++)

### C++
```c++
  #include <bits/stdc++.h>
using namespace std;
 

void shuffle_array(int arr[], int n)
{
 
    unsigned seed = 0;
    shuffle(arr, arr + n,default_random_engine(seed));
     cout<<"\nThe Shuffled Array is: \n";
    for (int i = 0; i < n; ++i)
        cout << arr[i] << " ";
}
 

int main()
{
 int n;
    cout<<"Enter the Size : ";
 cin>>n;
 int a[n];
 cout<<"Enter "<<n<<" Numbers: ";
 for(int i=0;i<n;i++){
    cin>>a[i];
 }
    shuffle_array(a, n);
    return 0;
}
```
