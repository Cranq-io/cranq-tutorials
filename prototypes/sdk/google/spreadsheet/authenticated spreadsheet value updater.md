# Authenticated spreadsheet value updater

[sdk/google/spreadsheet]

Authenticates the service user and  updates dedicated spreadsheet.

Example:
1. `session Id` receives "spreadsheet_session"@0 
2. `auth data` receives {
  "email": "email@email.com",
  "key": "TopSecretKey!"
}@0 
3. `spreadsheet Id` "1_ewweewweFileID"@0
4. `update data` receives {
  "update meta data": {
    "range": "Sheet1!A1:B10"
  },
  "values": [
    ["A1 value", "B1 value"],
    ["A2 value", "B2 value"]
  ]
}}@0 
5. `done` sends null@0 

### Input ports:

* __session Id__: _string_

    Receives the session id of the spreadsheet action.
    
    Example: 
    "spreadsheet_session"



* __auth data__: _{"email" :string, "key" :string}_

    Receives the authentication data of service account.
    
    Example: 
    {
      "email": "email@email.com",
      "key": "TopSecretKey!"
    }
    



* __spreadsheet Id__: _string_

    Receives the id of the spreadsheet to be updated.
    
    Example:
    "1_ewweewweFileID"



* __update data__: _{"update meta data" :{string: any}, "values" :any[][]}_

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



