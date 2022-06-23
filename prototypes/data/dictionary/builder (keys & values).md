---
description: [data/dictionary]
---

# Builder (keys & values)

Builds a dictionary based on matching arrays of keys and values. Items are constructed from the same indices of the input arrays.

If the array received by `keys` contains duplicates,  only the last precedent is taken into effect - the other corresponding values are discarded.

If the item counts of the input arrays differ, the out-of-bounds items are ignored.

Example A:
1. [ "first", "third", "fifth" ]@0 received via `keys`
2. [ 1, 3, 5 ]@0 received via `values`
3. `dict` sends { "first": 1, "third": 3, "fifth": 5 }@0

Example B:
1. [ "first", "third", "fifth" ]@0 received via `keys`
2. [ 1, 3 ]@0 received via `values`
3. `dict` sends { "first": 1, "third": 3 }@0

Example C:
1. [ "first", "first", "fifth" ]@0 received via `keys`
2. [ 1, 3, 5 ]@0 received via `values`
3. `dict` sends { "first": 3,  "fifth": 5 }@0

More:
https://github.com/Cranq-io/cranq-tutorials/tree/main/reference/2_constructing_data/2_2_builders

### Input ports:

* __keys__: `string[]`

    Receives the keys to construct the dictionary from.
    
    Example:
    ["first","third","fifth"]


* __values__: `any[]`

    Receives the values to construct the dictionary from.
    
    Example:
    [1, 3, 5]

### Output ports:

* __dict__: `{string: any[][number]}`

    Sends the resulting dictionary.
    
    Example:
    { "first": 1, "third": 3, "fifth": 5 }

