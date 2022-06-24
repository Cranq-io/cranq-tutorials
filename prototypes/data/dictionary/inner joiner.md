---
description: [data/dictionary]
---

# Inner joiner

Joins dictionary 'b' to dictionary `a`, by matching the values of `a` to the keys of `b`.

Items from `b` with no matching value in `a` are excluded from the result.

Items from `a` with no matching key in `b` are excluded from the result.

Example:
1. {"first":"first_id", "third":"third_id", "fifth":"fifth_id"}@0 received via `a`
2. {"first_id":1, "second_id":2, "third_id":3}@0 received via `b`
3. `joined` sends {"first": 1,"third": 3}@0

### Input ports:

* __a__: ` {string: string} `

    Receives the dictionary containing the keys to join and the values to join by.
    
    Example:
    {"first":"first_id", "third":"third_id", "fifth":"fifth_id"}


* __b__: ` {string: any} `

    Receives the dictionary containing the values to join and the keys to join by.
    
    Example:
    {"first_id":1, "second_id":2, "third_id":3}

### Output ports:

* __joined__: ` {string: {string: any}[string]} `

    Sends the resulting joined dictionary.
    
    Example:
    {"first": 1,"third": 3}

