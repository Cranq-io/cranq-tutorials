# Contract verifier error handler

[blockchain/ethereum/actions]

### Input ports:

* __error__: _any_

    Receives the data to be forwarded to either output.



* __command busy__: _any_

    The "busy" signal of a `system/Command runner` node.



### Output ports:

* __retry__: _any_

    Sends signal received via `data` when condition was true.



* __success__: _boolean_



