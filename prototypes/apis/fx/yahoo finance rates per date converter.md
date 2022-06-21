# Yahoo Finance rates per date converter

[apis/fx]

### Input ports:

* __timestamps__: _any[]_

    [Inherited from port `array` of `create rates per date mapping`] 
    Receives array to be reduced.
    
    Example:
    ["A", "B", "C"]



* __prices__: _any[]_

    [Inherited from port `array` of `iterate over adjusted close prices`] 
    Recieves array to be iterated over.
    
    Example:
    [1,2,3]
    



### Output ports:

* __rates per date__: _any[][number]_

    [Inherited from port `reduced` of `create rates per date mapping`] 
    Sends the reduced array.
    
    Example:
    "ABC"



