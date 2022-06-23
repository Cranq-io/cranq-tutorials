---
description: [blockchain/nftport/api v0]
---

# POST request dispatcher

Dispatches a POST request to one of the NFTPort API endpoints.

### Input ports:

* __API key__: `string`

    Receives the NFT port API key.


* __URL__: `string`

    Receives the target NFT port endpoint.
    


* __data__: `{string: any}`

    Receives the post data.

### Output ports:

* __data__: `any`


* __error__: `{"error" :string}`


* __response__: 
    ```
    {"status" :number, "headers" :{string: string}, "body" :string}
    ```

    Sends the reconstructed HTTP response.

