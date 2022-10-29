# Time Difference
Returns the time difference between input and current time.

## Result
```js
  timeDiff("2022-10-27 17:30:00"); // 1 hour 5 minutes
  // Supposing that the current time is 18:35
```

## Snip Langauge
* [JavaScript](#javascript)

### JavaScript
```js
  const timeDiff = (input = " ") => {
    const [date, time] = input.split(' ')
    const [year, month, day] = date.split('-')
    const [hour, minute, second] = time.split(':')

    const oldDate = new Date(`${year}/${month}/${day} ${hour}:${minute}:${second}`)
    const newDate = new Date()

    const diff = Math.abs(Math.floor(((newDate - oldDate) / 1000)))
    const obj = {}
    
    obj["year"] = Math.floor(diff /( 60 * 60 * 24 * 365))
    let rem = diff - obj["year"] * 60 * 60 * 24 * 365
    
    obj["month"] = Math.floor(rem /( 60 * 60 * 24 * 30))
    rem -= obj["month"] * 60 * 60 * 24 * 30
    
    obj["day"] = Math.floor(rem /( 60 * 60 * 24))
    rem -= obj["day"] * 60 * 60 * 24
    
    obj["hour"] = Math.floor(rem /( 60 * 60))
    rem -= obj["hour"] * 60 * 60
    
    obj["minute"] = Math.floor(rem / 60)
    rem -= obj["minute"] * 60
    
    obj["second"] = rem

    return Object.entries(obj).reduce((acc, curr) => {
      let str = ""
      if(curr[1]){
        str += curr[1] + " " + curr[0]
        if(curr[1] > 1)
          str += "s"
      }
      return (acc ? acc + " " : acc) + str
    }, "") || "0 seconds"
  }
```
