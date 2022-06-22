# File tester

[io/file]

Determines whether the the specified path points to a file.

Example:
1. "/home/user1/dir1/foo.txt"@0 received on `path`
2. true sent on `is file`

### Input ports:

* __path__: _string_

    Receives the path to test whether it is a file or not.
    
    Example:
    "/home/user1/dir1/foo.txt"
    
    (To keep the application portable use "/" as path separator.)



### Output ports:

* __is file__: _boolean_

    Boolean value that indicates, whether the specified path is a file.
    
    Example:
    true


