# Yahoo Finance historical adjusted closed price & timestamp getter

[apis/fx]

### Input ports:

* __instrument__: `(any[] or {string: any})`

    [Inherited from port `tree` of `select adjusted prices`] 
    Receives the tree the node is extracted from

### Output ports:

* __timestamps__: `({string: any} or any[])`

    [Inherited from port `synced` of `syncer`] 
    Sends synchronized inputs as a record or tuple indexed by the names of the ports they were received through.
    
    Example:
    {"a": "Foo", "b": "Bar"}


* __adjustedcloses__: `any`

