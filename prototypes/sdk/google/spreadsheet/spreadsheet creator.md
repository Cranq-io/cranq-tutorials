# Spreadsheet creator

[sdk/google/spreadsheet]

Creates google spreadsheet on the given drive/folder.

Example:
1. `auth data` receives {
  "email": "email@email.com",
  "key": "TopSecretKey!"
}@0 
2. `drive data` {
  "file meta data": {
    "name": "Test!",
    "driveId": "0AFITUOLHhs3T_ID",
    "corpora": "drive",
    "parents": [
      "1_ghBRrDju9oMNSy8DqqNtOEfDRIVE_Id"
    ]
  },
  "supports all drives": true
}"@0
3. `spreadsheet data` receives {
  "update meta data": {
    "range": "Sheet1!A1:B10"
  },
  "values": [
    ["A1 value", "B1 value"],
    ["A2 value", "B2 value"]
  ]
}}@0 
4. `done` sends null@0 

### Input ports:

* __auth data__: _{"email" :string, "key" :string}_

    Receives the authentication data of service account.
    
    Example: 
    {
      "email": "email@email.com",
      "key": "TopSecretKey!"
    }



* __drive data__: _{"file meta data" :{string: any}, "supports all drives" :boolean}_

    Receives the data of the drive where the spreadsheet is stored.
    
    
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



* __spreadsheet data__: _{"update meta data" :{string: any}, "values" :any[][]}_

    Receives the spreadsheet metadata.
    
    {
      "update meta data": {
        "range": "Sheet1!A1:B10"
      },
      "values": [
        ["A1 value", "B1 value"],
        ["A2 value", "B2 value"]
      ]
    }
    



### Output ports:

* __done__: _null_

    Sends null if the action was successful.
    
    Example:
    null



* __error__: _{"error" :string}_

    Sends the error which happened during the execution of the action.
    
    Example:.
    {error: "Something went wrong!"}


