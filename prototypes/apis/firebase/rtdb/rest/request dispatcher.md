# Request dispatcher

[apis/firebase/rtdb/rest]

Dispatches an HTTP request for running a query in a Firebase Realtime Database via its REST API.

https://firebase.google.com/docs/reference/rest/database

### Input ports:

* __query context__: _any_

    idToken
    dbUrl



* __method__: _any_

    HTTP method as required by the Firebase Realtime Database REST API.
    
    https://firebase.google.com/docs/reference/rest/database



* __path__: _any_

    Identifies data entry that the query will interact with.



* __data__: _any_

    Data to be sent via the HTTP request. Usually data to be set or updated.



### Output ports:

* __data__: _{string: any}_



* __error__: _string_



* __query context__: _any_

    idToken
    dbUrl



