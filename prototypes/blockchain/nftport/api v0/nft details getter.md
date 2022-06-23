# NFT details getter

[blockchain/nftport/api v0]

### Input ports:

* __API key__: _string_



* __contract address__: _string_



* __token ID__: _string_



* __params__: _{optional "chain" :("ethereum" or "polygon"), optional "refresh_metadata" :boolean}_



### Output ports:

* __NFT__: _{"chain" :("ethereum" or "polygon"), "contract_address" :string, "token_id" :string, "metadata_url" :string, "metadata" :{"attributes" :{"trait_type" :string, "value" :string}[], "description" :string, "external_url" :string, "image" :string, "name" :string, "properties" :{string: any}}, "file_information" :{string: any}, "file_url" :string, "cached_file_url" :string, "mint_date" :string, "updated_date" :string}_



* __response__: _{"status" :number, "headers" :{string: string}, "body" :any}_



* __error__: _{"error" :string}_



