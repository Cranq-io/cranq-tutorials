# Fork

[flow]

Forwards input data to one of two outputs, depending on the condition.

Example:
1. false@0 received via `condition`
2. "A"@0 received via `data`
3. "A"@0 sent via `on false`

More:
https://github.com/Cranq-io/cranq-tutorials/blob/main/reference/1_application_flow/1_1_junctions/README.md#example---using-forks

### Input ports:

* __data__: _any_

    Receives the data to be forwarded to either output.



* __condition__: _boolean_

    Receives the evaluation of some condition.



### Output ports:

* __on true__: _any_

    Sends signal received via `data` when condition was true.



* __on false__: _any_

    Sends signal received via `data` when condition was false.



