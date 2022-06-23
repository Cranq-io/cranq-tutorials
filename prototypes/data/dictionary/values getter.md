# Values getter

[data/dictionary]

Gets all values from the dictionary as an array.


Example A:
1. { "first": 1, "third": 3, "fifth": 5 } @0 received via `dict`
2. `values` sends  [ 1,3,5 ]@0

More:
https://github.com/Cranq-io/cranq-tutorials/tree/main/reference/3_querying_data/3_1_getters

### Input ports:

* __dict__: `{string: any}`
    Receives the dictionary to extract the values from.
    
    Example:
    { "first": 1, "third": 3, "fifth": 5 } 



### Output ports:

* __values__: `{string: any}[string]`
    Sends the values of the dictionary as an array,
    
    Example:
    [ 1,3,5 ]



