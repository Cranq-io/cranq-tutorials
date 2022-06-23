# Item inserter

[data/array]

Inserts item into the array at the specified index.

Example: 
1. [1,2,3]@0 recieved via `array` 
2.  1@0 recieved via `index` 
2. 1@0 recieved via `item` 
3. [1,1,2,3]@0 sent via `array`

More:
https://github.com/Cranq-io/cranq-tutorials/blob/main/reference/2_constructing_data/2_1_setters_deleters/README.md#example---inserting-items-into-arrays

### Input ports:

* __array__: `any[]`

    Recieves array to insert into.
    
    Example:
    [1,2,3]


* __index__: `number`

    Recieves index at which to insert.
    
    Example:
    1


* __item__: `any`

    Recieves item to be inserted.
    
    Example:
    1

### Output ports:

* __array__: `any[][number][]`

    Sends array with specified item inserted.
    
    Example:
    [1,1,2,3]

