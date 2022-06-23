# Contract verifier error handler

[blockchain/ethereum/actions]

### Input ports:

* __error__: `any`

    Receives the data to be forwarded to either output.


* __command busy__: `any`

    The "busy" signal of a `system/Command runner` node.

### Output ports:

* __retry__: `any`

    Sends signal received via `data` when condition was true.


* __success__: `boolean`

