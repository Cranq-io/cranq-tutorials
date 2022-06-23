---
description: [data/array]
---

# Last item getter

Retrieves last item of the array.

Example:
1. [1,2]@0 received via `array`
2. 2@0 sent via `item`

More:
https://github.com/Cranq-io/cranq-tutorials/tree/main/reference/3_querying_data/3_1_getters#getting-the-first--last-array-elements

### Input ports:

* __array__: `any[]`

    Recieves array to retrieve last item from.
    
    Example:
    [1,2]

### Output ports:

* __item__: `any[][number]`

    Sends last item of the array.
    
    Example:
    2

