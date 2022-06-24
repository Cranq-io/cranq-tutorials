---
description: [blockchain/ethereum/actions]
---

# NFT minter

### Input ports:

* __state__: ` any `


* __params__: 
    ```
    {"install-dependencies" :{"install-web3" :{"cwd" :(string or number)[], "result-path" :string, "message" :string, "command" :string}, "install-dotenv" :{"cwd" :(string or number)[], "result-path" :string, "message" :string, "command" :string}}, "create-files" :{"write-api-url" :{"cwd" :string, "result-path" :string, "message" :string, "name" :string, "value" :string, "append" :boolean}, "write-private-key" :{"cwd" :string, "result-path" :string, "message" :string, "name" :string, "value" :string, "append" :boolean}, "write-public-key" :{"cwd" :string, "result-path" :string, "message" :string, "name" :string, "value" :string, "append" :boolean}, "create-mint-script" :{"cwd" :string, "result-path" :string, "message" :string, "contract-address" :string, "contract-name" :string, "token-uri" :string, "create-file" :string}}, "run-script" :{"cwd" :string, "result-path" :string, "message" :string, "command" :string, "regex" :string}}
    ```

### Output ports:

* __state__: ` any `

