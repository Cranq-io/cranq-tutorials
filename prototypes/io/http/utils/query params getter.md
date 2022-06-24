---
description: [io/http/utils]
---

# Query params getter

Retrieves the 'query' component of an HTTP request.

Example:
1. {"headers": {}, "query": {"message": "Hello"}}@1 received via `request`
2. {"message": "Hello"}@1 sent via `query`

### Input ports:

* __request__: ` {"query" :{string: (string or string[])}} `

    Receives an HTTP request that has query params.

### Output ports:

* __query__: ` {string: (string or string[])} `

    Sends the 'query' component of the received request.

