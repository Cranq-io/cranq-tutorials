---
description: [data/array]
---

# Builder

Builds an array of identical items.

Example:
1. "Foo"@0 recieved via  `item`
2. 3@0 recieved via `count` 
3. ["Foo", "Foo", "Foo"]@0 sent  via `array`

More:
https://github.com/Cranq-io/cranq-tutorials/tree/main/reference/2_constructing_data/2_2_builders

### Input ports:

* __item__: `any`

    Receives item to be added to the array.
    
    Example:
    "Foo"


* __count__: `number`

    Receives the number of times the item is to be add to the array.
    
    Example:
    3

### Output ports:

* __array__: `any[]`

    Sends the built array.
    
    Example:
    ["Foo", "Foo", "Foo"]

