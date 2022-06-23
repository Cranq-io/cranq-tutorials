# Contract compiler & deployer

[blockchain/ethereum/actions]

Compiles and deploys a smart contract

### Input ports:

* __state__: `any`


* __params__: 
    ```
    {"compile-contract" :{"cwd" :(string or number)[], "result-path" :string, "message" :string, "command" :string}, "deploy-contract" :{"cwd" :string, "result-path" :string, "message" :string, "network" :string, "regex" :string}, "prepare-verify-contract-params" :{string: string}, "verify-contract" :{"contract-address" :string, "cwd" :string, "result-path" :string, "message" :string}}
    ```



### Output ports:

* __state__: `any`


