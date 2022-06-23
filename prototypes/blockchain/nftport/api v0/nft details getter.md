# NFT details getter

[blockchain/nftport/api v0]

### Input ports:

* __API key__: `string`


* __contract address__: `string`


* __token ID__: `string`


* __params__: 
    ```
    {optional "chain" :("ethereum" or "polygon"), optional "refresh_metadata" :boolean}
    ```



### Output ports:

* __NFT__: 
    ```
    {"chain" :("ethereum" or "polygon"), "contract_address" :string, "token_id" :string, "metadata_url" :string, "metadata" :{"attributes" :{"trait_type" :string, "value" :string}[], "description" :string, "external_url" :string, "image" :string, "name" :string, "properties" :{string: any}}, "file_information" :{string: any}, "file_url" :string, "cached_file_url" :string, "mint_date" :string, "updated_date" :string}
    ```



* __response__: 
    ```
    {"status" :number, "headers" :{string: string}, "body" :any}
    ```



* __error__: `{"error" :string}`


