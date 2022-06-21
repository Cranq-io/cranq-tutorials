# Item getter with default

[data/dictionary]

Retrieves an item's value by its key from a dictionary.
If the item is not found, the specified default value is sent.

Example A:
1. { "first": 1, "third": 3, "fifth": 5 } @0 received via `dict`
2. "first"@0 received via `key`
3. `value` sends 1@0

Example B:
1. 2 assigned to `default`
2. { "first": 1, "third": 3, "fifth": 5 } @0 received via `dict`
3. "second"@0 received via `key`
4. `value` sends 2@0

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



* __default__: _{string: any}[string]_

    Receives the default value to be sent when the requested key is absent.
    
    Must be parameter.
    
    Example:
    2



### Output ports:

* __value__: _{string: any}[string]_

    Sends the value corresponding to the specified key, or, when not found, the specified default value.
    
    Example:
    1



