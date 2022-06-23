# Request dispatcher

[apis/firebase/rtdb/rest]

Dispatches an HTTP request for running a query in a Firebase Realtime Database via its REST API.

https://firebase.google.com/docs/reference/rest/database

### Input ports:

* __query context__: `any`
    idToken
    dbUrl



* __method__: `any`
    HTTP method as required by the Firebase Realtime Database REST API.
    
    https://firebase.google.com/docs/reference/rest/database



* __path__: `any`
    Identifies data entry that the query will interact with.



* __data__: `any`
    Data to be sent via the HTTP request. Usually data to be set or updated.



### Output ports:

* __data__: `{string: any}`


* __error__: `string`


* __query context__: `any`
    idToken
    dbUrl



