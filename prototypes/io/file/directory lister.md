# Directory lister

[io/file]

Non-recursively lists the names of files & directories under the specified path.

Example (success): 
1. "/home/user1/dir1"@0 received on `path`
2. [ "foo.txt", "bar.txt" ]@0 sent on `child names`

Example (failure): 
1. "/home/user1/dir1"@0 received on `path`
2. 
- "/home/user1/dir1"@0 sent on `bounced`
- {
  "error": "Error: ENOENT: no such file or directory, scandir '/home/user1/dir1'"
}@0 sent on `error`

### Input ports:

* __path__: _string_

    Receives the path of the directory to list the content of.
    
    Example:
    "/home/user1/dir1"
    
    (To keep the application portable use "/" as path separator.)



### Output ports:

* __child names__: _string[]_

    Sends the names of files & directories under the specified path.
    
    Example:
    [
      "foo.txt",
      "subdir1"
    ]



* __bounced__: _string_

    Sends the path if the operation has failed.
    
    Example:
    "/home/user1/dir1"



* __error__: _{"error" :string}_

    Sends error information if the operation has failed.
    
    Example: 
    {
      "error": "Error: ENOENT: no such file or directory, scandir '/home/user1/dir1'"
    }



