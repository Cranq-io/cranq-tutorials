# Node getter

[data/tree]

Retrieves the node at the specified path of the tree.

Example:
1. {"foo": {"bar": "baz"}}@0 is received via `tree`
2. ["foo", "bar"]@0 is received via `path`
3. "baz"@0 is sent via `node`


### Input ports:

* __tree__: _(any[] or {string: any})_

    Receives the tree the node is extracted from



* __path__: _(string or number)[]_

    Receives the path segments in an array



### Output ports:

* __node__: _any_

    Sends the node at the specified path



* __not found__: _(string or number)[]_

    Sends the `path` if it was not found



