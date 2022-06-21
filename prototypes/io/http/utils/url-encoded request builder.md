# URL-encoded request builder

[io/http/utils]

Builds a URL-encoded request record with data to be sent as the request's body.

For body-less requests, see `io/http/utils/Body-less request builder`.

### Input ports:

* __method__: _("GET" or "POST" or "PUT" or "PATCH" or "DELETE")_



* __url__: _string_



* __headers__: _{string: string}_



* __data__: _{string: (string or string[])}_



### Output ports:

* __URL-enc. req.__: _{"method" :("GET" or "POST" or "PUT" or "PATCH" or "DELETE"), "url" :string, "headers" :{string: string}, "data" :{string: (string or string[])}}_



