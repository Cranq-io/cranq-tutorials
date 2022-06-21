---
description: [data/array]
---

# Iterator

Iterates through items of an array.


Examples:
https://github.com/Cranq-io/cranq-tutorials/tree/main/reference/1_application_flow/1_2_iterators

### Input ports:

* __array__: ` any[] `

    Recieves array to be iterated over.
    
    Example:
    [1,2,3]
    

### Output ports:

* __item__: ` any[][number] `

    Sends current item.
    
    Example:
    1


* __index__: ` number `

    Sends current index.
    
    Example:
    0


* __done__: ` any[] `

