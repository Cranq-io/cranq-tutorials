---
description: blockchain/moralis/actions]
---

# Bulk auto-metadata uploader

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
}@ received via `state`
2. {
  "build-data": {
    "cwd": "./nft",
    "result-path": "ipfs.image-metadata",
    "message": "Building metadata for images...",
    "image-urls": [],
    "image-names": []
  },
  "upload": {
    "params": {
      "cwd": "./nft",
      "result-path": "ipfs.metadata-urls",
      "message": "Uploading metadata to IPFS...",
      "api-key": "API_KEY"
    },
    "mapping": {
      "folder-upload-data": "ipfs.image-metadata"
    }
  }
}@0 received via params
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
    {"build-data" :{"cwd" :string, "result-path" :string, "message" :string, "image-urls" :string[], "image-names" :string[]}, "upload" :{"cwd" :string, "result-path" :string, "message" :string, "folder-upload-data" :any, "api-key" :string}}
    ```

    Recieves upload metadata script parameters.
    
    Example:
    {
      "build-data": {
        "cwd": "./nft",
        "result-path": "ipfs.image-metadata",
        "message": "Building metadata for images...",
        "image-urls": [],
        "image-names": []
      },
      "upload": {
        "params": {
          "cwd": "./nft",
          "result-path": "ipfs.metadata-urls",
          "message": "Uploading metadata to IPFS...",
          "api-key": "API_KEY"
        },
        "mapping": {
          "folder-upload-data": "ipfs.image-metadata"
        }
      }
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

