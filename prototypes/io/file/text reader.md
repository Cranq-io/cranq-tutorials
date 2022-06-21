# Text reader

[io/file]

Reads a text file from the specified path and outputs its content.

Example (success):
1. "/home/user1/dir1/foo.txt"@0 received on `path`
2. "Hello World"@0 sent on `text`

Example (failure):
1. "/home/user1/dir1/foo.txt"@0 received on `path`
2. 
- "/home/user1/dir1/foo.txt"@0 sent on `bounced`
- {
  "error": "Error: ENOENT: no such file or directory, open '/home/user1/dir1/foo.txt'"
}@0 sent on `error`

### Input ports:

* __path__: _string_

    Receives the path of the file to read content of as text.
    
    Example:
    "/home/user1/dir1/foo.txt"
    
    (To keep the application portable use "/" as path separator.)



### Output ports:

* __text__: _string_

    Sends the text content read from the file specified by `path`.
    
    Example:
    "Hello World"



* __bounced__: _string_

    Sends the path if the operation has failed.
    
    Example:
    "/home/user1/dir1/foo.txt"



* __error__: _{"error" :string}_

    Sends error information if the operation has failed.
    
    Example: 
    {
      "error": "Error: ENOENT: no such file or directory, open '/home/user1/dir1/foo.txt'"
    }



