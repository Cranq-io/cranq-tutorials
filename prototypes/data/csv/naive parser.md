# Naive parser

[data/csv]

Parses CSV naively. (Only commas, all values will be strings, quotes not recognized.)

Example:
1. "foo,1\nbar,2"@1 received via `csv`
2. [["foo", "1"], ["bar", "2"]]@1 sent via `2D array`

### Input ports:

* __csv__: _string_



### Output ports:

* __2D array__: _string[][]_


