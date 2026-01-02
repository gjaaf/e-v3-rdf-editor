---
title: Updating
layout: home
nav_order: 3
collection: Other Things
parent: Extending modelling
---

## Updating the model

I personally think that, just making static charts may not have the
implact we would like Enterprise Architecture to have. Especially
since nowadays infrastructure comes and goes with an update of a
config file (infrastructure as code). Another aspect that makes
classical Architecture views less relevant is that the major
applications in organisations tend to be bought as software as a
service (we pushed that with the re-use before buy before make
principle). 

On the other hand, questions like: are we moving in the right
direction? Are we sure we not only do things good, but are we also
sure we’re doing the good things? In general, there is a much more
strategic view is requested.

This strategic view necesarely is based on data associated to the
objects we’re modelling. To show this data we could use the annotation
techniques shown in the [previous story](../Annotation). 

However I think that there are use-cases where a view containing
annotations will be re-used over time, and in that case an automated
update of the annotation would help to keep an overview over the
development of the enterprise.

In this final part of this series we’ll research the options to do
actual update to the model.

### What does not work
- Using the .csv export of the model. The annotations are not in in there.
- Using the Open Exchange File (also here the annotations are not included).

### What could work
- Reading the actual Archimate file, updating it and writing a new
  file with updates. The annotation objects are in the archimate file.

There are of course major drawbacks here, especially the close
coupling of the reader/updater to the internal fileformat of
Archimate. On the other hand: the Archimate file is a ZIP file, and
the part we need to update is an .xml file. For a proof of concept
that should do. And when the PoC is seen as valuable, a better (API
based) approach can be developed.

Cliffhanger deteced here: there will be sub-article the shows the PoC.

### Coining the term ArchDevOps
This appraoch, where models are updated from the environment requires
writing code that retrieves data from other systems. Some examples:
- retrieve headcount from HR systems
- retrieve the number of instances for Architecture Building Blocks
- Retrieve the number of projects that run on specific Software
Building Blocks There are many others that can make sense, even up to
creating graphs and adding them to an annotation block.

However, in some way or another, code has to be written and code has
to run. And the obvious way of doing that is is using a DevOps
appraoch. Which then translates to ArchDevOps. 
