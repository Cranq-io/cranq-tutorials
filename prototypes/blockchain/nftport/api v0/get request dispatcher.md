# GET request dispatcher

[blockchain/nftport/api v0]

Dispatches a GET request to one of the NFTPort API endpoints.

### Input ports:

* __API key__: _string_



* __URL__: _string_

    [Inherited from port `url` of `dispatch request`] 
    Receives the target of the HTTP request. Also called "resource" 
    
    Example:
    "https://jsonplaceholder.typicode.com/todos/1"



### Output ports:

* __data__: _any_



* __error__: _{"error" :string}_



* __response__: _{"status" :number, "headers" :{string: string}, "body" :string}_

    Sends the reconstructed HTTP response.



