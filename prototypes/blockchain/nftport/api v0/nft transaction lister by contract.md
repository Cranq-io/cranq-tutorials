---
description: [blockchain/nftport/api v0]
---

# NFT transaction lister by contract

Retrieves a list of transfers matching the specified contract address and token ID using the NFTPort API. Also returns the original API response for additional information.

Requires NFTPort account.

API key and endpoint documentation:
https://docs.nftport.xyz/docs/nftport/b3A6MzAxNDQ3NzY-retrieve-transactions-by-contract

### Input ports:

* __API key__: `string`

    Receives the NFTPort API key.


* __address__: `string`

    Receives the contract address for a token.


* __params__: 
    ```
    {"chain" :"ethereum", "continuation" :string, "include" :("default" or "metadata"), "page_size" :number}
    ```

    Receives parameters that customize the result transfer list.
    
    https://docs.nftport.xyz/docs/nftport/b3A6MzAxNDQ3NzY-retrieve-transactions-by-contract#Query-Parameters


* __token ID__: `string`

    Receives the identifier of the token in the context of its governing contract.

### Output ports:

* __transactions__: ``blockchain/nftport/NFT transaction`[]`


* __error__: `{"error" :string}`


* __response__: 
    ```
    {"status" :number, "headers" :{string: string}, "data" :`blockchain/nftport/NFT transactions by contract response`}
    ```

