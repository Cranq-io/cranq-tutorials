---
description: Important features we're committed to delivering
---

# 🛬 Roadmap

CRANQ is designed from the ground up to deliver never before seen heights of productivity, comprehension, and operational transparency. However, a system that can deliver all that is necessarily complex, and CRANQ - the way we always envisioned it - is based on a number of fundamental features working in concert.

Some of these features we've already implemented, at least to the extent that they're usable:

* building and navigation
* basic repo search
* running and downloading compiled program
* activity view w/ JSON traffic inspectors

But some others we're still working on. This is a collection of features from our backlog - each of which we expect will multply CRANQ's usefulness.

## Recommendation engine

Perhaps the most important feature on our roadmap is the recommendation engine.

It's an extension of searching the repo, and it's main purpose is to predict the next component or the next connection you're going to place on the canvas. First, it looks at what you're building: nodes and connections already on the canvas. Then it matches them to the vast number of components available in the repo, and comes up with a list of nodes that it found to be used in similar contexts.

The matching process relies on component structure, data types, [behaviors](roadmap.md#behaviors), documentation quality, and even popularity to give you the best options.

Beyond predicting the next best node, the recommendation engine has other uses, too. It can also tell you about your existing CRANQ program, drawing your attention to potential risks and errors. A connection between mismatching types? Shows up in red.

## Behaviors

In the world of classical software development, the best code is the one that can express what it's going to do without actually doing it.

This has several benefits. Code like this is easier to read, easier to catch bugs, and easier to test. The more code tells about itself without running, the better.

This is no different in CRANQ. But in CRANQ, we're dealing with code that is represented by structured data, not text. And structured data has the advantage of being extensible without sacrificing readability. So while in textual programming languages code can tell very little about itself (:wrench: class structure, arguments, & return value), CRANQ code can tell much more. The difference is what we call _behaviors_, and their purpose is help CRANQ developers build faster, and catch problems sooner.

:wrench: Behaviors include: statefulness, synchronicity, mutation, signal multiplicity, signal routing.

Behaviors also contribute to the qualitative scoring of nodes. Prototypes with more specific behaviors score higher.

## Forms

Easy and meaningful data entry is what makes a low-code tool accessible and brings it closer the realm of no-code.

Setting node parameters as JSON data may be a challenge, especially to no-code users, and considering complex data types.

Fortunately, JSON can be broken down along structural lines into multi-level forms. With information built into data types about what kind of input field to use, we'll be able to generate forms for input ports of virtually any complexity.

## Typed traffic viewers

What forms are to input ports, are type-specific traffic viewers to output ports and connections.

In order to work even faster in CRANQ, ideally, traffic viewers would display data according to its kind. Images should show as images, charts displayed as chats, HTML rendered as HTML, and so on.

The same way we can associate form fields with types, we can do the same with traffic viewers.
