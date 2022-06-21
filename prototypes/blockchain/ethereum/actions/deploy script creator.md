# Deploy script creator

[blockchain/ethereum/actions]

Creates the deploy script to deploy the contract using Hardhat.

### Input ports:

* __params__: _{"cwd" :string, "path" :string, "contract-name" :string, "result-path" :string, "message" :string}_

    {
      "cwd": string, // the working directory
      "path": string, // the path to write the deploy script to
      "contract-name": string, // the name of the contract to deploy
      "result-path": string, // the path in the state to write the result to
      "message": string // the message to print on the console
    }



* __state__: _any_

    Receives script state.



### Output ports:

* __state__: _any_

    Sends updated script state.



