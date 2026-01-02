---
layout: page
title: "RDF-editor visualisations"
permalink: /visualisations.html
nav_order: 5
parent: RDF-Editor
---

## Visualizations

A topic came up in my job about visualization techniques, and there
are, of course, many of them. Links to some of these resources will be
provided here. However, most techniques cannot display both a class
and its attributes in the same view. I came across rdfpuml and decided
to use it. The following brief visuals explain how this visualization
is embedded in RDF-Editor.

First, there is a new element in the tree: Visualizations. Here, you
can add folders to group the visualizations you create.

![Startup](assets/Peek 2025-07-06 09-35.gif)

Within the folder, you can create files.

![Startup](assets/Peek 2025-07-06 09-36.gif)

Finally, the files can be opened in Emacs just as you would normally
do.

![Startup](assets/Peek 2025-07-06 09-37.gif)

The last file you opened becomes the target for the element you want
to visualize. You can open any file, mark a region, and invoke
‘rdf-append-region-to-target-buffer’ (in my setup, bound to C-. r),
and the visualization will be displayed.

![Copy and render](assets/Peek 2025-07-07 13-40.gif)

I do not want all the details to be shown, so I will comment out some
of them:

![Copy and render](assets/Peek 2025-07-07 13-41.gif)

Next, add another object and edit the details there as well:

![Copy and render](assets/Peek 2025-07-07 13-51.gif)

In general, you can continue to copy content to the .ttl file that
will be visualized. I have added some extra functionality to the
[rdfpuml](https://github.com/VladimirAlexiev/rdf2rml) application used
in the background for visualization. With the open-sourcing of
RDF-Editor, these enhancements will also be made available as open
source.

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
