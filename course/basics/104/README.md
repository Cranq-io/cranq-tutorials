---
description: >-
  Covers CRANQ's public node repository. Why it's necessary, what its advantages
  are, how it's populated.
---

# 103: The CRANQ repo

The centerpiece of CRANQ's innovation is the _repo_: it takes the gobal database of editable code of [GitHub](https://github.com), the universal reusability of [npm](http://npmjs.com) packages, and the ease of use of [Zapier](https://zapier.com) connectors, and blends them into an global, extensible component library that is accessible right from the CRANQ app.

Unlike _GitHub_, the code you find in the CRANQ repo can be put to use right away. The repo is integrated into the IDE, and all CRANQ components share a common makeup of interface and internal structure. This allows you to just drag-and-drop anything from the repo right into your program.

Unlike code on _GitHub_, CRANQ code is an _actual database_ - the representations of hierarchical dataflow graphs - and thus, is a much richer medium than text code for expressing what components are expected to do.

:information\_source: CRANQ's natural progression will take it way beyond static typing. It's going to support built-in code attributes like statefulness, synchronicity, concurrency, and signal multiplicity; qualitative assessment based on documentation, unit tests, and popularity; and ties them all together in a recommendation engine that will predict the next component you need.

Unlike _npm_, the CRANQ repo hosts individual components instead of packages of components. Your running CRANQ program will only contain code that it actually uses.

Unlike _npm_ packages, CRANQ components are editable in place.

Unlike _Zapier_, the CRANQ repo is extensible without limit. Building new API integrations, data transformations, and webhooks are all possible without ever stepping outside CRANQ.

Unlike _Zapier_ triggers, apps, and actions, CRANQ components are editable with sophisticated version control.

The CRANQ repo aspires to be the place where all future code will be stored and accessed with ease.

## Namespaces

Since the CRANQ repo is the _one_ place for storing CRANQ code, and components are made to be reusable individually, it makes sense to organize them into a hierarchy of _namespaces_.

:information\_source: Private namespaces will soon provide a way for you to _own_ portions of the public repo, and store your code there. Eg. the namespace `@cranq` would belong to CRANQ LTD.

Read more about namespaces [here](../../advanced/namespaces.md).

## Storage

Currently the repo is stored as a set of files - one JSON for each node prototype. This comes with a number of advantages, the best of them being that CRANQ code can fit into existing software development workflows. You can use your usual version control system, while still treating the repo as a singular database by CRANQ internally.

:information\_source: Repo storage will not stop at files though. Our goal is to extend the file-based repository into a high performance database, so that storage will match the repo's internal representation, paving the way to a powerful component-recommendation engine.

:wrench: Because version control is very important to any sowtware development work, and the cloud-based repository does not yet exist, CRANQ supports mapping multiple paths in the file system to [custom namespaces](../../how-to/mapping-paths-to-namespaces.md). This offers an easy and transparent way to blend public and private domains of CRANQ code into a single, extended repository.
