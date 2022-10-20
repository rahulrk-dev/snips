# Random String Generator
Generate random strings using Javascript

## Result
```
generateString(5); // 50qkj
```

## Snip Langauge
* [JavaScript](#javascript)
* [Python](#python)
* [Java](#java)
* [Dart](#dart)
* [Bash](#bash)
* [cpp](#Cpp)


### JavaScript
```js
function generateString(length) {
    const characters ='ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789';
    let result = '';
    const charactersLength = characters.length;
    for ( let i = 0; i < length; i++ ) {
        result += characters.charAt(Math.floor(Math.random() * charactersLength));
    }
    return result;
}
```

### Python
```python
def generateString(length):
    characters ='ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789'
    return ''.join(random.choice(characters) for i in range(length))
```

### Java
```java
public static String generateString(int length) {
    String characters = "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789";
    StringBuilder salt = new StringBuilder();
    Random rnd = new Random();
    while (salt.length() < 18) {
        int index = (int) (rnd.nextFloat() * characters.length());
        salt.append(characters.charAt(index));
    }
    String randomStr = salt.toString();
    return randomStr;
}
```

### Dart
```dart
String generateString(int length) {
  const characters = 'ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789';

  Random _rnd = Random();
  return String.fromCharCodes(Iterable.generate(length, (_) => characters.codeUnitAt(_rnd.nextInt(characters.length))));
}
```

### Bash
```bash
generateString(){
    characters=ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789
    stringLength=$(($1))
    result=""
    count=1
    while [ $count -lt $1 ] ; do
        count=$((count+1))
        result="${result}${characters:RANDOM%${#characters}:1}"
    done
    echo $result
}
```

### Cpp
```cpp
using namespace std;
const int ch_MAX = 26;
string RandomString(int ch)
{
    char alpha[ch_MAX] = { 'a', 'b', 'c', 'd', 'e', 'f', 'g',
                          'h', 'i', 'j', 'k', 'l', 'm', 'n',
                          'o', 'p', 'q', 'r', 's', 't', 'u',
                          'v', 'w', 'x', 'y', 'z' };
    string result = "";
    for (int i = 0; i<ch; i++)
        result = result + alpha[rand() % ch_MAX];

    return result;
}
int main()
{
srand(time(NULL));
   int ch = 15;
cout<<RandomString(ch) <<"\n";
   return 0;
}
```
