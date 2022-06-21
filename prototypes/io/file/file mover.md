# File mover

[io/file]

Moves a file specified by the path in `source` to the path in `destination`.

Example (success): 
1. "home/user1/dir1/foo.txt"@0 received on `source`
2. "home/user1/dir2/bar.txt"@0 received on `destination`
3. { 
source: "/home/user1/dir1/foo.txt", 
destination: "home/user1/dir2/bar.txt"
}@ sent on `moved`

Example (failure): 
1. "home/user1/dir1/foo.txt"@0 received on `source`
2. "home/user1/dir2/bar.txt"@0 received on `destination`
3. 
- { 
source: "/home/user1/dir1/foo.txt", 
destination: "home/user1/dir2/bar.txt"
}@0 sent on `bounced`
- {
  "error": "Error: ENOENT: no such file or directory, rename 'home/user1/dir1/foo.txt' -> 'home/user1/dir2/bar.txt'"
}@0 sent on `error`

### Input ports:

* __source__: _string_

    Receives the path of the source file to move.
    
    Example:
    "/home/user1/dir1/foo.txt"
    
    (To keep the application portable use "/" as path separator.)



* __destination__: _string_

    Receives the path of the desired target file.
    
    Example:
    "/home/user1/dir2/bar.txt"
    
    (To keep the application portable use "/" as path separator.)



### Output ports:

* __bounced__: _{"source" :string, "destination" :string}_

    Sends synced parameters if operation has failed.
    
    Example:
    { 
      source: "/home/user1/dir1/foo.txt", 
      destination: "/home/user1/dir2/bar.txt"
    }



* __moved__: _{"source" :string, "destination" :string}_

    Sends synced parameters if operation has succeeded.
    
    Example:
    { 
      source: "/home/user1/dir1/foo.txt", 
      destination: "/home/user1/dir2/bar.txt"
    }



* __error__: _{"error" :string}_

    Sends error information if the operation has failed.
    
    Example: 
    {
      "error": "Error: ENOENT: no such file or directory, rename '/home/user1/dir1/foo.txt' -> '/home/user1/dir2/bar.txt'"
    }



