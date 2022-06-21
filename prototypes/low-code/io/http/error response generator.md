# Error response generator

[low-code/io/http]

Generates a default error response based on the error received from an `io/http/express/Endpoint listener`.

### Input ports:

* __error__: _{"error" :"incorrect bearer token"}_



### Output ports:

* __response__: _({"status" :400, "headers" :{string: string}, "body" :"Bad request"} or {"status" :403, "headers" :{string: string}, "body" :"Unauthorized"})_



