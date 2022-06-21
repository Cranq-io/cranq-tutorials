# Endpoint listener

[io/http/express]

Sets up a listener on an HTTP route. Starts an Express server if one is not started yet.

### Input ports:

* __response__: _{"status" :number, "headers" :{string: string}, "body" :string}_



* __params__: _{"appId" :string, "port" :number, "method" :("GET" or "POST" or "PUT" or "PATCH" or "DELETE"), "route" :string, optional "request" :{optional "bearerToken" :string, optional "contentType" :("text" or "json" or "urlencoded")}, optional "response" :{optional "contentType" :("text" or "json")}}_



### Output ports:

* __request__: _`io/http/Request`_



* __error__: _any_



