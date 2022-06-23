---
description: [data/dictionary]
---

# Builder (key-value pairs)

Builds a dictionary based on an array of objects with key & value properties.

Any non-conforming items in the array are discarded.

Example:
1. [ { "key":"first", "value": 1 }, { "key":"third", "value": 3 } ]@0 received via `key-value pairs`
2. `dict`sends { "first": 1, "third": 3 }@0

More:
https://github.com/Cranq-io/cranq-tutorials/tree/main/reference/2_constructing_data/2_2_builders

### Input ports:

* __key-value pairs__: `{"key" :string, "value" :any}[]`

    Receives objects having key & value properties.
    
    Example:
    [ { "key":"first", "value": 1 }, { "key":"third", "value": 3 } ]

### Output ports:

* __dict__: 
    ```
    {string: {"key" :string, "value" :any}[][number]["value"]}
    ```

    Sends the resulting dictionary.
    
    Example:
    { "first": 1, "third": 3 }

