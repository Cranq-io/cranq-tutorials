# Builder (paths & values)

[data/tree]

Constructs a tree data structure based on the path-value pairs received via `paths` and `values`.

Bounces when the length of `values` and `path` don't match.

### Input ports:

* __paths__: _(string or number)[][]_

    Receives paths that form the structure of the constructed tree.



* __values__: _any[]_

    Receives the values that will be the leaf nodes of the constructed tree.



### Output ports:

* __tree__: _any_



* __bounced__: _{"paths" :(string or number)[][], "values" :any[]}_



