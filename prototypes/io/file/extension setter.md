# Extension setter

[io/file]

Sets the extension on the received path.

Example:
1. "/home/user1/dir1/foo.txt"@0 received on `path`
2. ".json"@0 received on `extension`
3. "/home/user1/dir1/foo.json"@0 sent on `path`

### Input ports:

* __path__: _string_

    Receives the path to set the extension on.
    
    Example:
    "/home/user1/dir1/foo.txt"
    
    (To keep the application portable use "/" as path separator.)



* __extension__: _string_

    Receives the extension to set on `path`.
    
    Example:
    ".json"



### Output ports:

* __path__: _string_

    Sends the resulting path.
    
    Example:
    "/home/user1/dir1/foo.json"


