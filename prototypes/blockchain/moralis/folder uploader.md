---
description: [blockchain/moralis]
---

# Folder uploader

Posts upload file data to  https://deep-index.moralis.io/api/v2/ipfs/uploadFolder endpoint

More: 
https://docs.moralis.io/moralis-server/web3-sdk/ipfs-storage-new

Example:
1. [
    {
      "path": "moralis/logo.jpg",
      "content": "iVBORw0KGgoAAAANSUhEUgAAABgAAAAYCAYAAADgdz34AAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAAApgAAAKYB3X3"
    }
  ]"@0 received via `folder data`  
2. "ffdfdhdhgdjjhggkjcvxc"@0 received via `API key` 
3. [  :"https://ipfs.moralis.io:2053/ipfs/QmVsdDLF8gmZeUCdrqgjXHLZ4VupdvxQaCiCdDvVApmR2o/moralis/logo.jpg" 
]@0 sent via `file URLs`

### Input ports:

* __folder data__: ` {"path" :string, "content" :string}[] `

    Receives moralis post data.
    
    Example:
    [
        {
          "path": "moralis/logo.jpg",
          "content": "iVBORw0KGgoAAAANSUhEUgAAABgAAAAYCAYAAADgdz34AAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAAApgAAAKYB3X3"
        }
      ]


* __API key__: ` string `

    Receives moralis API key.
    
    Example: 
    "ffdfdhdhgdjjhggkjcvxc" 

### Output ports:

* __file URLs__: ` string[] `

    Sends file ipfs URLs.
    
    Example:
     [
    "https://ipfs.moralis.io:2053/ipfs/QmVsdDLF8gmZeUCdrqgjXHLZ4VupdvxQaCiCdDvVApmR2o/moralis/logo.jpg" 
    ]
    


* __error__: ` any `

