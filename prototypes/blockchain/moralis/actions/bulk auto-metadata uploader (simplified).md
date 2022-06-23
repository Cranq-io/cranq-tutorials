# Bulk auto-metadata uploader (simplified)

[blockchain/moralis/actions]

Builds and uploads images meta data and stores the ipfs URLs in the state.

Example: 
1. {
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
}@0 received via `state`
2. {
  "cwd": "./nft",
  "moralis-api-key": "API_KEY",
  "images-urls" : ["https://ipfs.moralis.io:2053/ipfs/QmVsdDLF8gmZeUCdrqgjXHLZ4VupdvxQaCiCdDvVApmR2o/nft\\batch-images\\logo.jpg"],
  "image-names": ["logo.jpg"]
}@0 received via `params`
3. {
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
  ],
  "ipfs": {
      "image-metadata": [
		  {
			"content": {
			  "description": "Image",
			  "image": "https://ipfs.moralis.io:2053/ipfs/QmVsdDLF8gmZeUCdrqgjXHLZ4VupdvxQaCiCdDvVApmR2o/nft\\batch-images\\logo.jpg",
			  "name": "logo.jpg"
			},
			"path": "logo.jpg"
		  }
	  ],
	  "metadata-urls": [
		"https://ipfs.moralis.io:2053/ipfs/Qmf3QmpGzz5vZ4TkrSJapRwD36f9sQ9zZJUwj6CCmA2bAs/logo.json"
	  ]	
  }
}@0 sent via `state`

### Input ports:

* __state__: `any`
    Receives script state.
    
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



* __params__: 
    ```
    {"cwd" :string, "moralis-api-key" :string, "image-urls" :string[], "image-names" :string[]}
    ```

    Recieves upload metadata script parameters.
    
    Example:
    {
      "cwd": "./nft",
      "moralis-api-key": "API_KEY",
      "image-urls" : ["https://ipfs.moralis.io:2053/ipfs/QmVsdDLF8gmZeUCdrqgjXHLZ4VupdvxQaCiCdDvVApmR2o/nft\\batch-images\\logo.jpg"],
      "image-names": ["logo.jpg"]
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
      ],
      "ipfs": {
          "image-metadata": [
    		  {
    			"content": {
    			  "description": "Image",
    			  "image": "https://ipfs.moralis.io:2053/ipfs/QmVsdDLF8gmZeUCdrqgjXHLZ4VupdvxQaCiCdDvVApmR2o/nft\\batch-images\\logo.jpg",
    			  "name": "logo.jpg"
    			},
    			"path": "logo.jpg"
    		  }
    	  ],
    	  "metadata-urls": [
    		"https://ipfs.moralis.io:2053/ipfs/Qmf3QmpGzz5vZ4TkrSJapRwD36f9sQ9zZJUwj6CCmA2bAs/logo.json"
    	  ]	
      }
    }



