---
description: [blockchain/nftport/api v0]
---

# Counterfeit NFT finder with token ID

Retrieves list of duplicate (i.e. counterfeit) NFTs. 

Requires NFTPort account.

https://docs.nftport.xyz/docs/nftport/b3A6MjQ1OTQxMDc-find-counterfeit-nf-ts-w-token-id

### Input ports:

* __API key__: ` string `

    Receives the NFTPort API key.


* __contract address__: ` string `

    Receives the address of the NFT.


* __token ID__: ` any `

    Receives the token ID of the NFT.


* __params__: 
    ```
    {optional "chain" :("ethereum" or "polygon"), optional "page_number" :number, optional "page_size" :number, optional "threshold" :number}
    ```

    Receives parameters that customize the result NFT list.
    
    https://docs.nftport.xyz/docs/nftport/b3A6MjQ1OTQxMDc-find-counterfeit-nf-ts-w-token-id#request-body

### Output ports:

* __similar NFTs__: `` `blockchain/nftport/api v0/SimilarNft`[] ``


* __error__: ` {"error" :string} `


* __response__: ` any `

