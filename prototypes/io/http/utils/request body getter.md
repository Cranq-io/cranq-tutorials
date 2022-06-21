# Request body getter

[io/http/utils]

Retrieves the 'body' component of an HTTP request.

Example:
1. {"headers": {}, "body": "Hello"}@1 received via `request`
2. "Hello"@1 sent via `body`

### Input ports:

* __request__: _{"body" :any}_

    Receives an HTTP request that has a body.



### Output ports:

* __body__: _{"body" :any}["body"]_

    Sends the 'body' component of the received request.



