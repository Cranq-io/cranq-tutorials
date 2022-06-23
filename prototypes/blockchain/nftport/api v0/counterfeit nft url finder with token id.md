# Counterfeit NFT URL finder with token ID

[blockchain/nftport/api v0]

Retrieves list of file URLs for duplicate (i.e. counterfeit) NFTs.

Requires NFTPort account.

https://docs.nftport.xyz/docs/nftport/b3A6MjQ1OTQxMDc-find-counterfeit-nf-ts-w-token-id

### Input ports:

* __NFT ID__: `{"contractAddress" :string, "tokenId" :string}`


* __params__: 
    ```
    {"apiKey" :string, optional "chain" :("ethereum" or "polygon"), optional "page_number" :number, optional "page_size" :number, optional "threshold" :number}
    ```



### Output ports:

* __file URLs__: `string[]`


* __error__: `{"error" :string}`


