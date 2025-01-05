---
layout: page
title: "Introduction"
permalink: /introduction
nav_order: 2
---

RDF-editor was created as a response to a unique situation where
Linked Data was exchanged between parties, and where the exchanged
amount of data was in the region of 200M triples (or facts) per
exchange. Exchanging that much data creates it own problems. I had the
opportunity at the time to spend 10% of my time on study (this is a
standard rule for experts working at agency that I was employed) I
decided to dig a bit deeper ans spend the 10% study time on solutions
of the problem I encountered.

The results are presented here. I'm assuming that the reader is
familiar with Linked data and Lisp. If not, here are some links to
get you started:

### Linked data

1. *Introduction to Linked Data (by Linked Data Tools)*  
   [Intro to Linked Data](https://linkeddata.tools/linked-data-introduction/)

2. *What is Linked Data? (W3C)*  
   [W3C Linked Data Overview](https://www.w3.org/standards/semanticweb/data)

3. *Tim Berners-Lee's Design Principles for Linked Data*  
   [Linked Data Principles](https://www.w3.org/DesignIssues/LinkedData.html)

4. *W3C Linked Data Primer*  
    [Linked Data Primer (W3C)](https://www.w3.org/TR/ld-glossary/)

5. *LOD Cloud*  
    [Linked Open Data Cloud Diagram](https://lod-cloud.net/)

6. *RDF  Resource Description Framework (W3C)*  
    [W3C RDF Overview](https://www.w3.org/RDF/)

7. *SPARQL  Query Language for RDF (W3C)*  
    [W3C SPARQL Standard](https://www.w3.org/TR/sparql11-overview/)

8. *OWL  Web Ontology Language (W3C)*  
    [W3C OWL Overview](https://www.w3.org/OWL/)

9. *JSON-LD 1.1: A JSON-based Serialization for Linked Data (W3C)*  
    [W3C JSON-LD Documentation](https://www.w3.org/TR/json-ld11/)

10. *SKOS  Simple Knowledge Organization System (W3C)*  
     [W3C SKOS Reference](https://www.w3.org/TR/skos-reference/)

### Lisp

*   **Beginner:**

    *    [Practical Common Lisp](http://www.gigamonkeys.com/book/): A practical introduction to Common Lisp, excellent for grasping fundamental concepts. (Focuses on CL but concepts transfer to other Lisps)

*   **Beginner/Intermediate (Specifically Elisp):**

    *  [An Introduction to Emacs Lisp](https://www.gnu.org/software/emacs/manual/html_node/elisp/index.html): The official GNU Emacs Lisp manual introduction. It's comprehensive, but start with the early chapters.
    *   [Emacs Lisp Intro](https://www.emacswiki.org/emacs/EmacsLispIntro): A helpful introduction on the Emacs Wiki that gets you started.
    *   [A Beginner's Guide to Emacs Lisp Programming](https://www.masteringemacs.org): A very friendly guide for those completely new to programming and Elisp.
    *   [introduction to Lisp](https://www.geeksforgeeks.org/introduction-to-lisp/): A Lisp syntax description.

*   **Intermediate:**

    *   [On Lisp](https://www.paulgraham.com/onlisp.html): A comprehensive study of advanced Lisp techniques, with bottom-up programming as the unifying theme.



## Central Questions
When I started on this journey there were two very relevant questions:

1. Is it possible to get an understanding of the contents of a data set without prior communication about it?
2. Is it possible to create an editor for linked data that works on data stored in a RDF-store (so not in a file)?
3. Is it p[ossible to do this with open source tools?

### Understanding large datasets

There are of course many tools available for this. Ontologies and
concepts schemes are an integral part of Linked data. Tools like
Protege allow viewing of a class hierarchy, and right now there are
[many others]({% link other-solutions.md %})

It is the combination of the ontology and the linked data that for
many of the available tools is a problem. For example: Protege allows
you to view both the ontology and the instance data. However, when
that ontology has about 25.000 classes and the data contains more than
200 Million data triples it struggles (for 20 minutes or more) to show
that data. resorting to creating sparql queries is then the only
option. My intention in answering this question was to allow a quick
view of the structure of the data and then to allow easy insight in
the associated data.

### Edit RDF data

In general rdf-data in transit is often file based. At some point the
data is stored in a RDF-store. If there are then minor changes needed,
the input file must be edited, and then reloaded. This, again due to
the shere filesize is not a simple task. What I wanted to know if it
is possible to edit the data while it is still inside the server.
There are of course the well known update, insert and delete sparql
statements. However also here I would like to avoid having to write
sparql statements for simple updates.

### Open source

I have, for most of my career, worked with open source software and
I've learned much from it. As a result I'm biased to using open source
solutions, so I decided that part of the challange would be to use
open source solutions. In my case, I'm an avid emacs user, the tool to
use was emacs. I have limited experience with programming so I thought
it might help to be (again) more knowledgeable in that area as well.