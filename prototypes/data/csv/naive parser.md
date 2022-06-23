---
description: [data/csv]
---

# Naive parser

Parses CSV naively. (Only commas, all values will be strings, quotes not recognized.)

Example:
1. "foo,1\nbar,2"@1 received via `csv`
2. [["foo", "1"], ["bar", "2"]]@1 sent via `2D array`

### Input ports:

* __csv__: `string`

### Output ports:

* __2D array__: `string[][]`

