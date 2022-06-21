# Authenticator

[sdk/google/spreadsheet]

Authenticates the service user to use google spreadsheet drive.

Example:
1. `session Id` receives "spreadsheet_session"@0 
2. `email` receives  "email@email.com"@0
3. `key` receives "TopSecretKey"@0
4. `done` sends null@0 

### Input ports:

* __session Id__: _string_

    Receives the session id of the spreadsheet action.
    
    Example: 
    "spreadsheet_session"



* __email__: _string_

    Receives the email address of the service account.
    
    Example: 
    "email@email.com"



* __key__: _string_

    Receives the private key of the service account.
    
    Example: 
    "TopSecretKey!"



### Output ports:

* __done__: _null_

    Sends null if the action was successful.
    
    Example:
    null



* __error__: _{"error" :string}_

    Sends the error which happened during the execution of the action.
    
    Example:.
    {error: "Something went wrong!"}



