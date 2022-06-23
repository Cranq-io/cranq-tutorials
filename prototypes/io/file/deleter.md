---
description: io/file]
---

# Deleter

Deletes a file or directory specified by the path input.

Example (success):
1. "/home/user1/dir1/foo.txt"@0 received on `path`
2 false@0 received on `recursive`
3. { path: "/home/user1/dir1/foo.txt", recursive: false } sent on `deleted`

Example (failure): 
1. "/home/user1/dir1"@0 received on `path`
2 true@0 received on `recursive`
3.
- { path: "/home/user1/dir1", recursive: true } sent on `bounced`
- {
  "error": "Error: ENOENT: no such file or directory, stat '/home/user1/dir1'"
} sent on `error`

### Input ports:

* __path__: `string`

    Receives the path of the file or directory to delete.
    
    Example:
    - "/home/user1/dir1"
    - "/home/user1/dir1/foo.txt"
    
    (To keep the application portable use "/" as path separator.)


* __recursive__: `boolean`

    Receives boolean flag which, when set, performs a recursive delete of all files & folders under the specified path.
    
    Example:
    false
    
    (Be VERY cautious with recursive delete as it may cause irreversible harm on the host running the application if applied to a wrong path!)

### Output ports:

* __bounced__: `{"path" :string, "recursive" :boolean}`

    Sends synced parameters if operation has failed.
    
    Example:
    - { path: "/home/user1/dir1", recursive: true }
    - { path: "/home/user1/dir1/foo.txt", recursive: false }


* __deleted__: `{"path" :string, "recursive" :boolean}`

    Sends synced parameters if the operation has succeeded.
    
    Example:
    - { path: "/home/user1/dir1", recursive: true }
    - { path: "/home/user1/dir1/foo.txt", recursive: false }


* __error__: `{"error" :string}`

    Sends error information if the operation has failed.
    
    Example: 
    {
      "error": "Error: ENOENT: no such file or directory, stat 'home/user1'"
    }

