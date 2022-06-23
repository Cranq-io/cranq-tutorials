---
description: apis/firebase/rtdb/rest]
---

# Data pusher

Adds a new data entry to a Firebase Realtime Database under 'parent path'.
Returns the path of the new entry.

### Input ports:

* __query context__: `any`

    idToken
    dbUrl


* __parent path__: `any`

    Identifies parent data entry that will contain the new entry.
    
    type: string[]


* __data__: `any`

### Output ports:

* __path__: `any`

    Identifies data actually written.
    
    type: string[]


* __data__: `any`


* __error__: `any`


* __query context__: `any`

    idToken
    dbUrl

