---
layout: page
title: "What does it do"
permalink: /what-does-it-do
nav_order: 3
---

## What does it do?

RDF-editor can:

- access any sparql 1.1 store on the internet and locally
- use specific drivers when needed
- based on a configuration file allow you to define the ways classes, concepts etc. are retrieved from the rdf-store. These are called entry-points.
  - the entry-points can be followed into more detail (sub-classes, narrower conceptes etc.)
  - descend into more detail can optinally be based in incoming or outgoing arc's
- format the display of a subject on a shacl declaration that is stored in a rdf-store
- visualize geo (point only) locations 
- depict triples materializing as pictures when appropriate
- search (both over all graph's and on specific graphs)
- load data into graphs and store 
- get an LLM description of a subject
- analyze relational data stores 
- update triples in the store
- show a directory treeview and switch back and forth between both views
- transparantly swich stores if the namespace of an object is known 

## What does it (not yet) do?

- Show non-point geolocations
- Show web-links as clickable links
- page the output (currently is will limit most queries to a configurable number)
- allow access to property graphs
- color indicate a namespace switch in the treeview