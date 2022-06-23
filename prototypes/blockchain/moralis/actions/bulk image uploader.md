# Bulk image uploader

[blockchain/moralis/actions]

Uploads multiple images and place them in a folder directory and stores the ipfs URLs in the state.

Example:
1. {}@0 received via `state`
2. {
  "get-names": {
    "cwd": "./nft",
    "result-path": "image-names",
    "message": "Reading list of images...",
    "directory-path": "nft/batch-images"
  },
  "build-paths": {
    "params": {
      "cwd": "./nft",
      "result-path": "image-paths",
      "message": "Constructing image paths...",
      "base-path": "nft/batch-images"
    },
    "mapping": {
      "child-paths": "image-names"
    }
  },
  "build-data": {
    "params": {
      "cwd": "./nft",
      "result-path": "image-upload-data",
      "message": "Preparing image upload data..."
    },
    "mapping": {
      "image-paths": "image-paths"
    }
  },
  "upload": {
    "params": {
      "cwd": "./nft",
      "result-path": "image-urls",
      "message": "Uploading images to IPFS...",
      "api-key": "API_KEY"
    },
    "mapping": {
      "folder-upload-data": "image-upload-data"
    }
  }
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
  ]
}@0 sent via `state`

### Input ports:

* __state__: `any`

    Receives script state.
    
    Example:
    {}


* __params__: 
    ```
    {"get-names" :{"cwd-path" :(string or number)[], "result-path" :string, "message" :string, "directory-path" :string}, "build-paths" :{"cwd" :string, "result-path" :string, "message" :string, "child-paths" :string[], "base-path" :string}, "build-data" :{"cwd" :string, "result-path" :string, "message" :string, "image-paths" :string[]}, "upload" :{"cwd" :string, "result-path" :string, "message" :string, "folder-upload-data" :any, "api-key" :string}}
    ```

    Recieves upload images params.
    
    Example:
    {
      "get-names": {
        "cwd": "./nft",
        "result-path": "image-names",
        "message": "Reading list of images...",
        "directory-path": "nft/batch-images"
      },
      "build-paths": {
        "params": {
          "cwd": "./nft",
          "result-path": "image-paths",
          "message": "Constructing image paths...",
          "base-path": "nft/batch-images"
        },
        "mapping": {
          "child-paths": "image-names"
        }
      },
      "build-data": {
        "params": {
          "cwd": "./nft",
          "result-path": "image-upload-data",
          "message": "Preparing image upload data..."
        },
        "mapping": {
          "image-paths": "image-paths"
        }
      },
      "upload": {
        "params": {
          "cwd": "./nft",
          "result-path": "image-urls",
          "message": "Uploading images to IPFS...",
          "api-key": "API_KEY"
        },
        "mapping": {
          "folder-upload-data": "image-upload-data"
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
      ]
    }

