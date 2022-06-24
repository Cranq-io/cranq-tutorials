---
description: [io/file]
---

# Text appender

Appends the input text to a file specified on `path`.

Example (success):
1. "/home/user1/dir1/foo.txt"@0 received on `path`
2. "Hello World"@0 received on `text`
3. { 
  path: "/home/user1/dir1/foo.txt", 
  text: "Hello World"
}@0 sent on `written`

Example (failure):
1. "/home/user1/dir1/foo.txt"@0 received on `path`
2. "Hello World"@0 received on `text`
3.
- { 
  path: "/home/user1/dir1/foo.txt", 
  text: "Hello World"
}@0 sent on `bounced`
- {
  "error": "Error: ENOENT: no such file or directory, open '/home/user1/dir1/foo.txt'"
}@0 sent on `error`

### Input ports:

* __path__: ` string `

    Receives the path of the file to append text to.
    
    Example:
    "/home/user1/dir1/foo.txt"
    
    (To keep the application portable use "/" as path separator.)


* __text__: ` string `

    Receives the text to append to the specified file.
    
    Example:
    "Hello World"

### Output ports:

* __bounced__: ` any `

    Sends synced parameters if operation has failed.
    
    Example:
    { 
      path: "/home/user1/dir1/foo.txt", 
      text: "Hello World"
    }


* __written__: ` any `

    Sends synced parameters if operation has succeeded..
    
    Example:
    { 
      path: "/home/user1/dir1/foo.txt", 
      text: "Hello World"
    }


* __error__: ` {"error" :string} `

    Sends error information if the operation has failed.
    
    Example: 
    {
      "error": "Error: ENOENT: no such file or directory, open '/home/user1/dir1/foo.txt'"
    }

