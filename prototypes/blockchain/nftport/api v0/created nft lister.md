---
description: [blockchain/nftport/api v0]
---

# Created NFT lister

Retrieves a list of NFTs created by the specified address, using the NFTPort API.

Requires NFTPort account.

https://docs.nftport.xyz/docs/nftport/b3A6MzA2ODYzMjM-retrieve-nf-ts-created-by-an-account

### Input ports:

* __API key__: ` string `

    Receives the NFTPort API key.


* __creator address__: ` string `

    Receives the address of the NFT creator.


* __params__: 
    ```
    {"chain" :"ethereum", "continuation" :string, "include" :("default" or "metadata"), "page_size" :number}
    ```

    Receives parameters that customize the result NFT list.
    
    https://docs.nftport.xyz/docs/nftport/b3A6MzA2ODYzMjM-retrieve-nf-ts-created-by-an-account#Query-Parameters

### Output ports:

* __nfts__: `` `blockchain/nftport/api v0/CreatorNft`[] ``

    Sends the list of NFTs associated with a given creator.


* __response__: ` any `


* __error__: 
    ```
    {"error" :{"response" :string, "error" :{"status_code" :number, "code" :string, "message" :string}}}
    ```

