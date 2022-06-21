# Login & query

[examples/apis/firebase/rtdb/rest]

Demonstrates basic authentication and querying in a Firebase Realtime Database. Requires an API key and a database URL. (Obtained from the Firebase console's "Project Overview" and "Realtime Database" tabs.)

For the example to work the Firebase project must allow anonymous login and database rules must be set up as follows:

{
  "rules": {
    ".read": false,
    ".write": false,
    "$user_id": {
      ".read": "$user_id === auth.uid",
      ".write": "$user_id === auth.uid"
    }
  }
}

### Input ports:

* __API key__: _any_



* __DB URL__: _any_



### Output ports:

* __data__: _any_

    Sends forwarded data.



* __error__: _any_

    Sends forwarded data.



