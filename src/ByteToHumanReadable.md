# Different Element in Array
This snippet converts a given number of bytes into a human-readable string format such as KB, MB, GB, etc.

## Result
```
bytesToHumanReadable(123456789); //117.74 MB
```

## Snip Langauge
* [Python](#python)
* [CPP](#cpp)
* [JavaScript](#javascript)
* [Java](#java)

### Python
```python
def bytesToHumanReadable(n):
    for unit in ['B', 'KB', 'MB', 'GB', 'TB']:
        if n < 1024:
            return f"{n:.2f} {unit}"
        n /= 1024
```

### CPP
```cpp
std::string bytesToHumanReadable(double n) {
    std::vector<std::string> units = {"B", "KB", "MB", "GB", "TB"};
    int i = 0;
    while (n >= 1024 && i < units.size() - 1) {
        n /= 1024;
        ++i;
    }
    std::ostringstream stream;
    stream << std::fixed << std::setprecision(2) << n << " " << units[i];
    return stream.str();
}
```

### JavaScript
```js
function bytesToHumanReadable(n) {
    const units = ['B', 'KB', 'MB', 'GB', 'TB'];
    let i = 0;
    while (n >= 1024 && i < units.length - 1) {
        n /= 1024;
        i++;
    }
    return `${n.toFixed(2)} ${units[i]}`;
}
```

### Java
```java
public static String bytesToHumanReadable(long n) {
    String[] units = {"B", "KB", "MB", "GB", "TB"};
    int i = 0;
    while (n >= 1024 && i < units.length - 1) {
        n /= 1024;
        i++;
    }
    return String.format("%.2f %s", (double)n, units[i]);
}
```
