# Info getter

[io/file]

Reads common file system information of the file or directory, specified by `path`.

Example (success):
1. "/home/user1/dir1/foo.txt"@0 received on `path`
2. {
  "size_bytes": 3128,
  "created": "2021-12-09T15:47:56.441Z",
  "accessed": "2021-12-09T15:47:56.441Z",
  "modified": "2021-12-09T15:47:56.441Z",
  "changed": "2021-12-09T22:08:22.314Z"
}@0 sent on `info`

Example (failure):
1. "/home/user1/dir1/foo.txt"@0 received on `path`
2."/home/user1/dir1/foo.txt"@ sent on `bounced`

### Input ports:

* __path__: `string`
    Receives the path of the file or directory to get information of.
    
    Example:
    - "/home/user1/dir1"
    - "/home/user1/dir1/foo.txt"
    
    (To keep the application portable use "/" as path separator.)



### Output ports:

* __info__: 
    ```
    {"size_bytes" :number, "created" :string, "accessed" :string, "modified" :string, "changed" :string}
    ```

    The resulting file/directory information.
    
    Example:
    {
      "size_bytes": 3128,
      "created": "2021-12-09T15:47:56.441Z",
      "accessed": "2021-12-09T15:47:56.441Z",
      "modified": "2021-12-09T15:47:56.441Z",
      "changed": "2021-12-09T22:08:22.314Z"
    }



* __bounced__: `string`
    Sends the path if the operation has failed.
    
    Example:
    - "/home/user1/dir1"
    - "/home/user1/dir1/foo.txt"



