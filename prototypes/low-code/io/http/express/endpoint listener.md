---
description: [low-code/io/http/express]
---

# Endpoint listener

Opinionated low-code version of `io/http/express/Endpoint listener`.

Sets up a listener on an HTTP route, and handles bad request errors. Starts an Express server if one is not started yet.

Possible error responses:
* {
    "status": 400,
    "headers": {},
    "body": "Bad request"
  }
* {
    "status": 403,
    "headers": {},
    "body": "Unauthorized"
  }

### Input ports:

* __response__: 
    ```
    {"status" :number, "headers" :{string: string}, "body" :string}
    ```


* __params__: 
    ```
    ({"appId" :string, "port" :number, "method" :("GET" or "POST" or "PUT" or "PATCH" or "DELETE"), "route" :string, optional "request" :{optional "bearerToken" :string, optional "contentType" :("text" or "json" or "urlencoded")}, optional "response" :{optional "contentType" :("text" or "json")}} and {"timeout" :number})
    ```

### Output ports:

* __request__: ``io/http/Request``

