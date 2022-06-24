---
description: [io/file]
---

# JSON reader

Reads a JSON file from the specified path and outputs its content.

Example (success):
1. "/home/user1/dir1/foo.txt"@0 received on `path`
2. {
  "foo": 1,
  "bar": 2,
  "foobar": [1,2]
}@0 sent on `text`

Example (failure):
1. "/home/user1/dir1/foo.txt"@0 received on `path`
2. 
- "/home/user1/dir1/foo.txt"@0 sent on `bounced`
- {
  "error": "Error: ENOENT: no such file or directory, open '/home/user1/dir1/foo.txt'"
}@0 sent on `error`

### Input ports:

* __path__: ` string `

    Receives the path of the file to read content of as JSON.
    
    Example:
    "/home/user1/dir1/foo.json"
    
    (To keep the application portable use "/" as path separator.)

### Output ports:

* __data__: ` {string: any} `

    Sends the parsed JSON content read from the file specified by `path`.
    
    Example:
    {
      "foo": 1,
      "bar": 2,
      "foobar": [1,2]
    }
    


* __bounced__: ` string `

    Sends the path if the operation has failed.
    
    Example:
    "/home/user1/dir1/foo.json"


* __error__: ` {"error" :string} `

    Sends error information if the operation has failed.
    
    Example (file access error): 
    {
      "error": "Error: ENOENT: no such file or directory, open '/home/user1/dir1/foo.txt'"
    }
    
    Example (json parse error):
    {
      "error": "SyntaxError: Unexpected token } in JSON at position 45"
    }

