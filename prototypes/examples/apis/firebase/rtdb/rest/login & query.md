---
description: examples/apis/firebase/rtdb/rest]
---

# Login & query

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

* __API key__: `any`


* __DB URL__: `any`

### Output ports:

* __data__: `any`

    Sends forwarded data.


* __error__: `any`

    Sends forwarded data.

