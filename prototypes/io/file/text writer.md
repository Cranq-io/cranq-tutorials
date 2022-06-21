# Text writer

[io/file]

Writes the input text to the specified path as a text file.

### Input ports:

* __path__: _string_

    Receives the path of the file to write the specified text to.
    
    Example:
    "/home/user1/dir1/foo.txt"
    
    (To keep the application portable use "/" as path separator.)



* __text__: _string_

    Receives the text to write to the specified file. (Will overwrite existing content of the file if exists!)
    
    Example:
    "Hello World"



### Output ports:

* __bounced__: _string_

    Sends synced parameters if operation has failed.
    
    Example:
    { 
      path: "/home/user1/dir1/foo.txt", 
      text: "Hello World"
    }



* __written__: _null_

    Sends synced parameters if operation has succeeded..
    
    Example:
    { 
      path: "/home/user1/dir1/foo.txt", 
      text: "Hello World"
    }



* __error__: _{"error" :string}_

    Sends error information if the operation has failed.
    
    Example: 
    {
      "error": "Error: ENOENT: no such file or directory, open '/home/user1/dir1/foo.txt'"
    }



