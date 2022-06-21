# Contract file creator

[blockchain/ethereum/actions]

Creates the smart contract as file based on the parameters.

### Input ports:

* __params__: _{"cwd" :string, "contract" :"single-nft", "single-nft" :{"contract-name" :string, "token-name" :string, "token-symbol" :string}, "result-path" :string, "message" :string}_

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



* __state__: _any_

    Receives script state.



### Output ports:

* __state__: _any_

    Sends updated script state.



