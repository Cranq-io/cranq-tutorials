---
description: [low-code/io/http]
---

# Error response generator

Generates a default error response based on the error received from an `io/http/express/Endpoint listener`.

### Input ports:

* __error__: `{"error" :"incorrect bearer token"}`

### Output ports:

* __response__: 
    ```
    ({"status" :400, "headers" :{string: string}, "body" :"Bad request"} or {"status" :403, "headers" :{string: string}, "body" :"Unauthorized"})
    ```

