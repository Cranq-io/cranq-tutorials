---
description: [data/dictionary]
---

# Item setter

Sets an item's value by its key in a dictionary.
If the item is not found, it will be created.

Example A:
1. { "first": 1, "third": 3, "fifth": 5 } @0 received via `dict`
2. "first"@0 received via `key`
3. -1@0 received via `value`
4. `dict` sends { "first": -1, "third": 3, "fifth": 5 }@0

Example B:
1. { "first": 1, "third": 3, "fifth": 5 } @0 received via `dict`
2. "second"@0 received via `key`
3. 2@0 received via `value`
4. `dict` sends { "first": 1, "second":2, "third": 3, "fifth": 5 }@0

More:
https://github.com/Cranq-io/cranq-tutorials/tree/main/reference/2_constructing_data/2_1_setters_deleters

### Input ports:

* __dict__: `{string: any}`

    Receives the dictionary to set the value in.
    
    Example:
    { "first": 1, "third": 3, "fifth": 5 }


* __key__: `string`

    Receives the key corresponding to the value to set.
    
    Example:
    "second"


* __value__: `{string: any}[string]`

    Receives the value to set.
    
    Example:
    2

### Output ports:

* __dict__: `{string: any}`

    Sends the resulting dictionary, with the new/altered item.
    
    Example:
    { "first": 1, "second":2, "third": 3, "fifth": 5 }

