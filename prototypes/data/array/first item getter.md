# First item getter

[data/array]

Retrieves first item of the array.

Example:
1. [1,2]@0 received via `array`
2. 1@0 sent via `item`

More:
https://github.com/Cranq-io/cranq-tutorials/blob/main/reference/3_querying_data/3_1_getters/README.md#getting-the-first--last-array-elements

### Input ports:

* __array__: `any[]`

    Receives array to retrieve first item from.
    
    Example:
    [1,2]

### Output ports:

* __item__: `any[][number]`

    Sends first item of the array.
    
    Example:
    1

