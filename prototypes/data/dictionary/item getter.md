# Item getter

[data/dictionary]

Retrieves an item's value by its key from a dictionary.
If the item is not found, the inputs are sent via `not found`.

Example A:
1. { "first": 1, "third": 3, "fifth": 5 } @0 received via `dict`
2. "first"@0 received via `key`
3. `value` sends 1@0

Example B:
1. { "first": 1, "third": 3, "fifth": 5 } @0 received via `dict`
2. "second"@0 received via `key`
3. `not found` sends { "dict":  { "first": 1, "third": 3, "fifth": 5 }, "key": "second" }@0

More:
https://github.com/Cranq-io/cranq-tutorials/tree/main/reference/3_querying_data/3_1_getters

### Input ports:

* __dict__: _{string: any}_

    Receives the dictionary to get the value from.
    
    Example:
    { "first": 1, "third": 3, "fifth": 5 }



* __key__: _string_

    Receives the key corresponding to the value to get.
    
    Example:
    "third"



### Output ports:

* __value__: _{string: any}[string]_

    If found, sends the value corresponding to the specified key.
    
    Example:
    1



* __not found__: _{"dict" :{string: any}, "key" :string}_

    Sends the input values, when the specified key is not found in the dictionary.
    
    Example:
    { "dict":  { "first": 1, "third": 3, "fifth": 5 }, "key": "second" }



