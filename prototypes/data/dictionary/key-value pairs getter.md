---
description: [data/dictionary]
---

# Key-value pairs getter

Gets the key-value pairs from the dictionary as an array.

Example:
1. { "first": 1, "third": 3 }@0 is received by `dict`
2. `key-value pairs` sends [ { "key":"first", "value": 1 }, { "key":"third", "value": 3 } ]@0

More:
https://github.com/Cranq-io/cranq-tutorials/tree/main/reference/3_querying_data/3_1_getters

### Input ports:

* __dict__: ` {string: any} `

    Receives a dictionary to extract the key-value pairs from.
    
    Example:
     { "first": 1, "third": 3 }

### Output ports:

* __key-value pairs__: ` {"key" :string, "value" :{string: any}[string]}[] `

    Sends the extracted key-value pairs.
    
    Example:
    [ { "key":"first", "value": 1 }, { "key":"third", "value": 3 } ]

