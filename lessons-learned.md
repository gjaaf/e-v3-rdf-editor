---
layout: page
title: "Lessons learned"
permalink: /llearned
nav_order: 7
---

## Lessons learned

### Config in .yaml is not really needed

I've created a seperate
configuration file (called rdf-editor.yaml by default). When starting
it seemed a good idea, because well, everybody does it that
way. Having learned more about lisp however, and especially about the
'data is code and code is data' adagium [^1], I would currently create the
entire config in a separate lisp file. Processing of the .yaml file
turned aout to be slow, even if it is a moderately small file.

### Mixing config styles

At some pint I thought it might make sense to change the config system
over from yaml based to a construct based on hashes of hashes. That
turned out to be a nightmare, especailly because I had the bright idea
to mix both approaches to facilitate a step by step migration. It is
still unfinished work and I do not look forward to finishing it, as
every error breaks the entire RDF-editor.

### Blank-nodes should be avoided.

I spend a considerable amount of
time on handling blank-nodes. Currently the editor can (when it
encounters one) transfer blank-nodes to the tree. However this is a
905% solution. I've encountered datasets where it is impossible to
distinguish one balnk node from another. There is only one failsafe
solution: skolemize your data.

### Emacs as malleable development tool

More has been written about this. Emacs can be made into something it
is not when you download the default distribution. And it can be
changed to almost anything you would like. This is one serious
advantage when writing something that you are not sure of what it will
be. This, by the way, is mostly due to the Lisp underpinning of
emacs. Developing against a running Lisp engine is extremely
powerfull.

[^1]: <small>The adage "code is data and data is code" in Lisp refers to the language's homoiconicity, where the program's representation is built from the same data structures as the data the program manipulates, typically lists. This allows for metaprogramming, where code can be treated as data and manipulated by the program itself.  Here are some links for more information: </small>

    *   *<small>Wikipedia on Homoiconicity:</small>*  
        <small>[https://en.wikipedia.org/wiki/Homoiconicity](https://en.wikipedia.org/wiki/Homoiconicity)</small>

    *   <small>*Paul Graham's "On Lisp"*      </small>
    <small>While not directly addressing the adage, this book explores Lisp metaprogramming extensively. You can find the online version here: [http://www.paulgraham.com/onlisp.html](http://www.paulgraham.com/onlisp.html) </small>
    
    



