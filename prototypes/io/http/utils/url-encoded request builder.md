---
description: [io/http/utils]
---

# URL-encoded request builder

Builds a URL-encoded request record with data to be sent as the request's body.

For body-less requests, see `io/http/utils/Body-less request builder`.

### Input ports:

* __method__: `("GET" or "POST" or "PUT" or "PATCH" or "DELETE")`


* __url__: `string`


* __headers__: `{string: string}`


* __data__: `{string: (string or string[])}`

### Output ports:

* __URL-enc. req.__: 
    ```
    {"method" :("GET" or "POST" or "PUT" or "PATCH" or "DELETE"), "url" :string, "headers" :{string: string}, "data" :{string: (string or string[])}}
    ```

