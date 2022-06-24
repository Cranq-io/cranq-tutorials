---
description: [blockchain/nftport/api v0]
---

# Request dispatcher

Dispatches a POST request to one of the NFTPort API endpoints.

### Input ports:

* __API key__: ` string `

    Receives the NFT port API key.


* __URL__: ` string `

    Receives the target NFT port endpoint.
    


* __body__: ` string `

    Receives the post data.


* __method__: ` any `

### Output ports:

* __data__: ` any `


* __error__: ` {"error" :string} `


* __response__: 
    ```
    {"status" :number, "headers" :{string: string}, "body" :string}
    ```

    Sends the reconstructed HTTP response.

