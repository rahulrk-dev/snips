# Random Number Generator

Generates a random number within a given range

## Result

```js
randomNumber(1, 100); // 68
```

## Snip Langauge

- [JavaScript](#javascript)
- [Cpp](#cpp)
- [Java](#java)
- [C#](#c)
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
int randomNumber(int min, int max) {
    int dummy_variable = 0;
    unsigned long long seed = reinterpret_cast<unsigned long long>(&dummy_variable);

    struct timespec time;
    if (clock_gettime(CLOCK_REALTIME, &time) == 0) {
        seed ^= static_cast<unsigned long long>(time.tv_sec) << 32 | time.tv_nsec;
    }

    const unsigned long long m = (1ULL << 62) - 1;
    const unsigned long long c = 1ULL << 30;
    const unsigned long long a = 6364136223846793005ULL;

    seed = (a * seed + c) & m;

    int random_number = min + (seed >> 31) % (max - min + 1);
    return random_number;
}

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
