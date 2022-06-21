# Contract files creator

[blockchain/ethereum/actions]

### Input ports:

* __state__: _any_



* __params__: _{"write-api-url" :{"cwd" :string, "result-path" :string, "message" :string, "name" :string, "value" :string, "append" :boolean}, "write-private-key" :{"cwd" :string, "result-path" :string, "message" :string, "name" :string, "value" :string, "append" :boolean}, "create-hardhat-config" :{"cwd" :string, "path" :string, "network" :string, "result-path" :string, "message" :string}, "create-contract" :{"cwd" :string, "contract" :"single-nft", "single-nft" :{"contract-name" :string, "token-name" :string, "token-symbol" :string}, "result-path" :string, "message" :string}, "prepare-write-deploy-params" :{string: string}, "write-deploy" :{"cwd" :string, "path" :string, "contract-name" :string, "result-path" :string, "message" :string}}_



### Output ports:

* __state__: _any_



