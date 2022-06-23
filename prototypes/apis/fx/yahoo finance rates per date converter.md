---
description: [apis/fx]
---

# Yahoo Finance rates per date converter

### Input ports:

* __timestamps__: `any[]`

    [Inherited from port `array` of `create rates per date mapping`] 
    Receives array to be reduced.
    
    Example:
    ["A", "B", "C"]


* __prices__: `any[]`

    [Inherited from port `array` of `iterate over adjusted close prices`] 
    Recieves array to be iterated over.
    
    Example:
    [1,2,3]
    

### Output ports:

* __rates per date__: `any[][number]`

    [Inherited from port `reduced` of `create rates per date mapping`] 
    Sends the reduced array.
    
    Example:
    "ABC"

