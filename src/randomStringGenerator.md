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
import random

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
import 'dart:math';

String generateString(int length) {
  const characters = 'ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789';

  Random _rnd = Random();
  return String.fromCharCodes(Iterable.generate(length, (_) => characters.codeUnitAt(_rnd.nextInt(characters.length))));
}
```

### Bash
```bash
#!/bin/bash

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

# Example to execute
echo $(generateString 10) #XqyIxIUhW
```