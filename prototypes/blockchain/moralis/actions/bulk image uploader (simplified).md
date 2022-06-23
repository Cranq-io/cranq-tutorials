# Bulk image uploader (simplified)

[blockchain/moralis/actions]

Uploads multiple images  and stores the ipfs URLs in the state.

Example:
1. {}@0 receiced via `state`
2. {
  "cwd": "./nft",
  "images-directory": "nft/batch-images",
  "moralis-api-key": "API_KEY"
}@0 received via `params`
3.{
  "image-names": [
    "logo.jpg"
  ],
  "image-paths": [
    "nft\\batch-images\\logo.jpg"
  ],
  "image-upload-data": [
    {
      "path": "nft\\batch-images\\logo.jpg",
      "content": "iVBORw0KGgoAAAANSUhEUgAAABgAAAAYCAYAAADgdz34AAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAAApgAAAKYB3X3"
    }
  ],
  "image-urls": [
	"https://ipfs.moralis.io:2053/ipfs/QmVsdDLF8gmZeUCdrqgjXHLZ4VupdvxQaCiCdDvVApmR2o/nft\\batch-images\\logo.jpg"
  ]
}@0 sent via `state`

### Input ports:

* __state__: `any`
    Receives script state.
    
    Example:
    {}@0



* __params__: 
    ```
    {"cwd" :string, "images-directory" :string, "moralis-api-key" :string}
    ```

    Recieves upload images script parameters.
    
    Example:
    {
      "cwd": "./nft",
      "images-directory": "nft/batch-images",
      "moralis-api-key": "API_KEY"
    }



### Output ports:

* __state__: `any`
    Sends updated script state.
    
    Example:
    {
      "image-names": [
        "logo.jpg"
      ],
      "image-paths": [
        "nft\\batch-images\\logo.jpg"
      ],
      "image-upload-data": [
        {
          "path": "nft\\batch-images\\logo.jpg",
          "content": "iVBORw0KGgoAAAANSUhEUgAAABgAAAAYCAYAAADgdz34AAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAAApgAAAKYB3X3"
        }
      ],
      "image-urls": [
    	"https://ipfs.moralis.io:2053/ipfs/QmVsdDLF8gmZeUCdrqgjXHLZ4VupdvxQaCiCdDvVApmR2o/nft\\batch-images\\logo.jpg"
      ]
    }



