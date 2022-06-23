---
description: [sdk/google]
---

# Spreadsheet

Works with google spreadsheet using the googleapis sdk.

### Input ports:

* __action__: 
    ```
    {"sessionid" :string, "type" :("service_account_auth" or "update"), "options" :{string: any}}
    ```

    Receives the parameters of the google spreadsheet base prototype.
    
    Example: 
    {
      "sessionid" : "drive_session",
      "type": "service_account_auth",
      "options": {
         "email" : "email@email.com",
        "keyFile":  null,
         "key": "TopSecretKey!" 
      }
    }

### Output ports:

* __done__: `any`

    Sends the result fo the action.
    
    Example:
    null


* __error__: `{"error" :string}`

    Sends the error which happened during the execution of the action.
    
    Example:.
    {error: "Something went wrong!"}

