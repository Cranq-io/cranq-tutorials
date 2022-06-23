# Item getter

[data/array]

Retrieves item from the specified index.
If the item is not found, the inputs are sent via `not found`.

Example A:
1. [1,2]@0  received via `array`
2. 1@0  recieved via `index`
3. 2@0  sent via `item`

Example B:
1. [1,2]@0  received via `array`
2. 9@0  recieved via `index`
3. {"array":[1,2], "index":9}@0  sent via `not found`

More:
https://github.com/Cranq-io/cranq-tutorials/blob/main/reference/3_querying_data/3_1_getters/README.md#getting-array-element-by-index

### Input ports:

* __array__: `any[]`

    Recieves array to retrieve item from.
    
    Example:
    [1,2]


* __index__: `number`

    Recieves index which identifies item to be retrieved in the array.
    
    Example:
    1

### Output ports:

* __item__: `any[][number]`

    Sends item at the specified index.
    
    Example:
    2


* __not found__: `{"array" :any[], "index" :number}`

