---
description: [apis/fx/yahoo finance]
---

# Daily rates getter

### Input ports:

* __symbol__: ` string `

    Receives ticker symbol.
    
    Example:
    "DIS"


* __from__: ` number `

    Receives start date timestamp for querying data.
    
    Example:
    1486598400


* __to__: ` number `

    Receives end date timestamp for querying data.
    
    Example:
    1644364800


* __interval__: 
    ```
    ("1d" or "5d" or "1mo" or "3mo" or "6mo" or "1y" or "2y" or "5y" or "10y" or "ytd" or "max")
    ```

    Receives the interval of the `rates per date` output

### Output ports:

* __rates per date__: ` {string: number} `

    Sent the rates of the symbol per interval


* __error__: ` {"error" :"Service unavailable"} `

