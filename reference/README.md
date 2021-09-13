# CRANQ reference course

Welcome to the CRANQ reference course! The intention of these tutorials, is to provide:
- A step by step guide to programming in CRANQ
- A set of examples for typical development scenarios, especially for transitioning from imperative languages

Like CRANQ itself, the documentation is also under constant development. We will constantly update this course as we add new features and capabilities.

## Assumptions

This tutorial assumes, that the reader is already familiar with the concept of CRANQ, the UI, and it's interactions - check out our [CRANQ 101 video course](https://cranq.io/go/app-tutorials) to learn the basics!

## How to use this guide

**Use it as a course:**

The examples in this guide are structured in a way, that they can be consumed as a course, walking through the various aspects of CRANQ. Just open up the [first section](1_application_flow/README.md) to get started!

**Use it as a quick reference:**

However, it can also be used as a quick reference guide, to get inspiration for solving typical programming tasks. Find the topic you are looking for in the list below!


## How to try the examples

Each example in this tutorial is included with your installation of CRANQ. With each example, you will find a section, such as this:

> **_Try out:_**
>
> Place node **tutorials/flow/Fork example**

Just search for this node in CRANQ, place it on your canvas, wire it to a start/log node, and you are good to go.


## Contents
---

### __[Managing application flow](1_application_flow/README.md)__

- __[Junctions](1_application_flow/1_1_junctions/README.md#junctions)__
  - [Example - Using conditions](1_application_flow/1_1_junctions/README.md#example---using-conditions)
  - [Example - Using forks](1_application_flow/1_1_junctions/README.md#example---using-forks)
  - [Example - Using gates](1_application_flow/1_1_junctions/README.md#example---using-gates)
- __[Iterators / loops](1_application_flow/1_2_iterators/READMEmd#iterators--loops)__
  - [Example - Simple foreach](1_application_flow/1_2_iterators/README.md#example---simple-foreach)
  - [Example - Parallel filtering](1_application_flow/1_2_iterators/README.md#example---parallel-filtering)
  - [Example - Synchronous filtering](1_application_flow/1_2_iterators/README.md#example---synchronous-filtering)
  - [Example - Reduction](1_application_flow/1_2_iterators/README.md#example---reduction)
  - [Example - Polling/synchronous loops](1_application_flow/1_2_iterators/README.md#example---pollingsynchronous-loops)
- __[Synchronization](1_application_flow/1_3_synchronization/READMEmd#synchronization)__
  - [Example - Synchronizing node inputs](1_application_flow/1_3_synchronization/README.md#example---synchronizing-node-inputs)
  - [Example - Using parameters with enumeration nodes](1_application_flow/1_3_synchronization/README.md#example---using-parameters-with-enumeration-nodes)

---
### __[Constructing data](2_constructing_data/README.md)__

- __[Using setters & deleters](2_constructing_data/2_1_setters_deleters/README.md#using-setters--deleters)__
    - [Example - Adding/assigning items to dictionaries](2_constructing_data/2_1_setters_deleters/README.md#example---addingassigning-items-to-dictionaries)
    - [Example - Inserting items into arrays](2_constructing_data/2_1_setters_deleters/README.md#example---inserting-items-into-arrays)
    - [Example - Deleting items from dictionaries](2_constructing_data/2_1_setters_deleters/README.md#example---deleting-items-from-dictionaries)
    - [Example - Deleting items from arrays](2_constructing_data/2_1_setters_deleters/README.md#example---deleting-items-from-arrays)
- __[Using builders](2_constructing_data/2_2_builders/README.md#using-builders)__
  - [Example - Initializing an empty array](2_constructing_data/2_2_builders/README.md#example---initializing-an-empty-array)
  - [Example - Building a record](2_constructing_data/2_2_builders/README.md#example---building-a-record)
- __[Merging & concatenation](2_constructing_data/2_4_merge_concat/README.md#merging--concatenation)__
  - [Example - Merging dictionaries](2_constructing_data/2_4_merge_concat/README.md#example---merging-dictionaries)
  - [Example - Concatenating arrays](2_constructing_data/2_4_merge_concat/README.md#example---concatenating-arrays)
- __[Using the flow/Syncer & Splitter nodes for data manipulation](2_constructing_data/2_3_syncer_splitter/README.md#using-the-flowsyncer--splitter-nodes-for-data-manipulation)__
  - [Example - Building arrays with values](2_constructing_data/2_3_syncer_splitter/README.md#example---building-arrays-with-values)
  - [Example - Combining records](2_constructing_data/2_3_syncer_splitter/README.md#example---combining-records)
  - [Example - Splitting records by keys](2_constructing_data/2_3_syncer_splitter/README.md#example---splitting-records-by-keys)
- __[Using templates](2_constructing_data/2_5_templating/README.md#using-templates)__
  - [Example - Filling string templates](2_constructing_data/2_5_templating/README.md#example---filling-string-templates)
- __[Serialization](2_constructing_data/2_6_serialization/README.md#serialization)__
  - [Example - Serializing structures](2_constructing_data/2_6_serialization/README.md#example---serializing-structures)
  - [Example - Parsing JSON structures](2_constructing_data/2_6_serialization/README.md#example---parsing-json-structures)
---
### __[Querying data](3_querying_data/README.md)__

- __[Using getters](3_querying_data/3_1_getters/README.md#using-getters)__
  - [Example - Getting data from dictionaries](3_querying_data/3_1_getters/README.md#example---getting-data-from-dictionaries)
    - [Getting dictionary size](3_querying_data/3_1_getters/README.md#getting-dictionary-size)
    - [Getting dictionary values by key](3_querying_data/3_1_getters/README.md#getting-dictionary-values-by-key)
    - [Getting all values from a dictionary](3_querying_data/3_1_getters/README.md#getting-all-values-from-a-dictionary)
    - [Getting all keys from a dictionary](3_querying_data/3_1_getters/README.md#getting-all-keys-from-a-dictionary)
  - [Example - Getting data from arrays](3_querying_data/3_1_getters/README.md#example---getting-data-from-arrays)
    - [Getting array length](3_querying_data/3_1_getters/README.md#getting-array-length)
    - [Getting array element by index](3_querying_data/3_1_getters/README.md#getting-array-element-by-index)
    - [Getting the first & last array elements](3_querying_data/3_1_getters/README.md#getting-the-first--last-array-elements)
- __[Using filters](3_querying_data/3_2_filters/README.md#using-filters)__
  - [Example - Filtering an array](3_querying_data/3_2_filters/README.md#example---filtering-an-array)
- __[Using mappers](3_querying_data/3_3_mappers/README.md#using-mappers)__
  - [Example - Selecting from collections of records](3_querying_data/3_3_mappers/README.md#example---selecting-from-collections-of-records)
  - [Example - Left-joining collections](3_querying_data/3_3_mappers/README.md#example---left-joining-collections)
- __[Using reducers](3_querying_data/3_4_reducers/README.md#using-reducers)__
    - [Example - Summing array values](3_querying_data/3_4_reducers/README.md#example---summing-array-values)
### __Using APIs__
- Coming soon
### __Working with file IO__
  - Coming soon
### __Working with OS processes__
  - Coming soon