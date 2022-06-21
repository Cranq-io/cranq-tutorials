# Merger

[data/dictionary]

Merges dictionary `b` to dictionary `a`. Values of `a` will be ignored on key conflict.

Example:
1. { "first": 1, "third": 0 }@0 received via `a`
2. { "third": 3, "fifth": 5 }@0 received via `b`
3. `merged` sends { "first": 1, "third": 3, "fifth": 5 }@0

More:
https://github.com/Cranq-io/cranq-tutorials/tree/main/reference/2_constructing_data/2_4_merge_concat

### Input ports:

* __a__: _{string: any}_

    Receives the dictionary to merge onto.
    
    Example:
    { "first": 1, "third": 0 }



* __b__: _{string: any}_

    Receives the dictionary to merge with.
    
    Example:
    { "third": 3, "fifth": 5 }



### Output ports:

* __merged__: _({string: any} and {string: any})_

    Sends the resulting merged dictionary.
    
    Example:
    { "first": 1, "third": 3, "fifth": 5 }



