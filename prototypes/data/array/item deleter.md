# Item deleter

[data/array]

Deletes item from the array at the specified index.

Example: 
1.  [1,2,3]@0 recieved via array 
2. 1@0 recieved via `index` 
3. [1,3]@0 sent via `array`

More:
https://github.com/Cranq-io/cranq-tutorials/blob/main/reference/2_constructing_data/2_1_setters_deleters/README.md#example---deleting-items-from-arrays

### Input ports:

* __array__: _any[]_

    Recieves array to delete item from.
    
    Example:
    [1,2,3]



* __index__: _number_

    Recieves index which identifies item to be deleted from the array.
    
    Example:
    1



### Output ports:

* __array__: _any[]_

    Sends array with specified item deleted.
    
    Example:
    [1,3]



