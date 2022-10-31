# Merge Objects
Merges two or more objects.

## Result
```js
  merge({ a: [1,2,3], b: 1 }, { a: 4, c: 'bar' }); // { a: [1,2,3,4], b: 1, c: 'bar' }
```

## Snip Langauge
* [JavaScript](#javascript)

### JavaScript
```js
  const merge = (...arr) => {
    arr = arr.filter(obj => typeof obj == 'object' && obj !== null)
    const keys = [], result = {}
    arr.forEach(obj => {
      Object.keys(obj).forEach(key => {
        if(!keys.includes(key)) keys.push(key)
      })
    })

    for(const key of keys){
      let newValue
      for(const obj of arr){
        if(Array.isArray(obj[key])){
          if(Array.isArray(newValue)) 
            newValue = newValue.concat(obj[key].filter(x => !newValue.includes(x)))
          else newValue = obj[key]
        }
        else if(Array.isArray(newValue)) newValue.push(obj[key])
        else if(obj[key]) newValue = obj[key]
      }
      result[key] = newValue
    }
    return result
  }
```
