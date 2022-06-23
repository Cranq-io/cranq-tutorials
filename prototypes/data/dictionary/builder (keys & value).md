# Builder (keys & value)

[data/dictionary]

Builds a dictionary based on an array of keys and a single value for all items.

Example:
1. [ "first", "third", "fifth" ]@0 received via `keys`
1. 1@0 received via `value`
2. `dict` sends { "first": 1, "third": 1, "fifth": 1 }@0

More:
https://github.com/Cranq-io/cranq-tutorials/tree/main/reference/2_constructing_data/2_2_builders

### Input ports:

* __keys__: `string[]`

    Receives the keys to construct the dictionary from.
    
    Example:
    ["first","third","fifth"]


* __value__: `any`

    Receives the value to assign to all items.
    
    Example:
    1

### Output ports:

* __dict__: `{string: any}`

    Sends the resulting dictionary.
    
    Example:
    { "first": 1, "third": 1, "fifth": 1 }

