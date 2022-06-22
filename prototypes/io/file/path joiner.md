# Path joiner

[io/file]

Joins the specified relative path to a base path in an operating system-specific manner.

Example:
1. "/home/user1/" received on `base`
2. "dir1/foo.txt" received on `relative`
3. "/home/user1/dir1/foo.txt" sent on `joined`

### Input ports:

* __base__: _string_

    Receives the base path to concatenate onto.
    
    Example:
    "/home/user1/"
    
    (To keep the application portable use "/" as path separator.)



* __relative__: _string_

    Receives the path relative to `base`.
    
    Example:
    "dir1/foo.txt"
    
    (To keep the application portable use "/" as path separator.)



### Output ports:

* __joined__: _string_

    Sends the resulting path.
    
    Example:
    "/home/user1/dir1/foo.txt"


