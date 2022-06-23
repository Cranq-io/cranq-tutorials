# NFT data getter

[blockchain/moralis/api v2]

Retrieves information of the NFT for the specified contract and token ID using the Moralis API. Also returns the original API response for additional information.

Requires Moralis account.

API key and endpoint documentation can be found at:
https://admin.moralis.io/web3Api

### Input ports:

* __API key__: `string`


* __address__: `string`
    Receives the contract address for a token.



* __token ID__: `string`
    Receives the identifier of the token in the context of its governing contract.



* __params__: 
    ```
    {"chain" :("eth" or "ropsten" or "rinkeby" or "goerli" or "kovan" or "polygon" or "mumbai" or "bsc" or "bsc testnet" or "avalanche" or "avalanche testnet" or "fantom"), "format" :("decimal" or "hex"), "offset" :number, "limit" :number, "order" :string, "cursor" :string}
    ```

    Receives parameters refining the transfers query.
    
    Example:  
    {  
    \ \ "chain": "ropsten"  
    }  



### Output ports:

* __NFT data__: ``blockchain/moralis/NFT data``
    Sends a list of NFT transfers as returned by the Moralis API



* __response__: 
    ```
    {"status" :number, "headers" :{string: string}, "data" :`blockchain/moralis/NFT data response`}
    ```

    Sends the entire response from the Moralis API, including status and header.



* __error__: `{"error" :string}`


