# Concatenator

[data/array]

Concatenates two arrays.

Example:
1. [1,2]@0 recieved via `a`
1. [3,4]@0 recieved via `b`
3. [1,2,3,4]@0 sent via `concatenated`

More:
https://github.com/Cranq-io/cranq-tutorials/blob/main/reference/2_constructing_data/2_4_merge_concat/README.md#example---concatenating-arrays

### Input ports:

* __a__: _any[]_

    Receives array `a` to concatenate.
    
    Example:
    [1,2]



* __b__: _any[]_

    Receives array `b` to concatenate.
    
    Example:
    [3,4]



### Output ports:

* __concatenated__: _(any[] or any[])_

    Sends the concatenated array.
    
    Example:
    [1,2,3,4]



