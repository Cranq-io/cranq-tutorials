---
description: data/dictionary]
---

# Type tester

Tells whether the `data` provided is a dictionary.

Example A:
1. { "first": 1, "third": 3, "fifth": 5 } @0 received via `data`
4. `is dict` sends true@0

Example B:
1. [ "first", "third" ]@0 received via `data`
4. `is dict` sends false@0

### Input ports:

* __data__: `any`

    Receives the data to test for being a dictionary.
    
    Example:
    { "first": 1, "third": 0 }

### Output ports:

* __is dict__: `boolean`

    Sends a value indicating whether the `data` received is a dictionary.
    
    Example:
    true

