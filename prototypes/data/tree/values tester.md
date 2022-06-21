# Values tester

[data/tree]

Tests for deep equality for `tree` and `reference`.

Example:
1. {"foo":{"bar":"baz"}}@0 is received via `tree`
2. {"foo":{"bar":"baz"}}@0 is received via `reference`
3. true@0 is sent via `all values are same`

### Input ports:

* __tree__: _(any[] or {string: any})_

    The tree to test



* __reference__: _(any[] or {string: any})_

    The reference tree structure



### Output ports:

* __all values are same__: _boolean_

    Whether all nodes of the `data` tree are the same as the `reference`



