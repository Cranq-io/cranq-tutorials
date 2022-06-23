---
description: data/tree]
---

# Builder (paths & values)

Constructs a tree data structure based on the path-value pairs received via `paths` and `values`.

Bounces when the length of `values` and `path` don't match.

### Input ports:

* __paths__: `(string or number)[][]`

    Receives paths that form the structure of the constructed tree.


* __values__: `any[]`

    Receives the values that will be the leaf nodes of the constructed tree.

### Output ports:

* __tree__: `any`


* __bounced__: `{"paths" :(string or number)[][], "values" :any[]}`

