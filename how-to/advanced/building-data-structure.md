---
description: Cover how to build and modifie data structures with different node.
---

# Building data structure

## Using builders

Cranq provides a set of builder nodes, allowing the construction/initialization of arrays and key-value based structures.

### Example - Initializing an empty array

> _**Try out:**_
>
> Open project: **Builder (array) example project**

In this example, we use the`tutorials/data/Builder (array) example project` project to initialize an empty array. The initial values can be specified on it's `item` input port.

![](../../.gitbook/assets/array\_builder.gif)

#### Sample output:

```json
[
  0,
  0,
  0,
  0
]
```

### Example - Building a record

> _**Try out:**_
>
> Open project called: **Builder (dictionary) example project**

In this example, we will build a simple entity, representing an employee. In Cranq, records can currently be built as dictionaries.&#x20;

![](../../.gitbook/assets/dict\_builder.gif)

* This node builds key-value pairs, by taking the keys & values from the appropriate input, matching them by their order
* Both inputs must be arrays

In our example, we supply the following values:

```json
# keys:
["EmpID","Name","Dept","HireDate","Salary"]

# values:
[101,"Sue","Facilities","2019-02-13",1500]
```

#### Sample output:

```json
{
  "EmpID": 101,
  "Name": "Sue",
  "Dept": "Accounting",
  "HireDate": "2019-02-13",
  "Salary": 1500
}
```



## Using the flow/Syncer & Splitter nodes for data manipulation

The `flow/Syncer` node in Cranq is a synchronization primitive, that combines the data content of it's input signals into a single output stucture. It can be construct both arrays & dictionaries.

The syncer node features a dynamic input port set (spread port):

* It's `fields` input takes an array, which determines the quantity and names of its input ports
* The names of these input ports will determine whether the node creates an array, or a dictionary

For example:

* `fields` value `[0,1,2]` will result in ports `0, 1, 2`, and will yield an array with 3 elements
* `fields` value `["a","b","c"]` will result in ports `a, b, c`, and will produce a dictionary with 3 elements

_****_

### Example - Building arrays with values

> _**Try out:**_
>
> Open project called: **Syncer (build employees array) example project**

&#x20;Let's take the schema created in Example - Building a record, and construct a collection of employee records:

![](../../.gitbook/assets/emp\_syncer.gif)

*   Let's create 2 employee records, by channeling our test data as illustrated in the example mentioned above:

    ```json
    # schema:
    ["EmpID","Name","Dept","HireDate","Salary"]

    # record_1:
    [100,"Ted","Accounting","2020-11-08",1500]

    # record_2:
    [101,"Sue","Facilities","2019-02-13",1500]
    ```
* Merge them together with the flow/Syncer node
  * Note, that we are using the array-building feature of the node in this example
  * We use `[0, 1]` as it's fields input

#### Sample output:

```json
[
  {
    "EmpID": 101,
    "Name": "Sue",
    "Dept": "Facilities",
    "HireDate": "2019-02-13",
    "Salary": 1500
  },
  {
    "EmpID": 100,
    "Name": "Ted",
    "Dept": "Accounting",
    "HireDate": "2020-11-08",
    "Salary": 1500
  }
]
```

### Example - Combining records

> _**Try out:**_
>
> Open project called: **Combining with syncer example project**

In this example, let's create a collection describing the departments, and combine it with employees collection created in the previous example, to establish a repository:

![](../../.gitbook/assets/comb\_emp\_dep.gif)

* In  this sample we use identical data as we used in the Building arrays with values block with a department collection and employees collection
* the to blocks are connected the employee & department records together with a flow/Syncer node
  * At syncer we use the values `["Employees","Departments"]` as the "fields" input

#### Sample output:

```json
{
  "Employees": [
    {
      "EmpID": 101,
      "Name": "Sue",
      "Dept": "Facilities",
      "HireDate": "2019-02-13",
      "Salary": 1500
    },
    {
      "EmpID": 100,
      "Name": "Ted",
      "Dept": "Accounting",
      "HireDate": "2020-11-08",
      "Salary": 1500
    }
  ],
  "Departments": [
    {
      "Dept": "Accounting",
      "Head": "Joan"
    },
    {
      "Dept": "Facilities",
      "Head": "Frank"
    },
    {
      "Dept": "Legal",
      "Head": "Louis"
    }
  ]
}
```

### Example - Splitting records by keys

> _**Try out:**_
>
> Open project called: **Splitting records example project**

The `flow/Syncer` has an inverse node, `flow/Splitter`, which can be used to split an array or dictionary by it's elements or items.

It's signature and mechanism is very similar to the syncer, but in this case, the output nodes are dynamic.

Taking the previous example and split it up again to "Employees" and "Departments"

* Re-used the cranq code from previous example `tutorials/data/Syncer (build dictionary) example project`
* Placed a `flow/Splitter` node, and assign the static value `["Employees", "Departments"]` to the `fields` input
* Note, that this will also work for arrays - in that case, the desired array indexes should be specified

![](../../.gitbook/assets/split\_emp\_dep.gif)

#### Sample output:

```json
# Employees output
[
  {
    "EmpID": 101,
    "Name": "Sue",
    "Dept": "Facilities",
    "HireDate": "2019-02-13",
    "Salary": 1500
  },
  {
    "EmpID": 100,
    "Name": "Ted",
    "Dept": "Accounting",
    "HireDate": "2020-11-08",
    "Salary": 1500
  },
  {
    "EmpID": 1,
    "Name": "Joan",
    "Dept": "Accounting",
    "HireDate": "2016-04-28",
    "Salary": 2200
  },
  {
    "EmpID": 2,
    "Name": "Frank",
    "Dept": "Facilities",
    "HireDate": "2011-11-13",
    "Salary": 2000
  },
  {
    "EmpID": 3,
    "Name": "Louis",
    "Dept": "Legal",
    "HireDate": "2015-09-01",
    "Salary": 3000
  }
  ]
# Departments output
[
  {
    "Dept": "Accounting",
    "Head": "Joan"
  },
  {
    "Dept": "Facilities",
    "Head": "Frank"
  },
  {
    "Dept": "Legal",
    "Head": "Louis"
  }
]
```
