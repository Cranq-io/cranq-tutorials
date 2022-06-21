# Response builder

[io/http/utils]

Builds a response structure out of its components: HTTP status, headers, and body.

Example:
1. 200@1 received via `status`
2. {"Content-Type": "text/plain"}@1 received via `headers`
3. "OK"@1 received via `body`
4. {"status": 200, "headers": {"Content-Type": "text/plain"}, "body": "OK"}@1 sent via `response`

### Input ports:

* __body__: _string_

    Receives the body of the response.
    
    Example:
    "OK"



* __status__: _number_

    Receives a HTTP status code.
    
    Example:
    200



* __headers__: _{string: string}_

    Receives a record of HTTP headers.
    
    Example:
    {"Contanet-Type": "text/plain"}



### Output ports:

* __response__: _{"status" :number, "headers" :{string: string}, "body" :string}_

    Sends the constructed HTTP response.



