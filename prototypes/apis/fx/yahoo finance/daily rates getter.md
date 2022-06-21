# Daily rates getter

[apis/fx/yahoo finance]

### Input ports:

* __symbol__: _string_

    Receives ticker symbol.
    
    Example:
    "DIS"



* __from__: _number_

    Receives start date timestamp for querying data.
    
    Example:
    1486598400



* __to__: _number_

    Receives end date timestamp for querying data.
    
    Example:
    1644364800



* __interval__: _("1d" or "5d" or "1mo" or "3mo" or "6mo" or "1y" or "2y" or "5y" or "10y" or "ytd" or "max")_

    Receives the interval of the `rates per date` output



### Output ports:

* __rates per date__: _{string: number}_

    Sent the rates of the symbol per interval



* __error__: _{"error" :"Service unavailable"}_



