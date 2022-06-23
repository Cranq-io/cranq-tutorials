# Node getter

[data/tree]

Retrieves the node at the specified path of the tree.

Example:
1. {"foo": {"bar": "baz"}}@0 is received via `tree`
2. ["foo", "bar"]@0 is received via `path`
3. "baz"@0 is sent via `node`


### Input ports:

* __tree__: `(any[] or {string: any})`

    Receives the tree the node is extracted from


* __path__: `(string or number)[]`

    Receives the path segments in an array

### Output ports:

* __node__: `any`

    Sends the node at the specified path


* __not found__: `(string or number)[]`

    Sends the `path` if it was not found

