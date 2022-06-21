# Command runner

[system]

Runs the received command string with the received options.

Sends stdout, stderr and optionally error message when the process finished.

Bounces command and options when the node is already in the state of executing a command.

### Input ports:

* __command__: _string_



* __options__: _{"cwd" :string, "env" :{string: string}}_



### Output ports:

* __stdout__: _string_



* __stderr__: _string_



* __error__: _(string or null)_

    Null on success.



* __on busy__: _{"command" :string, "options" :{"cwd" :string, "env" :{string: string}}}_

    The received command and options when the node is still executing another command.



* __bounced__: _any_



