---
layout: page
title: "What does it do"
permalink: /what-does-it-do.html
nav_order: 3
parent: RDF-Editor
comments:
giscus: 
repo: gjaaf/e-v3-rdf-editor-comments
---

## What it Does

RDF-Editor can:

*   Access any SPARQL 1.1 store, both on the internet and locally.
*   Utilize specific drivers when needed.
*   Use a configuration file to define *entry points*, which specify how classes, concepts, etc., are retrieved from the RDF store.
    *   These entry points can be followed to explore details such as subclasses or narrower concepts.
    *   The descent into more detail can optionally be based on incoming or outgoing arcs.
*   Format the display of a subject based on a SHACL declaration stored in the RDF store.
*   Visualize geo locations (currently only points).
*   Display triples as pictures when appropriate.
*   Search across all graphs or within specific graphs.
*   Load data into graphs and persist them.
*   Generate an LLM description of a subject.
*   Analyze relational database schemas and relationships.
*   Update triples within the store.
*   Display a directory tree view and allow switching between the directory and other views.
*   Transparently switch between stores if the namespace of an object is known.

## What it Does Not (Yet) Do

*   Display non-point geo-locations.
*   Render web links as clickable elements.
*   Page the output (currently, queries are limited to a configurable number of results).
*   Provide access to property graphs.
*   Visually indicate namespace switches in the tree view through color coding.

<script src="https://giscus.app/client.js"
        data-repo="gjaaf/e-v3-rdf-editor-comments"
        data-repo-id="R_kgDON2t9fg"
        data-category="Announcements"
        data-category-id="DIC_kwDON2t9fs4CmzNm"
        data-mapping="title"
        data-strict="0"
        data-reactions-enabled="0"
        data-emit-metadata="0"
        data-input-position="top"
        data-theme="light"
        data-lang="en"
        crossorigin="anonymous"
        async>
</script>
