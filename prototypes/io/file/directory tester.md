# Directory tester

[io/file]

Determines whether the specified path points to a directory.

Example:
1. "/home/user1/dir1"@0 received on `path`
2. true@0 sent on `is directory`

### Input ports:

* __path__: _string_

    Receives the path to test whether it is a directory or not.
    
    Example:
    "/home/user1/dir1"
    
    (To keep the application portable use "/" as path separator.)



### Output ports:

* __is directory__: _boolean_

    Sends boolean value that indicates whether the specified path is a directory.
    
    Example:
    true


