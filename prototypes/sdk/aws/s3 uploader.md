# S3 uploader

[sdk/AWS]

### Input ports:

* __session id__: `string`

    Receives the id of the S3 session.
    
    Example: 
    "s3-session-id"


* __bucket name__: `string`

    Receives the name of the S3 bucket to upload to.
    
    Example: 
    "buckat-name"


* __file name__: `any`

    Receives the name of the file  to be uploaded.
    
    Example: 
    "test.tx"


* __file content__: `any`

    Receives the content of the file  to be uploaded.
    
    Example: 
    "test content"

### Output ports:

* __done__: 
    ```
    {"ETag" :string, "Location" :string, "key" :string, "Key" :string, "Bucket" :string}
    ```

    Sent the data about the successful upload.
    
    Example:
    {
      "ETag": "\"7c36f14325954cd6cf996f8ee1261d56\"",
      "Location": "https://bucket-name.s3.amazonaws.com/test.txt",
      "key": "test.txt",
      "Key": "test.txt",
      "Bucket": "bucket-name"
    } 


* __error__: `{"error" :string}`

