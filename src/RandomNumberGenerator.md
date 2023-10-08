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
const unsigned long long a = 6364136223846793005ULL;
const unsigned long long c = 1ULL << 30;
const unsigned long long m = (1ULL << 62) - 1;

int randomNumber(int min, int max) {
    static unsigned long long seed = 0;

    seed = (seed == 0) ? time(NULL) : (a * seed + c) & m;

    int random_number = min + (seed >> 31) % (max - min + 1);
    return random_number;
}
```

### Python

```py
def randomNumber(min_value, max_value, seed=None):
    seed = seed if seed is not None else id(min_value)

    seed = (1664525 * seed + 1013904223) & 0xFFFFFFFF
    random_float = seed / 0xFFFFFFFF

    random_integer = int(min_value + random_float * (max_value - min_value + 1))

    return random_integer
```

### Java

```java
public static int customRandom(int min, int max) {
       long seed = System.nanoTime();
       long m = 1_000_000_000L;
       long a = 6364136223846793005L;
       long c = 1L << 30;

       seed = (a * seed + c) % m;

       int random_number = (int) (min + Math.abs(seed) % (max - min + 1));

       return random_number;
   }
```

### C#

```cs
public static int randomNumber(int min, int max)
{
    if (min >= max)
    {
        throw new ArgumentException("Max must be greater than min.");
    }
    Random random = new Random();
    return random.Next(min, max + 1);
}
```

### Go

```go
func customRandom(min, max int) int {
    const c = 1 << 30
    const m = (1 << 62) - 1
    const a = 6364136223846793005

    staticSeed := uint64(42)
    staticSeed = (staticSeed * a + c) & m

    randomNum := min + int(staticSeed>>31)%(max-min+1)

    return randomNum
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
