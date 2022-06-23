# Response fork by status

[io/http/utils]

Forwards `response` to either `on match` or `on mismatch` depending on whether the response matches the HTTP status received via `status`.

### Input ports:

* __status__: `number`
    Receives HTTP status code.



* __response__: ``io/http/Response``
    Receives HTTP response.



### Output ports:

* __on match__: ``io/http/Response``
    Forwards received response when it matches the HTTP status received via `status`.



* __on mismatch__: ``io/http/Response``
    Forwards received response when it does not match the HTTP status received via `status`.



