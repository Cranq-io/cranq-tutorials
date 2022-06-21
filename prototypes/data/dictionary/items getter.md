# Items getter

[data/dictionary]

Retrieves multiple items' values from the dictionary by their keys, in the order of the keys provided.
If any of the items are not found in the dictionary, a 'null' value will be sent in its place.

Example A:
1. { "first": 1, "third": 3, "fifth": 5 } @0 received via `dict`
2. [ "first", "third" ]@0 received via `key`
3. `values` sends  [ 1, 3 ]@0

Example B:
1. { "first": 1, "third": 3, "fifth": 5 } @0 received via `dict`
2. "second"@0 received via `key`
3. `values` sends  [ 1, null ]@0

More:
https://github.com/Cranq-io/cranq-tutorials/tree/main/reference/3_querying_data/3_1_getters

### Input ports:

* __dict__: _{string: any}_

    Receives the dictionary to get the values from.
    
    Example:
    { "first": 1, "third": 3, "fifth": 5 }



* __keys__: _string[]_

    Receives the keys corresponding to the values to get.
    
    Example:
    ["first", "third"]



### Output ports:

* __values__: _{string: any}[string][]_

    Sends the values corresponding to the received keys.
    
    Example:
    [1, 3]



