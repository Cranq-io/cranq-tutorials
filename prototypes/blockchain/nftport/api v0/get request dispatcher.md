# GET request dispatcher

[blockchain/nftport/api v0]

Dispatches a GET request to one of the NFTPort API endpoints.

### Input ports:

* __API key__: `string`


* __URL__: `string`

    [Inherited from port `url` of `dispatch request`] 
    Receives the target of the HTTP request. Also called "resource" 
    
    Example:
    "https://jsonplaceholder.typicode.com/todos/1"

### Output ports:

* __data__: `any`


* __error__: `{"error" :string}`


* __response__: 
    ```
    {"status" :number, "headers" :{string: string}, "body" :string}
    ```

    Sends the reconstructed HTTP response.

