# GetDiffDays
Get difference count between two dates in days

## Result
```
  getDiffDays("2022-10-01", "2022-10-31"); // 30
```

## Snip Langauge
* [JavaScript](#javascript)
* [Python](#python)
* [Go](#go)

### JavaScript
```js
  function getDiffDays(start, end) {
    start = new Date(start);
    end = new Date(end);
    const diff = Math.abs(end - start);
    return Math.ceil(diff / (1000 * 60 * 60 * 24));
  }
```

### Python

```python
  from datetime import datetime

  def getDiffDays(start, end):
      format = '%Y-%m-%d'
      start = datetime.strptime(start, format).date()
      end = datetime.strptime(end, format).date()
      return(end - start).days
```

### Go

```go
func getDiffDays(start, end string) int {
	startTime, _ := time.Parse("2006-01-02", start)
	endTime, _ := time.Parse("2006-01-02", end)

	duration := endTime.Sub(startTime)
	days := int(duration.Hours() / 24)

	return days
}
```
