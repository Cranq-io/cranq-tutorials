---
description: [io/file]
---

# Directory creator

Creates an empty directory under the specified path

Example:
1. "/home/user1/newdir"@0 received on `path`
2/a. "/home/user1/newdir"@0 sent on `created` if directory has been successfully created
2/b. "/home/user1/newdir"@0 sent on `bounced` if any error occured during directory creation

### Input ports:

* __path__: ` string `

    Receives the path of the  directory to create.
    
    Example:
    "/home/user1/newdir"
    
    (To keep the application portable use "/" as path separator.)

### Output ports:

* __created__: ` string `

    Sends the path if the operation has succeeded.
    
    Example:
    "/home/user1/newdir"
    
    


* __bounced__: ` string `

    Sends the path if the operation has failed.
    
    Example:
    "/home/user1/newdir"


* __error__: ` {"message" :string} `

    Sends error information if the operation has failed.
    
    Example: 
    {
      "message": "ENOENT: no such file or directory, mkdir '/home/user1/newdir'"
    }

