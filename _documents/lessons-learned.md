---
layout: page
title: "Lessons learned"
permalink: /llearned.html
nav_order: 7
parent: RDF-Editor
comments:
giscus: 
repo: gjaaf/e-v3-rdf-editor-comments
---


## Lessons Learned

### Config in .yaml is not really needed

I created a separate configuration file (called `rdf-editor.yaml` by default). When starting, it seemed like a good idea because, well, that's what's commonly done. However, having learned more about Lisp, and especially about the 'data is code and code is data' adage [^1], I would now create the entire configuration in a separate Lisp file. Processing the `.yaml` file turned out to be slow, even if it is a moderately small file.

### Mixing config styles

At some point, I thought it might make sense to change the configuration system from YAML-based to a construct based on hashes of hashes. That turned out to be a nightmare, especially because I had the bright idea to mix both approaches to facilitate a step-by-step migration. It is still unfinished work, and I do not look forward to finishing it, as every error breaks the entire RDF editor.

### Blank nodes should be avoided.

I spent a considerable amount of time on handling blank nodes. Currently, the editor can (when it encounters one) transfer blank nodes to the tree. However, this is a 90% solution. I've encountered datasets where it is impossible to distinguish one blank node from another. There is only one fail-safe solution: skolemize your RDF data.

### Emacs as a malleable development tool

Much has been written about the customizability of Emacs. Emacs can be transformed far beyond its default distribution. It can be changed to almost anything you would like. This is a serious advantage when writing something where the final form is uncertain. This, by the way, is mostly due to the Lisp underpinning of Emacs. Developing against a running Lisp engine is extremely powerful.

[^1]: <small>The adage "code is data and data is code" in Lisp refers to the language's homoiconicity, where the program's representation is built from the same data structures as the data the program manipulates, typically lists. This allows for metaprogramming, where code can be treated as data and manipulated by the program itself.  Here are some links for more information:</small>

    *   <small>*Wikipedia on Homoiconicity:*</small>  
        <small>[https://en.wikipedia.org/wiki/Homoiconicity](https://en.wikipedia.org/wiki/Homoiconicity)</small>

    *   <small>*Paul Graham's "On Lisp":*</small>     
      <small>While not directly addressing the adage, this book explores Lisp metaprogramming extensively. You can find the online version here: [http://www.paulgraham.com/onlisp.html](http://www.paulgraham.com/onlisp.html) </small>


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



