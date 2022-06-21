# Yahoo Finance historical adjusted closed price & timestamp getter

[apis/fx]

### Input ports:

* __instrument__: _(any[] or {string: any})_

    [Inherited from port `tree` of `select adjusted prices`] 
    Receives the tree the node is extracted from



### Output ports:

* __timestamps__: _({string: any} or any[])_

    [Inherited from port `synced` of `syncer`] 
    Sends synchronized inputs as a record or tuple indexed by the names of the ports they were received through.
    
    Example:
    {"a": "Foo", "b": "Bar"}



* __adjustedcloses__: _any_



