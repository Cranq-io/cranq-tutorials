---
description: [io/http/express]
---

# Endpoint listener

Sets up a listener on an HTTP route. Starts an Express server if one is not started yet.

### Input ports:

* __response__: 
    ```
    {"status" :number, "headers" :{string: string}, "body" :string}
    ```


* __params__: 
    ```
    {"appId" :string, "port" :number, "method" :("GET" or "POST" or "PUT" or "PATCH" or "DELETE"), "route" :string, optional "request" :{optional "bearerToken" :string, optional "contentType" :("text" or "json" or "urlencoded")}, optional "response" :{optional "contentType" :("text" or "json")}}
    ```

### Output ports:

* __request__: ``io/http/Request``


* __error__: `any`

