---
description: [data/dictionary]
---

# Keys getter

Gets all keys from the dictionary as an array.


Example A:
1. { "first": 1, "third": 3, "fifth": 5 } @0 received via `dict`
2. `keys` sends  [ "first", "third", "fifth" ]@0

More:
https://github.com/Cranq-io/cranq-tutorials/tree/main/reference/3_querying_data/3_1_getters

### Input ports:

* __dict__: ` {string: any} `

    Receives to dictionary to extract the keys from.
    
    Example:
    { "first": 1, "third": 3, "fifth": 5 } 

### Output ports:

* __keys__: ` string[] `

    Sends the keys of the dictionary as an array.
    
    Example:
    [ "first", "third", "fifth" ]

