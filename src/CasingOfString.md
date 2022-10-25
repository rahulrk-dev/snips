# Casing of a string
Returns the Case of a given string

## Result
```
 CheckCase("Hello World"); // Title Case
```

## Snip Langauge
* [JavaScript](#javascript)

### JavaScript
```js
  function CheckCase(string) {
    var upper = 0;
    var space=0
    
    for (var m = 0; m < string.length; m++) {
        if (string[m] === string[m].toUpperCase()
            && string[m] !== string[m].toLowerCase()) {
            upper++;
      
    
        }
          if(string[m] ===" "){
            space++;
            
        }
    }
    var lower=0;
    for (var m = 0; m < string.length; m++) {
        if (string[m] !== string[m].toUpperCase()
            && string[m] === string[m].toLowerCase()) {
            lower++;
    
        }
    }
    
    var title=0;
    var sentence = string.split(" ");
    
    for(var m = 0; m< sentence.length; m++){
        if(sentence[m][0]===sentence[m][0].toUpperCase()  && sentence[m][0]!==sentence[m][0].toLowerCase()){
           title++;
        }
     }  
    
    if(upper===(string.length-space)){
        return "Uppercase"}
    else if(lower===(string.length-space)){
        return "Lowercase"
    }
    else if(title===sentence.length){
        return "Title Case"
    }
    else
        return "sentence Case"
    }
```
