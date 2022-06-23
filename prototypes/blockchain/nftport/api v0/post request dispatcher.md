# POST request dispatcher

[blockchain/nftport/api v0]

Dispatches a POST request to one of the NFTPort API endpoints.

### Input ports:

* __API key__: _string_

    Receives the NFT port API key.



* __URL__: _string_

    Receives the target NFT port endpoint.
    



* __data__: _{string: any}_

    Receives the post data.



### Output ports:

* __data__: _any_



* __error__: _{"error" :string}_



* __response__: _{"status" :number, "headers" :{string: string}, "body" :string}_

    Sends the reconstructed HTTP response.



