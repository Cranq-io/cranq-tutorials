---
description: sdk/AWS]
---

# S3 authenticator

### Input ports:

* __session id__: `string`

    Receives the id of the S3 session.
    
    Example: 
    "s3-session-id"


* __access key id__: `string`

    Receives the AWS user's access key id.
    
    Example:
    "23478207027842073230762374023 "


* __secret access key__: `string`

    Receives the AWS user's secret access key.
    
    Example:
    "v3QoTTO2fmr5Wbh/v3QoTTO2fmr5Wbh+ASDF"

### Output ports:

* __done__: `null`

    It is triggered if the authentication was successful.


* __error__: `{"error" :string}`

    Sends error information in case the authenticatiomn was not successful.

