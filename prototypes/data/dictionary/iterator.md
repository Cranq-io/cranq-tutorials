---
description: [data/dictionary]
---

# Iterator

Iterates through items of a dictionary.

The tag on the output signals will contain the index of the current iteration.

Example:
1. { "first": 1, "third": 3, "fifth": 5 } @0 received via `dict`
2. `key` sends  "first"@0:0
3. `value` sends  1@0:0
4. `key` sends  "third"@0:1
5. `value` sends  3@0:1
6. `key` sends  "fifth"@0:2
7. `value` sends  5@0:2

More:
https://github.com/Cranq-io/cranq-tutorials/tree/main/reference/1_application_flow/1_2_iterators

### Input ports:

* __dict__: ` {string: any} `

    Receives the dictionary to iterate through.
    
    Example:
    { "first": 1, "third": 3, "fifth": 5 }

### Output ports:

* __value__: ` {string: any}[string] `

    Sends the value of the current item, with the tag corresponding to the iteration.


* __key__: ` string `

    Sends the key of the current item, with the tag corresponding to the iteration.

