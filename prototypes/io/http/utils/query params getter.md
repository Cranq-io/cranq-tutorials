# Query params getter

[io/http/utils]

Retrieves the 'query' component of an HTTP request.

Example:
1. {"headers": {}, "query": {"message": "Hello"}}@1 received via `request`
2. {"message": "Hello"}@1 sent via `query`

### Input ports:

* __request__: _{"query" :{string: (string or string[])}}_

    Receives an HTTP request that has query params.



### Output ports:

* __query__: _{string: (string or string[])}_

    Sends the 'query' component of the received request.



