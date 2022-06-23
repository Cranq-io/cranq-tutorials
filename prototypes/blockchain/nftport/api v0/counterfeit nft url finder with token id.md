# Counterfeit NFT URL finder with token ID

[blockchain/nftport/api v0]

Retrieves list of file URLs for duplicate (i.e. counterfeit) NFTs.

Requires NFTPort account.

https://docs.nftport.xyz/docs/nftport/b3A6MjQ1OTQxMDc-find-counterfeit-nf-ts-w-token-id

### Input ports:

* __NFT ID__: _{"contractAddress" :string, "tokenId" :string}_



* __params__: _{"apiKey" :string, optional "chain" :("ethereum" or "polygon"), optional "page_number" :number, optional "page_size" :number, optional "threshold" :number}_



### Output ports:

* __file URLs__: _string[]_



* __error__: _{"error" :string}_



