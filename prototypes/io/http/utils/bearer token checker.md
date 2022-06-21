# Bearer token checker

[io/http/utils]

Checks for the presence of the specified bearer token in the submitted request headers. Forwards request body only when found.

### Input ports:

* __bearer token__: _string_

    Receives the bearer token to be verified.



* __request__: _{"headers" :{string: string}, "body" :string}_

    Receives the request to be authorized.



### Output ports:

* __request__: _{"headers" :{string: string}, "body" :string}_



* __error__: _{"error" :"incorrect bearer token"}_



