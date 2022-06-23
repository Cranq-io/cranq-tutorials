# Created NFT lister

[blockchain/nftport/api v0]

Retrieves a list of NFTs created by the specified address, using the NFTPort API.

Requires NFTPort account.

https://docs.nftport.xyz/docs/nftport/b3A6MzA2ODYzMjM-retrieve-nf-ts-created-by-an-account

### Input ports:

* __API key__: _string_

    Receives the NFTPort API key.



* __creator address__: _string_

    Receives the address of the NFT creator.



* __params__: _{"chain" :"ethereum", "continuation" :string, "include" :("default" or "metadata"), "page_size" :number}_

    Receives parameters that customize the result NFT list.
    
    https://docs.nftport.xyz/docs/nftport/b3A6MzA2ODYzMjM-retrieve-nf-ts-created-by-an-account#Query-Parameters



### Output ports:

* __nfts__: _`blockchain/nftport/api v0/CreatorNft`[]_

    Sends the list of NFTs associated with a given creator.



* __response__: _any_



* __error__: _{"error" :{"response" :string, "error" :{"status_code" :number, "code" :string, "message" :string}}}_



