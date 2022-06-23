# Request authenticator

[io/http/utils]

Authenticates request using the provided authentication method.

### Input ports:

* __request__: ``io/http/Request``
    Receives request to be authenticated



* __params__: `{optional "bearerToken" :string}`
    [Inherited from port `dict` of `item getter`] 
    Receives the dictionary to get the value from.
    
    Example:
    { "first": 1, "third": 3, "fifth": 5 }



### Output ports:

* __request__: ``io/http/Request``


* __error__: `{"error" :"incorrect bearer token"}`


