---
description: [data/dictionary]
---

# Size getter

Gets the number of items in the dictionary.

Example:
1. { "first": 1, "third": 3, "fifth": 5 }@0 received via `dict`
3. `size` sends 3@0

More:
https://github.com/Cranq-io/cranq-tutorials/tree/main/reference/3_querying_data/3_1_getters

### Input ports:

* __dict__: `{string: any}`

    Receives the dictionary to count the number of items of.
    
    Example:
    { "first": 1, "third": 3, "fifth": 5 }

### Output ports:

* __size__: `number`

    Sends the calculated dictionary size.
    
    Example:
    3

