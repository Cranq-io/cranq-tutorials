---
description: [data/array]
---

# Item prepender

Inserts item into the beginning of the  array.
Example: 
1. [1,2,3]@0 recieved via `array` 
2.  4@0 recieved via `index` 
3. [4,1,2,3]@0 sent via `array`



### Input ports:

* __array__: `any[]`

    Recieves array to prepend to.
    
    Example:
    [1,2,3]


* __item__: `any[][number]`

    Recieves item to prepend.
    
    Example:
    4

### Output ports:

* __array__: `any[]`

    Sends array with specified item inserted to the begining.
    
    Example:
    [4,1,2,3]

