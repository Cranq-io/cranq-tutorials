---
description: [blockchain/ethereum/actions]
---

# Contract file creator

Creates the smart contract as file based on the parameters.

### Input ports:

* __params__: 
    ```
    {"cwd" :string, "contract" :"single-nft", "single-nft" :{"contract-name" :string, "token-name" :string, "token-symbol" :string}, "result-path" :string, "message" :string}
    ```

    {
      "cwd": string, // the working directory
      "contract": "single-nft", // the contract type
      "single-nft": {  // the parameters specific to the contract type
        "contract-name": string,
        "token-name": string,
        "token-symbol": string
      },
      "result-path": string, // the path in the state to write the result to
      "message": string // the message to print on the console
    }


* __state__: `any`

    Receives script state.

### Output ports:

* __state__: `any`

    Sends updated script state.

