# Smart contract deployer

[blockchain/ethereum/actions]

### Input ports:

* __state__: _any_



* __params__: _{"create-folders" :{"create-working-folder" :{"cwd" :string, "result-path" :string, "message" :string, "path" :string}, "create-contract-folder" :{"cwd" :string, "result-path" :string, "message" :string, "path" :string}, "create-scripts-folder" :{"cwd" :string, "result-path" :string, "message" :string, "path" :string}}, "install-dependencies" :{"init-package" :{"cwd" :(string or number)[], "result-path" :string, "message" :string, "command" :string}, "install-hardhat" :{"cwd" :(string or number)[], "result-path" :string, "message" :string, "command" :string}, "install-dotenv" :{"cwd" :(string or number)[], "result-path" :string, "message" :string, "command" :string}, "install-ether" :{"cwd" :(string or number)[], "result-path" :string, "message" :string, "command" :string}, "install-contracts" :{"cwd" :(string or number)[], "result-path" :string, "message" :string, "command" :string}}, "create-files" :{"write-api-url" :{"cwd" :string, "result-path" :string, "message" :string, "name" :string, "value" :string, "append" :boolean}, "write-private-key" :{"cwd" :string, "result-path" :string, "message" :string, "name" :string, "value" :string, "append" :boolean}, "create-hardhat-config" :{"cwd" :string, "path" :string, "network" :string, "result-path" :string, "message" :string}, "create-contract" :{"cwd" :string, "contract" :"single-nft", "single-nft" :{"contract-name" :string, "token-name" :string, "token-symbol" :string}, "result-path" :string, "message" :string}, "prepare-write-deploy-params" :{string: string}, "write-deploy" :{"cwd" :string, "path" :string, "contract-name" :string, "result-path" :string, "message" :string}}, "deploy-contract" :{"compile-contract" :{"cwd" :(string or number)[], "result-path" :string, "message" :string, "command" :string}, "deploy-contract" :{"cwd" :string, "result-path" :string, "message" :string, "network" :string, "regex" :string}, "prepare-verify-contract-params" :{string: string}, "verify-contract" :{"contract-address" :string, "cwd" :string, "result-path" :string, "message" :string}}}_



### Output ports:

* __state__: _any_

    Example: 
    {
      "working-folder-created": true,
      "hardhat": {
        "contracts-folder-created": true,
        "scripts-folder-created": true,
        "installed": true,
        "config-created": true,
        "deploy-script-created": true,
        "contract-compiled": true,
        "contract-deployed": "0xC6041039D24BF7BC467Ee51423347d6015bdC68C"
      },
      "npm": {
        "package-initialized": true
      },
      "dotenv": {
        "installed": true
      },
      "etherjs": {
        "installed": true
      },
      "openzeppelin": {
        "contracts": {
          "installed": true
        }
      },
      ".env": {
        "alchemy": {
          "api-url-written": true
        },
        "metamask": {
          "private-key-written": true
        }
      },
      "blockchain": {
        "erc721": {
          "contract": {
            "contract-created": "My_Test_NFT_Contract"
          }
        }
      }
    } @start



