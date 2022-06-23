---
description: [sdk/google/drive]
---

# Authenticated spreadsheet creator

Authenticates the service user and creates new spreadsheet on the given shared folder.

Example:
1. `session Id` receives "drive_session"@0 
2. `auth data` receives {
  "email": "email@email.com",
  "key": "TopSecretKey!"
}@0 
3. `create spreadsheet data` receives {
  "file meta data": {
    "name": "Test!",
    "driveId": "0AFITUOLHhs3T_ID",
    "corpora": "drive",
    "parents": [
      "1_ghBRrDju9oMNSy8DqqNtOEfDRIVE_Id"
    ]
  },
  "supports all drives": true
}@0
4. `done` sends {"fileid": "1_ewweewweFileID"}@0 

### Input ports:

* __session Id__: `string`

    Receives the session id of the drive action.
    
    Example: 
    "drive_session"


* __auth data__: `{"email" :string, "key" :string}`

    Receives the authentication data of service account.
    
    Example: 
    {
      "email": "email@email.com",
      "key": "TopSecretKey!"
    }
    


* __create spreadsheet data__: 
    ```
    {"file meta data" :{string: any}, "supports all drives" :boolean}
    ```

    Receives the data of the spreadsheet.
    
    
    Example:
    {
      "file meta data": {
        "name": "Test!",
        "driveId": "0AFITUOLHhs3T_ID",
        "corpora": "drive",
        "parents": [
          "1_ghBRrDju9oMNSy8DqqNtOEfDRIVE_Id"
        ]
      },
      "supports all drives": true
    }
    

### Output ports:

* __done__: `{"fileid" :string}`

    Sends the generated fileid.
    
    Eg.
    {"fileid": "1_ewweewweFileID"}


* __error__: `{"error" :string}`

    Sends the error which happened during the execution of the action.
    
    Example:.
    {error: "Something went wrong!"}

