# Step iterator

[data/array]

Iterates over the items of an array, asynchronously.

Tags are controlled:

On receiving the array, the node sends out the first item (if any) using a nested tag. (":0" appended to the original tag.)

Subsequent items will be sent out on receiving signals on `next`, with incremented tags.

### Input ports:

* __array__: _any[]_

    Sets up iteration and sends out the first item and index 0 with an iterable tag based on the original tag.
    
    When the array has only one or zero elements, a signal with the same tag will also be sent through `done`.
    
    Example:
    [1,2,3]



* __next__: _any_

    Triggers sending out the next item and index, or, when there are no more items, the done signal.
    
    Tags on signals received through `next` are expected to be iterable, and identical to the tag sent out for the previous item. (This allows for simple loopbacks between `item` and `next`.)
    
    Tags on signals sent out on `item` and `index` are incremented versions of what was received through `next`.
    
    Example:
    0



### Output ports:

* __item__: _any[][number]_

    Sends the next item in the array.
    
    Tags are iterable, and nested versions of the tag of the received array. (If the array tag was "start", item tags will be "start:0", "start:1", etc.)
    
    Example:
    1



* __index__: _number_

    Sends the next index in the array.
    
    Tags are iterable, and nested versions of the tag of the received array. (If the array tag was "start", item tags will be "start:0", "start:1", etc.)
    
    Example:
    0



* __done__: _any[]_

    Sends out the iterated array when there are no more items in the array and a signal received through `next`, or, when an array is received through `array` that has one or 0 items.
    
    The tag of the outgoing signal matches that of he original array.
    
    Example:
    [1,2,3]



* __bounced__: _any_

    Sends any `next` signal that didn't satisfy the iterable tag requirement.
    



