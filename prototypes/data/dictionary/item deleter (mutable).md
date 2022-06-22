# Item deleter (mutable)

[data/dictionary]

Deletes an item from the dictionary by its key.
Mutates input.

If the item is not found, the original dictionary is forwarded.

Example A:
1. { "first": 1, "third": 3, "fifth": 5 } @0 received via `dict`
2. "first"@0 received via `key`
3. `dict` sends { "third": 3, "fifth": 5 }@0

Example B:
1. { "first": 1, "third": 3, "fifth": 5 } @0 received via `dict`
2. "second"@0 received via `key`
3. `dict` sends{ "first": 1, "third": 3, "fifth": 5 }@0

More:
https://github.com/Cranq-io/cranq-tutorials/tree/main/reference/2_constructing_data/2_1_setters_deleters

### Input ports:

* __dict__: _{string: any}_

    Receives the dictionary to delete the item from.
    
    Example:
    { "first": 1, "third": 3, "fifth": 5 }



* __key__: _string_

    Receives the key corresponding to the value to delete.
    
    Example:
    "third"



### Output ports:

* __dict__: _any_

    Sends the resulting dictionary.
    
    Example:
    { "first": 1, "fifth": 5 }


