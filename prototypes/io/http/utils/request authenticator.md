# Request authenticator

[io/http/utils]

Authenticates request using the provided authentication method.

### Input ports:

* __request__: _`io/http/Request`_

    Receives request to be authenticated



* __params__: _{optional "bearerToken" :string}_

    [Inherited from port `dict` of `item getter`] 
    Receives the dictionary to get the value from.
    
    Example:
    { "first": 1, "third": 3, "fifth": 5 }



### Output ports:

* __request__: _`io/http/Request`_



* __error__: _{"error" :"incorrect bearer token"}_



