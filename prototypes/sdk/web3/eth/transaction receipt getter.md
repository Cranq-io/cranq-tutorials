---
description: [sdk/web3/eth]
---

# Transaction receipt getter

Sends receipt of a transaction by transaction hash.

Example:
1. {
  "transaction_hash": "0x9fc76417374aa880d4449a1f7f31ec597f00b1f6f3dd2d66f4c9c6c445836d8b",
 "provider": "https://speedy-nodes-nyc.moralis.io/1a2b3c4d5e6f1a2b3c4d5e6f/eth/mainnet"
} @0 received via `transaction hash & provider`
2. {
  "status": true,
  "transactionHash": "0x9fc76417374aa880d4449a1f7f31ec597f00b1f6f3dd2d66f4c9c6c445836d8b",
  "transactionIndex": 0,
  "blockHash": "0xef95f2f1ed3ca60b048b4bf67cde2195961e0bba6f70bcbea9a2c4e133e34b46",
  "blockNumber": 3,
  "contractAddress": "0x11f4d0A3c12e86B4b5F39B213F7E19D048276DAe",
  "cumulativeGasUsed": 314159,
  "gasUsed": 30234,
  "logs": [{
    data: '0x7f9fade1c0d57a7af66ab4ead79fade1c0d57a7af66ab4ead7c2c2eb7b11a91385',
    topics: ['0xfd43ade1c09fade1c0d57a7af66ab4ead7c2c2eb7b11a91ffdd57a7af66ab4ead7', '0x7f9fade1c0d57a7af66ab4ead79fade1c0d57a7af66ab4ead7c2c2eb7b11a91385']
    logIndex: 0,
    transactionIndex: 0,
    transactionHash: '0x7f9fade1c0d57a7af66ab4ead79fade1c0d57a7af66ab4ead7c2c2eb7b11a91385',
    blockHash: '0xfd43ade1c09fade1c0d57a7af66ab4ead7c2c2eb7b11a91ffdd57a7af66ab4ead7',
    blockNumber: 1234,
    address: '0xde0B295669a9FD93d5F28D9Ec85E40f4cb697BAe'
}.]
}@0 received via `transaction_receipt`


### Input ports:

* __transaction hash & provider__: `{"transaction_hash" :string, "provider" :string}`

    Receives transaction hash & web3 provider.
    
    Example:
    {
      "transaction_hash": "0x9fc76417374aa880d4449a1f7f31ec597f00b1f6f3dd2d66f4c9c6c445836d8b",
     "provider": "https://speedy-nodes-nyc.moralis.io/1a2b3c4d5e6f1a2b3c4d5e6f/eth/mainnet"
    }
    

### Output ports:

* __transaction_receipt__: 
    ```
    {"status" :boolean, "transactionHash" :string, "transactionIndex" :number, "from" :string, "to" :string, "blockHash" :string, "blockNumber" :number, "contractAddress" :string, "cumulativeGasUsed" :number, "gasUsed" :number, "logs" :{"data" :string, "topics" :string[], "logIndex" :number, "transactionIndex" :number, "transactionHash" :string, "blockHash" :string, "blockNumber" :number, "address" :string}[]}
    ```

    Sends the transaction receipt.
    
    More: https://web3js.readthedocs.io/en/v1.7.1/web3-eth.html#gettransactionreceipt
    
    Example:
    {
      "status": true,
      "transactionHash": "0x9fc76417374aa880d4449a1f7f31ec597f00b1f6f3dd2d66f4c9c6c445836d8b",
      "transactionIndex": 0,
      "blockHash": "0xef95f2f1ed3ca60b048b4bf67cde2195961e0bba6f70bcbea9a2c4e133e34b46",
      "blockNumber": 3,
      "contractAddress": "0x11f4d0A3c12e86B4b5F39B213F7E19D048276DAe",
      "cumulativeGasUsed": 314159,
      "gasUsed": 30234,
      "logs": [{
        data: '0x7f9fade1c0d57a7af66ab4ead79fade1c0d57a7af66ab4ead7c2c2eb7b11a91385',
        topics: ['0xfd43ade1c09fade1c0d57a7af66ab4ead7c2c2eb7b11a91ffdd57a7af66ab4ead7', '0x7f9fade1c0d57a7af66ab4ead79fade1c0d57a7af66ab4ead7c2c2eb7b11a91385']
        logIndex: 0,
        transactionIndex: 0,
        transactionHash: '0x7f9fade1c0d57a7af66ab4ead79fade1c0d57a7af66ab4ead7c2c2eb7b11a91385',
        blockHash: '0xfd43ade1c09fade1c0d57a7af66ab4ead7c2c2eb7b11a91ffdd57a7af66ab4ead7',
        blockNumber: 1234,
        address: '0xde0B295669a9FD93d5F28D9Ec85E40f4cb697BAe'
    }.]
    }
    


* __error__: `{"error" :string}`

