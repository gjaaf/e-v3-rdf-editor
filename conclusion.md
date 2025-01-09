---
layout: page
title: "Conclusions"
permalink: /conclusions.html
nav_order: 7
parent: RDF-Editor
---

## Conclusions

The project was started with [3 questions]({% link introduction.md %}).

The answer is positive on all three.

- Yes, it is possible to get an idea of the content of a store. But you need to know some things. For instance, that the `rdf:type` predicates are (in our case) almost always pointing to an object. This means the expansion mechanism 'incoming arcs' must be used to find instances of a class. So, this still requires a basic understanding of RDF. If a reverse predicate (for example, `has-instance`) were available, the discovery would be much easier.

- Yes, it is possible to create an editing tool for RDF stores.

- Yes, Emacs can be used for this. In fact, for the quick development of something where the entire functionality cannot be determined, the malleability of Emacs helps a lot in developing something like this.
