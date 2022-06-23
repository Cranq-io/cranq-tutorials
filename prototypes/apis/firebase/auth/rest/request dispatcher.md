# Request dispatcher

[apis/firebase/auth/rest]

### Input ports:

* __action__: `any`

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


* __API key__: `any`


* __data__: `any`

### Output ports:

* __ID token__: `any`


* __user ID__: `any`


* __error__: `any`


* __auth context__: `any`

