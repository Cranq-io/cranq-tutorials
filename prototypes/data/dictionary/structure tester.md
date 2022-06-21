---
description: [data/dictionary]
---

# Structure tester

Tests whether a dictionary  has the same structure as another one. Values are ignored.

If `strict` is set, extra properties are not tolerated, the provided dictionaries must have the same keys.

Example A:
1. { "first": 1, "third": 3, "fifth": 5 } @0 received via `dict`
2. { "first": 0, "fifth": 0 }@0 received via `structure`
3. `strict` is set to false
4. `matches` sends true@0

Example B:
1. { "first": 1, "third": 3, "fifth": 5 } @0 received via `dict`
2. { "first": 0, "seventh": 0 }@0 received via `structure`
3. `strict` is set to false
4. `matches` sends false@0

Example C:
1. { "first": 1, "third": 3, "fifth": 5 } @0 received via `dict`
2. { "first": 0, "fifth": 0 }@0 received via `structure`
3. `strict` is set to true
4. `matches` sends false@0


### Input ports:

* __dict__: ` {string: any} `

    Receives the dictionary to test.
    
    Example:
    { "first": 1, "third": 3, "fifth": 5 }


* __structure__: ` {string: any} `

    Receives the dictionary with the reference structure, to which the comparison will be made.
    
    Example:
    { "first": 0, "fifth": 0 }


* __strict__: ` boolean `

    Receives whether extra keys in `dict` are allowed.
    
    Example:
    true

### Output ports:

* __matches__: ` boolean `

    Sends a value indicating whether the dictionary matches the structure.
    
    Example:
    true

