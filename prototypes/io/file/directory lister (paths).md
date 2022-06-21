# Directory lister (paths)

[io/file]

Non-recursively lists the paths of files & directories under the specified path.

Example (success): 
1. "/home/user1/dir1"@0 received on `path`
2. [ "/home/user1/dir1/foo.txt", "/home/user1/dir1/bar.txt" ]@0 sent on `child names`

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

* __child paths__: _string[]_

    Sends the path of files & directories under the specified path.
    
    Example:
    [
      "/home/user1/dir1/foo.txt",
      "/home/user1/dir1/subdir1"
    ]



* __bounced__: _string_

    Sends the path if the operation has failed.
    
    Example:
    "/home/user1/dir1"



* __error__: _{"error" :string}_

    Sends error information if the operation has failed.
    
    Example: 
    {
      "error": "Error: ENOENT: no such file or directory, scandir 'home/user1'"
    }



