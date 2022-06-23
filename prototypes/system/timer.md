# Timer

[system]

Sets a timer which triggers `done` port after as many milliseconds as received or specified by `delay.  Timer can be canceled with ˙stop` (input).

Examples:
1. "timer1"@0 received via `start`
2. 300@0 received via `delay`
3. after 300 ms "timer1"@0 sent via `done`

1. "timer1"@0 received via `start`
2. `delay` set to 300
3.. "timer1"@0 received via `stop`
4. "timer1"@0 sent via `stopped`


### Input ports:

* __start__: `(string or number)`

    Receives the timerId which identifies the timer.
    
    Example:
    "timer1"


* __stop__: `(string or number)`

    Receives the timerId which identifies the timer to be stopped.
    
    
    Example:
    "timer1"


* __delay__: `number`

    Receives the time in milliseconds that the timer should wait before the `done` port is triggered.
    
    Example: 
    300

### Output ports:

* __done__: `(string or number)`

    Sends timerId when the delayed timeout is reached.
    
    Example:
    "timer1" 


* __stopped__: `(string or number)`

    Sends timerId when the timer is stopped.
    
    Example:
    "timer1" 

