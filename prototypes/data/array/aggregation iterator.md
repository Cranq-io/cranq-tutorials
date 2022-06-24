---
description: [data/array]
---

# Aggregation iterator

Iterates through items of an array, specifically for the purpose of being aggregated later.

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


* __is last__: ` boolean `

    Sends flag whether current item is the last one.
    
    To be connected directly to the `release` input of a `flow/Aggregator`.

