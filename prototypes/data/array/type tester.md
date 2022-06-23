# Type tester

[data/array]

Tells whether the input is an array.

Example:
1. [1,2,3]@0 received via `data`
2. true@0 sent via `is array`

### Input ports:

* __data__: `any[]`
    Receives data to test if its type is array.
    
    Example:
    [1,2,3]



### Output ports:

* __is array__: `boolean`
    Sends if the type of the recieved `data` is array.
    
    Example:
    true



