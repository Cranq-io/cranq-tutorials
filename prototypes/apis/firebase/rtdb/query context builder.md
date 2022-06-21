# Query context builder

[apis/firebase/rtdb]

Builds a Firebase Realtime Database query context from a Firebase ID token and a database URL (found on the Firebase Realtime Database console) to be passed around among related data querying and manipulation nodes.

### Input ports:

* __ID token__: _string_

    Receives individual fields for syncing.



* __DB URL__: _string_

    Receives individual fields for syncing.



### Output ports:

* __sync context-synced__: _{"ID token" :string, "DB URL" :string}_

    Sends synchronized inputs as a dictionary, indexed by field.



