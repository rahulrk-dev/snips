# Capitalize

Capitalizes the first letter of every word in a string.

## Result

```js
capitalize("hello world!"); // 'Hello World!'
```

## Snip Langauge

- [JavaScript](#javascript)
- [Python](#python)
- [Java](#java)

* [Cpp](#cpp)

### JavaScript

```js
function capitaliz(str) {
  return str.replace(/\b[a-z]/g, (char) => char.toUpperCase());
}
```

### Python

```python
  def capitalise(string):
    ls = string.split(" ")

    for i in range (len(ls)):
        ch = ls[i].capitalize()
        print(f"{ch}", end=' ')
```

### Java

```java
  public static String capitalize(String input){
    String words[]=input.split("\\s");
    String capitalizeWord="";
    for(String w:words){
        String first=w.substring(0,1);
        String afterfirst=w.substring(1);
        capitalizeWord+=first.toUpperCase()+afterfirst+" ";
    }
    return capitalizeWord.trim();
  }
```

### Cpp

```cpp
string capitalize(string s)
{
    for (int i = 0; i < s.size(); i++)
    {
        if (i == 0)
        {
            s[i] = toupper(s[i]);
        }
        if (s[i - 1] == ' ')
        {
            s[i] = toupper(s[i]);
        }
    }
    return s;
}
```
