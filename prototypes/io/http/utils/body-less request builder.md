# Body-less request builder

[io/http/utils]

Builds a HTTP request that has no body.

### Input ports:

* __method__: _("GET" or "POST" or "PUT" or "PATCH" or "DELETE")_



* __URL__: _string_



* __headers__: _{string: string}_



### Output ports:

* __request__: _{"method" :("GET" or "POST" or "PUT" or "PATCH" or "DELETE"), "url" :string, "headers" :{string: string}}_



