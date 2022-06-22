# Merger

[data/tree]

Merges two tree data structures. On conflict, the relevant paths / values of `b` take precedence.

### Input ports:

* __a__: _any_

    Receives tree data structure to merge to.



* __b__: _any_

    Receives tree data structure to be merged onto the one received via `a`. Data received via this port takes precedence on conflict.



### Output ports:

* __merged__: _any_

    Sends the merged tree structure.


