# Dictionary array to csv converter

[data/csv]

Formats a dictionary array as a csv string. Does not support multi-level dictionaries.

Example:
1. 'array' receives
[
  {
    "a":1
    "b":2
  },
  {
    "a":11
    "b":22
  },
]
2. 'csv' sends 
"a,b
1,1
11,11"

### Input ports:

* __array__: _{string: (string or number or boolean)}[]_

    Receives the array of dictionaries to format.
    
    Example:
    [
      {
        "a":1
        "b":2
      },
      {
        "a":11
        "b":22
      },
    ]



### Output ports:

* __csv__: _string_

    The resulting csv string.



