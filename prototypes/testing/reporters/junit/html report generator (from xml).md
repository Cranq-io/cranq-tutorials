# HTML report generator (from xml)

[testing/reporters/junit]

Generates a HTML report of the specified JUnit XML, and saves it to the specified path.

### Input ports:

* __junit xml__: _any_

    The JUnit-format XML content to generate the report for.
    
    Example:
    "<testsuites tests=\"2\" errors=\"0\" failures=\"0\" skipped=\"0\"><testsuite tests=\"2\" errors=\"0\" failures=\"0\" skipped=\"0\" name=\"GET /user/:id - for valid user IDs\" time=\"0.145\"><testcase name=\"should return status 200\" classname=\"should return status 200\" assertions=\"1\"></testcase><testcase name=\"should have &quot;id&quot; field\" classname=\"should have &quot;id&quot; field\" assertions=\"1\"></testcase></testsuite></testsuites>"



* __report path__: _any_

    The desired report path.



### Output ports:

* __generated path__: _any_

    Indicates, that the report was generated successfully.



* __bounced__: _any_

    Indicates, that the report has failed to generate.


