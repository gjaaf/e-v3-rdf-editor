---
layout: page
title: "RDF-editor org-pages"
permalink: /org-pages.html
nav_order: 6
parent: RDF-Editor
---

## Org-pages

After working on a visualitaion of the rdf-graph, another use-case for the tree that is used for the visualisation files. It is reused in rdf-editor to display org-babel pages.
The way the tree workis is exactly like the [visualisations]({{ site.baseurl }}/visualisations) method, but then under the org-pages entry.

Enter this in an org file that is created inside the tree:

``` python
#+TITLE: Python Hello World with Org-Babel

#+BEGIN_SRC python
return "Hello, World! This is an org-page inside rdf-emacs."
#+END_SRC

#+RESULTS:

```

And (after C-c C-c inside the BEGIN_SRC - END_SRC block) the resulting buffer contents is:

``` python
#+TITLE: Python Hello World with Org-Babel

#+BEGIN_SRC python
return "Hello, World, this is an org-page inside rdf-emacs."
#+END_SRC

#+RESULTS:
: Hello, World, this is an org-page inside rdf-emacs.
```


You can do the same with sparql mode:

``` sparql
#+BEGIN_SRC sparql  :url https://dbpedia.org/sparql :format text/csv
SELECT (COUNT(*) as ?triples)
WHERE {
?s ?p ?o
}
#+END_SRC
```
```txt
#+RESULTS:
|    triples |
|------------|
| 1153051695 |
```

This with the help of the [sparql-mode](https://github.com/ljos/sparql-mode) package.

Given what org-babel can do (the above examples are just to show that org-babel works) this supports very extensive research pages.
Learn more about org and org-babel:

1. [Org Mode on GNU ELPA](https://elpa.gnu.org/packages/org.html)
2. [Org Mode Wiki](https://orgmode.org/worg/)
3. [Org Mode Documentation](https://orgmode.org/manual/)
4. [Org-Babel Introductory Guide](https://orgmode.org/worg/org-contrib/babel/)
5. [Org Mode GitHub Repository](https://github.com/emacs-orgmode/org-mode)
6. [Org Mode Mailing List](https://lists.gnu.org/mailman/listinfo/emacs-orgmode)
7. [Org Mode GitHub Wiki](https://github.com/emacs-orgmode/org-mode/wiki)
8. [How to Use Org-Babel](https://www.schemers.org/texi-docs/org/org.texi/)
9. [Practical Org Mode](https://practical-org-mode.com/)
10. [Orgbabel: A Guide for Beginners](https://spacemacs.org/layers/+lang/org/README.html#orgbabel-example)

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
