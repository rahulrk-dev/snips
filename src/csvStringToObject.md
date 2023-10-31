# Convert CSV to array of object
Convert a comma-separated values (CSV) string to array of objects.

## Result
```js
CSV_to_JSON('col1,col2\na,b\nc,d')
// [{'col1': 'a', 'col2': 'b'}, {'col1': 'c', 'col2': 'd'}];
```

## Snip Langauge
* [JavaScript](#javascript)
* [Python](#python)


### JavaScript
```js
const CSV_to_JSON = (data, delimiter = ',') => {
  const titles = data.slice(0, data.indexOf('\n')).split(delimiter);
  return data
    .slice(data.indexOf('\n') + 1)
    .split('\n')
    .map(v => {
      const values = v.split(delimiter);
      return titles.reduce((obj, title, index) => ((obj[title] = values[index]), obj), {});
    });
};
```

### Python
```py
def CSV_to_JSON(data, delimiter=','):
    lines = data.split('\n')
    header = lines[0].split(delimiter)
    result = []

    for line in lines[1:]:
        values = line.split(delimiter)
        if len(values) == len(header):
            row = {header[i]: values[i] for i in range(len(header))}
            result.append(row)

    return result
```

