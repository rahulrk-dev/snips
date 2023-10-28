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
  public static void lengthOfbyteString(String str){
        int sizeInBytes = str.getBytes().length;
        System.out.println("Size of the string in bytes: " + sizeInBytes);
  }
```

### Python
```py
  def lengthOfByteString(text):
    sizeInBytes = len(text.encode('utf-8'))
    print(f"Size of the string in bytes: {sizeInBytes}")
```

### JavaScript
```js
  function lengthOfByteString(str) {
    const encoder = new TextEncoder();
    const bytes = encoder.encode(str);
    const sizeInBytes = bytes.length;
    console.log(`Size of the string in bytes: ${sizeInBytes}`);
}
```
