# Using setters & deleters

Setters are the atomic data manipulation operations in Cranq. There are built-in nodes for dictionaries/records, and one for arrays.

## Example - Adding/assigning items to dictionaries

> **_Try out:_**
>
> Place node **tutorials/data/Setter (dictionary) example**

Adding/assigning items in a dictionary can be performed with the ```data/dictionary/Item setter``` node
- It takes a dictionary, and a key/value pair as input
- If the key already exists in it, the value will be overwritten
- If the key does not exist, it will be created

![](images/2021-07-19-13-34-57.png)

### Sample output:

```json
{
  "key2": "value2",
  "key1": "value1"
}
```

## Example - Inserting items into arrays

> **_Try out:_**
>
> Place node **tutorials/data/Setter (array) example**

Adding/assigning elements in arrays can be performed with the ```data/array/Item inserter``` node.
- It takes the target array, the item to add, and the index to insert at as input
- Over-indexing is possible, but items can only be added to the end of the array

![](images/2021-07-19-13-45-44.png)

### Sample output:

```json
[
  "val1",
  "val2",
  "val#n",
  "val12"
]
```

## Example - Deleting items from dictionaries

> **_Try out:_**
>
> Place node **tutorials/data/Deleter (dictionary) example**

Deleting items from dictionaries by key can be performed with the ```data/dictionary/Item deleter``` node.
- It takes the dictionary and the key to remove as arguments
- If the key does not exists, the node leaves the input unchanged

![](images/2021-07-19-14-05-43.png)

### Sample output:

```json
{
  "a": "b"
}
```

## Example - Deleting items from arrays

> **_Try out:_**
>
> Place node **tutorials/data/Deleter (array) example**

Deleting items from arrays is possible by index, with the ```data/array/Item deleter``` node.
- It takes the array and the index to remove as arguments

![](images/2021-07-19-14-11-42.png)

### Sample output:

```json
[
  "a",
  "b",
  "d"
]
```