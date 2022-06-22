# Spreadsheet creator

[sdk/google/drive]

Creates new spreadsheet on the given shared folder.

Example:
1. `session Id` receives "drive_session"@0 
2. `file meta data` receives  {
  "name": "Test from CRANQ dynamic",
  "parents": [
    "FOLDER_ID"
  ]
}@0
3. `supports all drives` receives false@0
4. `done` sends {"fileid": "1_ewweewweFileID"}@0 

### Input ports:

* __session Id__: _string_

    Receives the session id of the drive action.
    
    Example: 
    "drive_session"



* __file meta data__: _{string: any}_

    Receives the metadata of the spreadsheet creation.
    
    Example in case of shared drive:
    
    {
      "name": "Test from CRANQ dynamic",
      "driveId": "0AFITUOLHhs3TUk9PVA",
      "corpora": "drive",
      "parents": [
        "FOLDER_ID"
      ]
    }
    
    
    Example in case of shared folder:
    
    {
      "name": "Test from CRANQ dynamic",
      "parents": [
        "FOLDER_ID"
      ]
    }



* __supports all drives__: _boolean_

    Receives `supports all drives` parameter whether create should support both drives and shared drives.
    
    Example: 
    "true"



### Output ports:

* __done__: _{"fileid" :string}_

    Sends the result of the action.
    
    Eg.
    {"fileid": "1_ewweewweFileID"}



* __error__: _{"error" :string}_

    Sends the error which happened during the execution of the action.
    
    Eg.
    {error: "Something went wrong!"}


