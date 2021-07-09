# Constructing data

This section demonstrates methods of constructing & initializing simple data structures in Cranq.

Starting from the basic atomic assignment operations, the examples will discuss building simple structures - with dedicated builders, and through merging / splitting - concluding with templating and serialization.



## Contents

- __[Using setters & deleters](2_1_setters_deleters/README.md#using-setters--deleters)__
    - [Example - Adding/assigning items to dictionaries](2_1_setters_deleters/README.md#example---addingassigning-items-to-dictionaries)
    - [Example - Inserting items into arrays](2_1_setters_deleters/README.md#example---inserting-items-into-arrays)
    - [Example - Deleting items from dictionaries](2_1_setters_deleters/README.md#example---deleting-items-from-dictionaries)
    - [Example - Deleting items from arrays](2_1_setters_deleters/README.md#example---deleting-items-from-arrays)
- __[Using builders](2_2_builders/README.md#using-builders)__
  - [Example - Initializing an empty array](2_2_builders/README.md#example---initializing-an-empty-array)
  - [Example - Building a record](2_2_builders/README.md#example---building-a-record)
- __[Merging & concatenation](2_4_merge_concat/README.md#merging--concatenation)__
  - [Example - Merging dictionaries](2_4_merge_concat/README.md#example---merging-dictionaries)
  - [Example - Concatenating arrays](2_4_merge_concat/README.md#example---concatenating-arrays)
- __[Using the flow/Syncer & Splitter nodes for data manipulation](2_3_syncer_splitter/README.md#using-the-flowsyncer--splitter-nodes-for-data-manipulation)__
  - [Example - Building arrays with values](2_3_syncer_splitter/README.md#example---building-arrays-with-values)
  - [Example - Combining records](2_3_syncer_splitter/README.md#example---combining-records)
  - [Example - Splitting records by keys](2_3_syncer_splitter/README.md#example---splitting-records-by-keys)
- __[Using templates](2_5_templating/README.md#using-templates)__
  - [Example - Filling string templates](2_5_templating/README.md#example---filling-string-templates)
- __[Serialization](2_6_serialization/README.md#serialization)__
  - [Example - Serializing structures](2_6_serialization/README.md#example---serializing-structures)
  - [Example - Parsing JSON structures](2_6_serialization/README.md#example---parsing-json-structures)