# Value tester

[data/dictionary]

Tests whether the value of  a certain `key` in a dictionary equals to the `value` provided.

If the `key` provided does not exist, the result will be false.

Example A:
1. { "first": 1, "third": 3, "fifth": 5 } @0 received via `dict`
2. "third"@0 received via `key`
3. 3@0 received via `value`
4. `same` sends true@0

Example B:
1. { "first": 1, "third": 3, "fifth": 5 } @0 received via `dict`
2. "seventh"@0 received via `key`
3. 7@0 received via `value`
4. `same` sends false@0

Example C:
1. { "first": 1, "third": 3, "fifth": 5 } @0 received via `dict`
2. "third"@0 received via `key`
3. 7@0 received via `value`
4. `same` sends false@0

### Input ports:

* __dict__: `{string: any}`

    Receives the dictionary to validate the value in.
    
    Example:
    { "first": 1, "third": 3, "fifth": 5 }


* __key__: `string`

    Receives the key in the dictionary to compare the value of.
    
    Example:
    "third"


* __value__: `any`

    Receives the value to test against the specified dictionary key.
    
    Example:
    3

### Output ports:

* __same__: `boolean`

    Sends a value indicating whether the value is the same as the item with the specified key in the provided dictionary.
    
    Example:
    true
    
    

