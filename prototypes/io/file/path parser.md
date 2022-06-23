---
description: [io/file]
---

# Path parser

Parses a file system path into its components.

Example:
1. "/home/user1/dir1/foo.txt"@0 received on `path`
2. {
  "directory": "/home/user1/dir1",
  "basename": "foo",
  "extension": ".txt"
}@0 sent on `components`

### Input ports:

* __path__: `string`

    Receives the path to parse.
    
    Example:
    - "/home/user1/dir1/foo.txt"
    - "C:/Users/User1/dir1/foo.txt"
    
    (To keep the application portable use "/" as path separator.)

### Output ports:

* __components__: 
    ```
    {"directory" :string, "basename" :string, "extension" :string}
    ```

    Sends the resulting path components.
    
    Example:
    - {
      "directory": "/home/user1/dir1",
      "basename": "foo",
      "extension": ".txt"
    }
    - {
      "directory": "C:/Users/User1/dir1",
      "basename": "foo",
      "extension": ".txt"
    }

