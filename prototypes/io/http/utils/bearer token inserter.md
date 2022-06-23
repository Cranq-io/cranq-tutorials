---
description: [io/http/utils]
---

# Bearer token inserter

Inserts bearer token into a HTTP request header.

Example:
1. { "content-type": "application/json" }@0 received on  `headers`
2. "SomeDummyToken"@0 received on `token`
3. {"content-type": "application/json", "Authorization": "Bearer SomeDummyToken" }@0 sent on `headers`

### Input ports:

* __headers__: `{string: string}`

    Recieves request headers. It is  used to describe a resource, or the behavior of the server or the client.
    
    Example:
    {
      "content-type": "application/json; charset=utf-8"
    }


* __token__: `string`

    Receives the string token to be inserted into the Authorization header as Bearer token.
    The token is usually used in base64 encoded form.
    
    Example: 
    - "SomeDummyToken" as plain text 
    - "U29tZUR1bW15VG9rZW4=" as base64 encoded text

### Output ports:

* __headers__: `{string: string}`

    Sends the received request headers with the authorization header added to it.
    
    Example:
    {
      "content-type": "application/json", 
      "Authorization": "Bearer SomeDummyToken" 
    }

