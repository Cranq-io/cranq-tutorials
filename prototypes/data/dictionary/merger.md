---
description: data/dictionary]
---

# Merger

Merges dictionary `b` to dictionary `a`. Values of `a` will be ignored on key conflict.

Example:
1. { "first": 1, "third": 0 }@0 received via `a`
2. { "third": 3, "fifth": 5 }@0 received via `b`
3. `merged` sends { "first": 1, "third": 3, "fifth": 5 }@0

More:
https://github.com/Cranq-io/cranq-tutorials/tree/main/reference/2_constructing_data/2_4_merge_concat

### Input ports:

* __a__: `{string: any}`

    Receives the dictionary to merge onto.
    
    Example:
    { "first": 1, "third": 0 }


* __b__: `{string: any}`

    Receives the dictionary to merge with.
    
    Example:
    { "third": 3, "fifth": 5 }

### Output ports:

* __merged__: `({string: any} and {string: any})`

    Sends the resulting merged dictionary.
    
    Example:
    { "first": 1, "third": 3, "fifth": 5 }

