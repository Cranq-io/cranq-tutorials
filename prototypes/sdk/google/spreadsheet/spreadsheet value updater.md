# Spreadsheet value updater

[sdk/google/spreadsheet]

Writes data to a single range of  a given spreadsheet.

Example:
1. `session Id` receives "spreadsheet_session"@0 
2. `spreadsheet Id` receives "1_ewweewweFileID"@0
3. `update meta data` receives {
 "range": "Sheet1!A1:B10"",
 "valueInputOption": "RAW" 
}@0
4. `done` sends null@0 

### Input ports:

* __session Id__: _string_

    Receives the session id of the spreadsheet action.
    
    Example: 
    "spreadsheet_session"



* __spreadsheet Id__: _string_

    Receives the id of the spreadsheet to be updated.
    
    Example:
    "1_ewweewweFileID"



* __update meta data__: _{"range" :string, "valueInputOption" :("RAW" or "USER_ENTERED")}_

    Receives the metadata of the update values.
    
    range: The A1 notation of the values to update. More: 
    https://developers.google.com/sheets/api/guides/concepts
    
    valueInputOption: Determines how input data should be interpreted. More: https://developers.google.com/sheets/api/reference/rest/v4/ValueInputOption
    
    Example:
    {
     "range": "Sheet1!A1:B10"",
     "valueInputOption": "RAW" 
    }



* __values__: _any[][]_

    Receives the new cell values to update.
    It contains arrays of the row values.
    
    Example:
    [
      ["A1 value", "B1 value"],
      ["A2 value", "B2 value"]
    ]



### Output ports:

* __done__: _null_

    Sends null if the action was successful.
    
    Example:
    null



* __error__: _{"error" :string}_

    Sends the error which happened during the execution of the action.
    
    Example:.
    {error: "Something went wrong!"}


