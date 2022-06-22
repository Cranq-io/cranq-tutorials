# Nodes setter

[data/tree]

Immutably stores the specified nodes on the specified paths of the tree.

Example:
1. `tree` receives 
{"a": "a"}@0
2. `path` receives
[
  ["a", "b"],
  ["a", "c"]
]@0
3. `nodes` receives
[0,1]@0
4. `tree` sends
{
  "a": {
     "b" : 0,
     "c": 1
  }
}@0

### Input ports:

* __tree__: _any_

    Receives tree data structure in which to store a node.
    
    Example:
    {"a": "a"}



* __paths__: _(string[] or number[])[]_

    Receives the location of the nodes.
    
    Example:
    [
      ["a", "b"],
      ["a", "c"]
    ]



* __nodes__: _any[]_

    Receives nodes to be stored in the tree.
    
    Example:
    [0,1]



### Output ports:

* __tree__: _any_

    Sends updated tree data structure.
    
    Example:
    {
      "a": {
         "b" : 0,
         "c": 1
      }
    }


