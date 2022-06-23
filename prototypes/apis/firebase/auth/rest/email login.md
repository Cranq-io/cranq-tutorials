# Email login

[apis/firebase/auth/rest]

Logs in a Firebase user by their email & password.

User must be signed up, and email authentication must be enabled for the relevant Firebase Project.

### Input ports:

* __API key__: `any`


* __email__: `any`


* __password__: `any`


### Output ports:

* __ID token__: `any`


* __user ID__: `any`


* __error__: `any`


* __auth context__: `any`
    idToken
    email
    refreshToken
    expiresIn
    localId
    registered



