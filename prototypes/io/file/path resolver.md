# Path resolver

[io/file]

Resolves a file system path into a fully qualified one relative to the current working directory.

Example:
1. "dir1"@0 received on `path`
2. "/home/user1/.cranq/runtime/dir1"@0 sent on `resolved` 
("/home/user1/.cranq/runtime" being the current working directory)

### Input ports:

* __path__: _string_

    Receives the path to resolve to absolute path.
    
    Example:
    - "dir1"
    - "dir1/foo.txt"
    
    (To keep the application portable use "/" as path separator.)
    



### Output ports:

* __resolved__: _string_

    Sends the resolved absolute path.
    
    Example:
    - "/home/user1/.cranq/runtime/dir1"
    - "/home/user1/.cranq/runtime/dir1/foo.txt"


