# Merge Objects
Merges two or more objects.

## Result
```js
merge({ a: [1, 2, 3], b: 1 }, { a: 4, c: "bar" }); // { a: [1,2,3,4], b: 1, c: 'bar' }
```

## Snip Langauge
- [JavaScript](#javascript)
- [Python](#python)
- [Java] (#java)
- [CPP] (#cpp)

### JavaScript
```js
const merge = (...arr) => {
  arr = arr.filter((obj) => typeof obj == "object" && obj !== null);
  const keys = [],
    result = {};
  arr.forEach((obj) => {
    Object.keys(obj).forEach((key) => {
      if (!keys.includes(key)) keys.push(key);
    });
  });

  for (const key of keys) {
    let newValue;
    for (const obj of arr) {
      if (Array.isArray(obj[key])) {
        if (Array.isArray(newValue))
          newValue = newValue.concat(
            obj[key].filter((x) => !newValue.includes(x))
          );
        else newValue = obj[key];
      } else if (Array.isArray(newValue)) newValue.push(obj[key]);
      else if (obj[key]) newValue = obj[key];
    }
    result[key] = newValue;
  }
  return result;
};
```

### Python
```python
def merge(*args):
    args = [obj for obj in args if isinstance(obj, dict)]
    keys, result = set(), {}

    for obj in args:
        keys.update(obj.keys())

    for key in keys:
        new_value = None
        for obj in args:
            if isinstance(obj.get(key), list):
                if isinstance(new_value, list):
                    new_value += [x for x in obj[key] if x not in new_value]
                else:
                    new_value = obj[key]
            elif isinstance(new_value, list):
                new_value.append(obj[key])
            elif obj.get(key):
                new_value = obj[key]
        result[key] = new_value

    return result
```

### Java
```java
public static Map<String, Object> merge(Map<String, Object>... maps) {
    Map<String, Object> result = new HashMap<>();
    Set<String> keys = new HashSet<>();
        
    for (Map<String, Object> map : maps) {
        keys.addAll(map.keySet());
    }

    for (String key : keys) {
        Object newValue = null;
        for (Map<String, Object> map : maps) {
            if (map.containsKey(key)) {
                Object value = map.get(key);
                if (value instanceof List) {
                    if (newValue instanceof List) {
                        ((List) newValue).addAll((List) value);
                    } else {
                        newValue = new ArrayList<>((List) value);
                    }
                } else if (newValue instanceof List) {
                    ((List) newValue).add(value);
                } else {
                    newValue = value;
                }
            }
        }
        result.put(key, newValue);
    }
    return result;
}
```

### CPP
```cpp
using Value = variant<int, string, vector<int>>;
using Dictionary = map<string, Value>;

Dictionary merge(vector<Dictionary> arr) {
    set<string> keys;
    Dictionary result;

    for (const auto& obj : arr) {
        for (const auto& [key, value] : obj) {
            keys.insert(key);
        }
    }

    for (const string& key : keys) {
        Value newValue;
        for (const auto& obj : arr) {
            if (obj.find(key) != obj.end()) {
                if (holds_alternative<vector<int>>(obj.at(key))) {
                    if (holds_alternative<vector<int>>(newValue)) {
                        vector<int>& oldVec = get<vector<int>>(newValue);
                        const vector<int>& newVec = get<vector<int>>(obj.at(key));
                        oldVec.insert(oldVec.end(), newVec.begin(), newVec.end());
                        sort(oldVec.begin(), oldVec.end());
                        oldVec.erase(unique(oldVec.begin(), oldVec.end()), oldVec.end());
                    } else {
                        newValue = obj.at(key);
                    }
                } else if (holds_alternative<vector<int>>(newValue)) {
                    get<vector<int>>(newValue).push_back(get<int>(obj.at(key)));
                } else {
                    newValue = obj.at(key);
                }
            }
        }
        result[key] = newValue;
    }
    return result;
}
```
