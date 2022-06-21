# Request dispatcher

[apis/firebase/auth/rest]

### Input ports:

* __action__: _any_

    Identifies account action in the Google Identity Toolkit API.
    
    Possible values:
    
    "signInWithCustomToken"
    "signUp"
    "signInWithPassword"
    "signInWithIdp"
    "createAuthUri"
    "sendOobCode"
    "resetPassword"
    "update"
    "lookup"
    "delete"



* __API key__: _any_



* __data__: _any_



### Output ports:

* __ID token__: _any_



* __user ID__: _any_



* __error__: _any_



* __auth context__: _any_



