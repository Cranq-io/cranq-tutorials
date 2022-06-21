---
description: [blockchain/ethereum/actions]
---

# Deploy script creator

Creates the deploy script to deploy the contract using Hardhat.

### Input ports:

* __params__: 
    ```
    {"cwd" :string, "path" :string, "contract-name" :string, "result-path" :string, "message" :string}
    ```

    {
      "cwd": string, // the working directory
      "path": string, // the path to write the deploy script to
      "contract-name": string, // the name of the contract to deploy
      "result-path": string, // the path in the state to write the result to
      "message": string // the message to print on the console
    }


* __state__: ` any `

    Receives script state.

### Output ports:

* __state__: ` any `

    Sends updated script state.

