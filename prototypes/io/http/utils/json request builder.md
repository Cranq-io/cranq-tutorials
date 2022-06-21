# JSON request builder

[io/http/utils]

Builds a JSON request record with data to be sent as the request's body.

For body-less requests, see `io/http/utils/Body-less request builder`.

### Input ports:

* __method__: _("GET" or "POST" or "PUT" or "PATCH" or "DELETE")_



* __url__: _string_



* __headers__: _{string: string}_



* __data__: _any_



### Output ports:

* __JSON req.__: _{"method" :("GET" or "POST" or "PUT" or "PATCH" or "DELETE"), "url" :string, "headers" :{string: string}, "data" :any}_



