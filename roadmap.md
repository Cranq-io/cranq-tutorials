---
description: Important features we're committed to delivering
---

# 🛬 Roadmap

## Forms

In the near future, CRANQ will support entering data through forms, making this process much easier.

## Behaviors

Documenting statefulness of nodes is a planned feature of CRANQ, aimed at aiding testing and qualitative scoring of nodes in the repository.

There are plans to make this more obvious. By extending nodes' interfaces with information about which outputs are expected to send signals in response to which inputs and under what circumstances, and comparing those expectations to the actually received and sent signals, CRANQ will be able to highlight nodes - also in red - where signals get stuck.

## Recommendation engine

CRANQ's natural progression will take it way beyond static typing. It's going to support built-in code attributes like statefulness, synchronicity, concurrency, and signal multiplicity; qualitative assessment based on documentation, unit tests, and popularity; and ties them all together in a recommendation engine that will predict the next component you need.

In the future, finding components you actually _need_ will become much easier, faster, and more intuitive with the introduction of the cloud-based repo and the recommendation engine built on top of it.

In the future, CRANQ will use data types to find compatible nodes for possible connections.

Code nodes don't do type checking at runtime because static type checking will be introduced soon, so a connection with mismatching data types (or other attributes) would be detected before the program runs.

## Private namespaces

Private namespaces will soon provide a way for you to _own_ portions of the public repo, and store your code there. Eg. the namespace `@cranq` would belong to CRANQ LTD.

## Typed traffic viewers

In the not so distant future, they'll be able to show images, charts, tables, HTML, and others meaningfully.
