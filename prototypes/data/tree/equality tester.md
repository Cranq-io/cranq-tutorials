# Equality tester

[data/tree]

Tests whether the tree equals the reference (same structure and same values).

Example:
1. { "a":1, "b":1 }@0 is received via `tree`
2. { "a":1, "b":1 }@0 is received via `reference`
3. true@0 is sent via `equals`

### Input ports:

* __tree__: `(any[] or {string: any})`

    The tree to test for equality with `reference`


* __reference__: `(any[] or {string: any})`

    The reference tree structure

### Output ports:

* __equals__: `boolean`

    Whether all values in the tree are the same as the items with the same key in the reference

