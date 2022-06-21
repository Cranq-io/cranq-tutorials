# Data pusher

[apis/firebase/rtdb/rest]

Adds a new data entry to a Firebase Realtime Database under 'parent path'.
Returns the path of the new entry.

### Input ports:

* __query context__: _any_

    idToken
    dbUrl



* __parent path__: _any_

    Identifies parent data entry that will contain the new entry.
    
    type: string[]



* __data__: _any_



### Output ports:

* __path__: _any_

    Identifies data actually written.
    
    type: string[]



* __data__: _any_



* __error__: _any_



* __query context__: _any_

    idToken
    dbUrl



