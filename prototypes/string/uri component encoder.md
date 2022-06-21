# URI component encoder

[string]

URI component-encodes the received string.

Example:
1. "hello world"@1 received via `string`
2. "hello%20world"@1 sent via `encoded`

### Input ports:

* __string__: _any_

    Receives a string to be URI component-encoded.



### Output ports:

* __encoded__: _string_

    Sends the URI component-encoded string.



