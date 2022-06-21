# S3 uploader

[sdk/AWS]

### Input ports:

* __session id__: _string_

    Receives the id of the S3 session.
    
    Example: 
    "s3-session-id"



* __bucket name__: _string_

    Receives the name of the S3 bucket to upload to.
    
    Example: 
    "buckat-name"



* __file name__: _any_

    Receives the name of the file  to be uploaded.
    
    Example: 
    "test.tx"



* __file content__: _any_

    Receives the content of the file  to be uploaded.
    
    Example: 
    "test content"



### Output ports:

* __done__: _{"ETag" :string, "Location" :string, "key" :string, "Key" :string, "Bucket" :string}_

    Sent the data about the successful upload.
    
    Example:
    {
      "ETag": "\"7c36f14325954cd6cf996f8ee1261d56\"",
      "Location": "https://bucket-name.s3.amazonaws.com/test.txt",
      "key": "test.txt",
      "Key": "test.txt",
      "Bucket": "bucket-name"
    } 



* __error__: _{"error" :string}_



