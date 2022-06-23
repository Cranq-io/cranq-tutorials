---
description: system]
---

# Simple command runner

### Input ports:

* __command__: `string`

    Command to be executed. Must be valid in the context of the current OS.
    
    It's recommended to verify the OS before attempting to execute.


* __cwd__: `string`

### Output ports:

* __success__: `boolean`

