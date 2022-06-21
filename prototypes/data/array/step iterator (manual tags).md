---
description: [data/array]
---

# Step iterator (manual tags)

Iterates over the items of an array asynchronously.

On receiving the array, the node sends out the first item (if any) using the same tag.

Subsequent items will be sent out on receiving signals on `next`, using the same tag.

### Input ports:

* __array__: ` any[] `

    Sets up iteration and sends out the first item and index 0 with the tag associated with the received array.
    When the array has only one or zero elements, a signal will also be sent through `done`. 
    
    Example:
    ["A","B","C"]


* __next__: ` any `

    Triggers sending out the next item and index, or, when there are no more items, the done signal.
    
    Signals sent out on `item` and `index` bear the same tag as the signal received through `next`.
    
    Example:
    0

### Output ports:

* __item__: ` any[][number] `

    The next item in the array.
    
    The first item (index 0) bears the tag of the received array, subsequent items bear the tag of the corresponding signals received through `next`.
    
    Example:
    "A"


* __index__: ` number `

    The next index in the array.
    
    The first index (0) bears the tag of the received array, subsequent indexes bear the tag of the corresponding signals received through `next`.
    
    Example:
    0


* __done__: ` any[] `

    Sends out the iterated array when there are no more items in the array and a signal was received through `next`, or, when an array was received through `array` that has one or 0 items.
    
    The tag of the outgoing signal matches that of he original array.
    
    Example:
    ["A","B","C"]

