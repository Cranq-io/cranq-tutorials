---
description: >-
  This lession introduces CRANQ: its purpose, how it's different from other
  low-code tools, and what its long-term vision is.
---

# 101: What is CRANQ?

The official answer to this question is that **"CRANQ is a general-purpose low-code development platform with a visual, nodes-and-arrows** [**IDE**](https://en.wikipedia.org/wiki/Integrated\_development\_environment)**"** .

However, since CRANQ has this unique quality of uniting the spectrum that stretches from [no-code](https://en.wikipedia.org/wiki/No-code\_development\_platform) all the way to professional coding, CRANQ may be looked at differently depending on where in this spectrum you stand.

## ...to a no-coder?

If you're familiar with workflow automation platforms like [Zapier](https://zapier.com/), [Integromat](https://www.integromat.com/en), or [N8N](https://n8n.io/), then the best way to put it would be that **CRANQ is an infinitely extensible Zapier**.

After all, you can build workflows in CRANQ out of easy to use, high-level nodes representing popular services such as Airtable, or Google Maps, but the range of connectors extends beyond what the developer of the platform provides.

In CRANQ, you can build your own by mixing, composing existing nodes without leaving the platform.

## ...to a professional developer?

:wrench: There are some caveats, but the fact is, _CRANQ code is just code_. It's tied to a hierarchical [dataflow](https://en.wikipedia.org/wiki/Dataflow\_programming) graph structure, but when you look at the [Node.js](https://nodejs.org) JavaScript that it compiles to, it's really just the user-defined code of [_code_ _node_](../../../terms/code-node.md)s, plus code generated for connections and composition.

So in essence, **CRANQ is a framework and visual IDE for dataflow programming**.

## What makes CRANQ different?

First of all, **CRANQ is general-purpose**, and as such, first of its kind. It's a low-code platform that you can use to code whatever you want. At the moment it's most suited to building APIs, more specifcally, Web3 APIs, but the possibilties are only limited by the (ever growing) contents of the CRANQ [repository](../../../terms/the-repo.md).

And **the CRANQ repo is**, perhaps CRANQ's most appealing feature. It's a **global, extensible** database of code and resources that is **integrated** into the platform. Compared to Zapier's selection of connectors, it's extensible; and as opposed to eg. [npm](https://npmjs.com) or [GitHub](https://github.com), you can drag-and-drop code from it right into your app.

CRANQ is also the first visual IDE to incorporate **comprehensive** [**debug**](../106/) features. When running your program from the editor, activity and traffic can be observed real-time. Identifying and eliminating bugs visually not only becomes possible through CRANQ, but it's significantly faster than debugging text-code.

:wrench: Finally, for a low-code tool, CRANQ **fits** exceptionally well **into existing development workflows**. You have the option to put CRANQ code under version control (eg. Git), and to deploy it onto your existing infrastructure. It also integrates well with existing Node.js code in both directions: use npm packages in CRANQ, and use compiled CRANQ code in JavaScript projects.

## Glimpse of the future

CRANQ is being used in production today - but there are still lots of exciting features to come. Each of those features will multiply the productivity and intuitiveness of CRANQ.

Imagine an engine that delivers you just the right piece of code without asking. Or one that makes suggestions to replace components with faster, more robust ones. Or, a monitoring system that lets you spot and fix problems in production. These are just a few examples, but they are coming - so the CRANQ app you start building today will reap the benefits tomorrow.
