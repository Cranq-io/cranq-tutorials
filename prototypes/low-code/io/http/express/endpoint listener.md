# Endpoint listener

[low-code/io/http/express]

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

* __response__: _{"status" :number, "headers" :{string: string}, "body" :string}_



* __params__: _({"appId" :string, "port" :number, "method" :("GET" or "POST" or "PUT" or "PATCH" or "DELETE"), "route" :string, optional "request" :{optional "bearerToken" :string, optional "contentType" :("text" or "json" or "urlencoded")}, optional "response" :{optional "contentType" :("text" or "json")}} and {"timeout" :number})_



### Output ports:

* __request__: _`io/http/Request`_



