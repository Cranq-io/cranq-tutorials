---
description: [io/file]
---

# Directory lister (paths)

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

* __path__: ` string `

    Receives the path of the directory to list the content of.
    
    Example:
    "/home/user1/dir1"
    
    (To keep the application portable use "/" as path separator.)

### Output ports:

* __child paths__: ` string[] `

    Sends the path of files & directories under the specified path.
    
    Example:
    [
      "/home/user1/dir1/foo.txt",
      "/home/user1/dir1/subdir1"
    ]


* __bounced__: ` string `

    Sends the path if the operation has failed.
    
    Example:
    "/home/user1/dir1"


* __error__: ` {"error" :string} `

    Sends error information if the operation has failed.
    
    Example: 
    {
      "error": "Error: ENOENT: no such file or directory, scandir 'home/user1'"
    }

