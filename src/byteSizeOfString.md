# Size of Byte String
A program to quickly determine the byte size of a string, which is useful for managing data storage and transmission.

## Result
```
 lengthOfbyteString("Hello World")  //11
```

## Snip Langauge
* [Java](#java)
* [Python](#python)
* [JavaScript](#javascript)

### Java
```java
  public static int lengthOfbyteString(String str){
        int sizeInBytes = str.getBytes().length;
        return sizeInBytes;
  }
```

### Python
```py
  def lengthOfByteString(text):
    sizeInBytes = len(text.encode('utf-8'))
    return sizeInBytes
```

### JavaScript
```js
  function lengthOfByteString(str) {
    const encoder = new TextEncoder();
    const bytes = encoder.encode(str);
    const sizeInBytes = bytes.length;
    return sizeInBytes;
}
```
