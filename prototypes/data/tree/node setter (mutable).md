# Node setter (mutable)

[data/tree]

Sets a node at the specified path of the tree. Mutates input.

Warning! This node mutates the tree it gets that means if any other node received the same tree as input from the original source it may get the modified tree depending on the execution order!

Example:
1. {"foo": {"bar": 1}}@0 is received via `tree`
2. ["foo", "baz"]@0 is received via `path`
3. 1@0 is received via `node`
4. {"foo": {"bar": 1, "baz": 1}}@0 is sent via `modified tree`

### Input ports:

* __tree__: _(any[] or {string: any})_

    Tree data structure in which to store a node.
    
    Will be mutated.



* __path__: _(string or number)[]_

    Receives the path segments where the `node` should  be written to



* __node__: _any_

    Receives the node to be set



### Output ports:

* __modified tree__: _(any[] or {string: any})_

    Sends the modified tree


