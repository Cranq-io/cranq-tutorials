# Query context builder

[apis/firebase/rtdb]

Builds a Firebase Realtime Database query context from a Firebase ID token and a database URL (found on the Firebase Realtime Database console) to be passed around among related data querying and manipulation nodes.

### Input ports:

* __ID token__: `string`
    Receives individual fields for syncing.



* __DB URL__: `string`
    Receives individual fields for syncing.



### Output ports:

* __sync context-synced__: `{"ID token" :string, "DB URL" :string}`
    Sends synchronized inputs as a dictionary, indexed by field.



