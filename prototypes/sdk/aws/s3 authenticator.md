# S3 authenticator

[sdk/AWS]

### Input ports:

* __session id__: _string_

    Receives the id of the S3 session.
    
    Example: 
    "s3-session-id"



* __access key id__: _string_

    Receives the AWS user's access key id.
    
    Example:
    "23478207027842073230762374023 "



* __secret access key__: _string_

    Receives the AWS user's secret access key.
    
    Example:
    "v3QoTTO2fmr5Wbh/v3QoTTO2fmr5Wbh+ASDF"



### Output ports:

* __done__: _null_

    It is triggered if the authentication was successful.



* __error__: _{"error" :string}_

    Sends error information in case the authenticatiomn was not successful.



