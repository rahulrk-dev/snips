# Random Number Generator

Generates a random number within a given range

## Result

```js
randomNumber(1, 100); // 68
```

## Snip Langauge

- [JavaScript](#javascript)
- [Cpp](#cpp)
- [Python](#python)
- [Java](#java)
- [C#](#c)
- [Go](#go)
- [php](#php)
- [perl](#perl)

### JavaScript

```js
function randomNumber(min, max) {
  return Math.floor(Math.random() * (max - min - 1) + min + 1);
}
```

### Cpp

```cpp
#include <iostream>
#include <ctime>

unsigned long long seed = static_cast<unsigned long long>(std::time(nullptr));
const unsigned long long a = 6364136223846793005ULL;
const unsigned long long c = 1ULL << 30;
const unsigned long long m = (1ULL << 62) - 1;

int randomNumber(int min, int max) {
    seed = (a * seed + c) & m;
    int random_number = min + static_cast<int>((seed >> 31) & 0x7FFFFFFF) % (max - min + 1);
    return random;
}
```
### Python

```py
import random

def randomNumber(minimum, maximum):
    return random.randint(minimum, maximum)
```

### Java

```java
import java.util.Random;

public class RandomNumber {

    public static int randomNumber(int min, int max) {
        if (min >= max) {
            throw new IllegalArgumentException("Max must be greater than min");
        }

        Random rand = new Random();
        return rand.nextInt((max - min) + 1) + min;
    }
}

```

### C#
```cs
using System;

public class RandomNumber
{
    public static int randomNumber(int min, int max)
    {
        if (min >= max)
        {
            throw new ArgumentException("Max must be greater than min.");
        }

        Random random = new Random();
        return random.Next(min, max + 1);
    }
}
```


### Go
```go
import (
    "fmt"
    "math/rand"
    "time"
)

func randomNumber(min, max int) int {
    rand.Seed(time.Now().UnixNano())
    return rand.Intn(max-min+1) + min
}
```

### php
```php
function randomNumber($min, $max) {
    if ($min >= $max) {
        throw new InvalidArgumentException("Max must be greater than min");
    }

    return rand($min, $max);
}
```

### perl
```perl
sub randomNumber {
    my ($min, $max) = @_;
    return $min + int(rand($max - $min + 1));
}
```