# Request dispatcher

[blockchain/nftport/api v0]

Dispatches a POST request to one of the NFTPort API endpoints.

### Input ports:

* __API key__: _string_

    Receives the NFT port API key.



* __URL__: _string_

    Receives the target NFT port endpoint.
    



* __body__: _string_

    Receives the post data.



* __method__: _any_



### Output ports:

* __data__: _any_



* __error__: _{"error" :string}_



* __response__: _{"status" :number, "headers" :{string: string}, "body" :string}_

    Sends the reconstructed HTTP response.



