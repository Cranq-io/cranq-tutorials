# Counterfeit NFT finder with token ID

[blockchain/nftport/api v0]

Retrieves list of duplicate (i.e. counterfeit) NFTs. 

Requires NFTPort account.

https://docs.nftport.xyz/docs/nftport/b3A6MjQ1OTQxMDc-find-counterfeit-nf-ts-w-token-id

### Input ports:

* __API key__: _string_

    Receives the NFTPort API key.



* __contract address__: _string_

    Receives the address of the NFT.



* __token ID__: _any_

    Receives the token ID of the NFT.



* __params__: _{optional "chain" :("ethereum" or "polygon"), optional "page_number" :number, optional "page_size" :number, optional "threshold" :number}_

    Receives parameters that customize the result NFT list.
    
    https://docs.nftport.xyz/docs/nftport/b3A6MjQ1OTQxMDc-find-counterfeit-nf-ts-w-token-id#request-body



### Output ports:

* __similar NFTs__: _`blockchain/nftport/api v0/SimilarNft`[]_



* __error__: _{"error" :string}_



* __response__: _any_



