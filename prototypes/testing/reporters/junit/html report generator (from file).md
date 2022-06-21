# HTML report generator (from file)

[testing/reporters/junit]

Generates an HTML report of the specified JUnit XML file, and saves it to the specified path.

### Input ports:

* __junit xml path__: _any_

    The path to the JUnit XML file to generate the report for.
    
    Example:
    "C:\\folder\\report.xml"



* __report path__: _any_

    The desired report path.
    
    Example:
    "C:\\folder\\report.html"



### Output ports:

* __generated path__: _any_

    Indicates, that the report was generated successfully.



* __bounced__: _any_

    Indicates, that the report has failed to generate.



