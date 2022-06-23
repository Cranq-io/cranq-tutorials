# Path builder

[io/file]

Constructs an operating system specific path of the specified segments.

Example:
1. {
  "directory": "/home/user1/dir1",
  "basename": "foo",
  "extension": ".txt"
}@0 received on `components`
2. "/home/user1/dir1/foo.txt"@0 sent on `path`

### Input ports:

* __components__: 
    ```
    {"directory" :string, "basename" :string, "extension" :string}
    ```

    Receives the components to build the path from.
    
    Example (Windows): 
    {
      "directory": "C:/Users/User1/dir1",
      "basename": "foo",
      "extension": ".txt"
    }
    
    Example (OSX & *nix): 
    {
      "directory": "/home/user1/dir1",
      "basename": "foo",
      "extension": ".txt"
    }
    
    (To keep the application portable use "/" as path separator.)



### Output ports:

* __path__: `string`
    Sends the resulting path.
    
    Example (Windows):
    "C:/Users/User1/dir1/foo.txt"
    
    Example (OSX & *nix):
    "/home/user1/dir1/foo.txt"



