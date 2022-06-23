# File renamer

[io/file]

Renames a file specified by the path in `source path` to the new file name in `new name`.

Example (success): 
1. "home/user1/foo.txt"@0 received on `source path`
2. "bar.txt"@0 received on `new name`
3. { 
source: "/home/user1/dir1/foo.txt", 
destination: "/home/user1/dir1/bar.txt"
}@ sent on `renamed`

Example (failure): 
1. "/home/user1/foo.txt"@0 received on `source path`
2. "bar.txt"@0 received on `new name`
3. 
- { 
source: "/home/user1/dir1/foo.txt", 
destination: "/home/user1/dir1/bar.txt"
}@0 sent on `bounced`
- {
  "error": "Error: ENOENT: no such file or directory, rename '/home/user1/dir1/foo.txt' -> '/home/user2/dir1/bar.txt'"
}@0 sent on `error`

### Input ports:

* __source path__: `string`
    Receives the path of the file to rename.
    
    Example:
    "/home/user1/dir1/foo.txt"
    
    (To keep the application portable use "/" as path separator.)



* __new name__: `string`
    Receives the desired new file name.
    
    Example:
    "bar.txt"



### Output ports:

* __bounced__: `any`
    Sends synced parameters if operation has failed.
    
    Example:
    { 
      source: "/home/user1/dir1/foo.txt", 
      destination: "/home/user1/dir1/bar.txt"
    }



* __renamed__: `any`
    Sends synced parameters if operation has succeeded.
    
    Example:
    { 
      source: "/home/user1/dir1/foo.txt", 
      destination: "/home/user1/dir1/bar.txt"
    }



* __error__: `{"error" :string}`
    Sends error information if the operation has failed.
    
    Example: 
    {
      "error": "Error: ENOENT: no such file or directory, rename '/home/user1/dir1/foo.txt' -> '/home/user1/dir1/bar.txt'"
    }



