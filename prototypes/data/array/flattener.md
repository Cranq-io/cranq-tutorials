---
description: data/array]
---

# Flattener

Flattens a 2D array into a  1 D array with.

Example:
1. [[1,2], [3,4]]@0 recieved via `2D array`
2. [1,2,3,4]@0 sent via `array` 

### Input ports:

* __2D array__: `any[][]`

    Recieves 2D arrays to be flattened.
    
    Example:
    [[1,2], [3,4]]

### Output ports:

* __array__: `any[][][number][number][]`

    Sends flattened array.
    
    Example:
    [1,2,3,4]

