# Path tester

[io/file]

Determines whether a file or directory exists under the specified path.

Example: 
1. "/home/user1/dir1/foo.txt"@0 received on `path`
2. true@0 sent on `exists`

### Input ports:

* __path__: `string`

    Receives the path to test whether it exists or not.
    
    Example:
    Example:
    - "/home/user1/dir1"
    - "/home/user1/dir1/foo.txt"
    
    (To keep the application portable use "/" as path separator.)

### Output ports:

* __exists__: `boolean`

    Sends boolean value that indicates whether a file or directory exists under the specified path.
    
    Example:
    true

