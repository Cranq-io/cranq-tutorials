---
description: io/http/utils]
---

# Body-less request builder

Builds a HTTP request that has no body.

### Input ports:

* __method__: `("GET" or "POST" or "PUT" or "PATCH" or "DELETE")`


* __URL__: `string`


* __headers__: `{string: string}`

### Output ports:

* __request__: 
    ```
    {"method" :("GET" or "POST" or "PUT" or "PATCH" or "DELETE"), "url" :string, "headers" :{string: string}}
    ```

