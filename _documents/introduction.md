---
layout: page
title: "Introduction"
permalink: /introduction.html
nav_order: 2
parent: RDF-Editor
comments:
giscus: 
repo: gjaaf/e-v3-rdf-editor-comments
---

## Introduction

RDF Editor was created in response to a unique situation where Linked
Data was exchanged between parties, with the amount of data reaching
around 200 million triples (or facts) per exchange. Exchanging this
volume of data creates its own problems. I had the opportunity to
dedicate 10% of my time to study (a standard practice for experts at
my agency). I decided to use this study time to investigate solutions
for the problem I encountered.

The results are presented here. I assume that the reader is familiar
with Linked Data and Lisp. If not, here are some resources to get you
started:

### Linked Data

1.  *Introduction to Linked Data (by Linked Data Tools)*
    [Intro to Linked Data](https://linkeddata.tools/linked-data-introduction/)

2.  *What is Linked Data? (W3C)*
    [W3C Linked Data Overview](https://www.w3.org/standards/semanticweb/data)

3.  *Tim Berners-Lee's Design Principles for Linked Data*
    [Linked Data Principles](https://www.w3.org/DesignIssues/LinkedData.html)

4.  *W3C Linked Data Primer*
    [Linked Data Primer (W3C)](https://www.w3.org/TR/ld-glossary/)

5.  *LOD Cloud*
    [Linked Open Data Cloud Diagram](https://lod-cloud.net/)

6.  *RDF Resource Description Framework (W3C)*
    [W3C RDF Overview](https://www.w3.org/RDF/)

7.  *SPARQL Query Language for RDF (W3C)*
    [W3C SPARQL Standard](https://www.w3.org/TR/sparql11-overview/)

8.  *OWL Web Ontology Language (W3C)*
    [W3C OWL Overview](https://www.w3.org/OWL/)

9.  *JSON-LD 1.1: A JSON-based Serialization for Linked Data (W3C)*
    [W3C JSON-LD Documentation](https://www.w3.org/TR/json-ld11/)

10. *SKOS Simple Knowledge Organization System (W3C)*
     [W3C SKOS Reference](https://www.w3.org/TR/skos-reference/)

11. *DASH Data Shapes*
     [Topquadrant: Stuff that could become an official standard](https://www.datashapes.org/). Highly recommended reading material, and the foundation
     for the RDF-editor as a feasible solution.

### Lisp

*   **Beginner:**

    *   [Practical Common Lisp](http://www.gigamonkeys.com/book/): A practical introduction to Common Lisp, excellent for grasping fundamental concepts. (Focuses on CL but concepts transfer to other Lisps)

*   **Beginner/Intermediate (Specifically Elisp):**

    *   [An Introduction to Emacs Lisp](https://www.gnu.org/software/emacs/manual/html_node/elisp/index.html): The official GNU Emacs Lisp manual introduction. It's comprehensive, but start with the early chapters.
    *   [Emacs Lisp Intro](https://www.emacswiki.org/emacs/EmacsLispIntro): A helpful introduction on the Emacs Wiki that gets you started.
    *   [A Beginner's Guide to Emacs Lisp Programming](https://www.masteringemacs.org): A very friendly guide for those completely new to programming and Elisp.
    *   [Introduction to Lisp](https://www.geeksforgeeks.org/introduction-to-lisp/): A Lisp syntax description.

*   **Intermediate:**

    *   [On Lisp](https://www.paulgraham.com/onlisp.html): A comprehensive study of advanced Lisp techniques, with bottom-up programming as the unifying theme.

## Central Questions

When I started this project, two key questions arose:

1.  Is it possible to understand the contents of a dataset without prior communication about it?
2.  Is it possible to create a Linked Data editor that works with data stored in an RDF store, rather than a file?

A third one came up during the work on these two:

3.  Is it possible to achieve this using open-source tools?

### Understanding Large Datasets

Many tools are available for this purpose. Ontologies and concept
schemes are integral to Linked Data. Tools like Protégé allow viewing
class hierarchies, and there are numerous other
[options](other-solutions.md).

However, many tools struggle with the combination of the ontology and
the linked data. For example, Protégé can display both the ontology
and instance data, but it struggles (taking 20 minutes or more) when
an ontology contains 25,000 classes and the data comprises more than
200 million triples. In such cases, SPARQL queries become the only
viable option. My goal was to enable quick insights into the data
structure and easy access to associated data.

### Editing RDF Data

RDF data is often file-based during transit. Eventually, the data is
stored in an RDF store. If minor changes are required, the input file
must be edited and reloaded. This can be a challenge due to the sheer
file size. I wanted to know if it was possible to edit data directly
within the server. While SPARQL's update, insert, and delete
statements exist, I wanted to avoid writing SPARQL for simple updates.

### Open Source

Having worked with open-source software for most of my career, I am
biased towards open-source solutions. Therefore, I decided that part
of the challenge would be to use open-source tools. As an avid Emacs
user, Emacs was the natural choice. My limited programming experience
also motivated me to become more proficient in that area.

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
