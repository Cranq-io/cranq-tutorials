# Smart contract deployer (simplified)

[blockchain/ethereum/actions]

Creates and deploys an Ethereum smart contract based on the parameters.
Using Alchemy to interact with the Ethereum network.

Example:
1. 

### Input ports:

* __state__: `any`


* __params__: 
    ```
    {"cwd" :string, "wallet-private-key" :string, "api-key" :string, "etherscan-api-key" :string, "blockchain" :"ethereum", "blockchain-network" :"string", "contract" :"single-nft", "single-nft" :{"contract-name" :string, "token-name" :string, "token-symbol" :string}}
    ```

    Parameters for smart contract creation and deployment:
    
    {
      "cwd": string, // the working directory
      "wallet-private-key": string, // the private key of your Ethereum wallet
      "api-key": string, // the api key of your app on Alchemy used to interact with the Ethereum network
      "contract": "single-nft", // the contract type (only "single-nft" at the moment)
      "single-nft": {  // parameters corresponding to the requested contract type
        "contract-name": string,
        "token-name": string,
        "token-symbol": string
      }
    }

### Output ports:

* __state__: `any`

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

