# Casing of a string
Returns the Case of a given string

## Result
```
 CheckCase("Hello World"); // Title Case
```

## Snip Langauge
* [JavaScript](#javascript)
* [Go](#go)
* [Python](#python)

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

### Go
```go
func CheckCase(input string) string {
	upper := 0
	lower := 0
	title := 0

	for _, char := range input {
		if unicode.IsUpper(char) {
			upper++
		} else if unicode.IsLower(char) {
			lower++
		}
	}

	words := strings.Fields(input)
	for _, word := range words {
		if unicode.IsUpper([]rune(word)[0]) {
			title++
		}
	}

	if upper == len(input) {
		return "Uppercase"
	} else if lower == len(input) {
		return "Lowercase"
	} else if title == len(words) {
		return "Title Case"
	} else {
		return "Sentence Case"
	}
}
```

### Python
```python

def CheckCase(string):
    upper = 0
    lower = 0
    title = 0
    
    for char in string:
        if char.isupper():
            upper += 1
        elif char.islower():
            lower += 1

    words = string.split()
    for word in words:
        if word[0].isupper():
            title += 1

    if upper == len(string):
        return "Uppercase"
    elif lower == len(string):
        return "Lowercase"
    elif title == len(words):
        return "Title Case"
    else:
        return "Sentence Case"
```
