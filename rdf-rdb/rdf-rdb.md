---
title: RDF/RDB
layout: home
nav_order: 2
parent: Home
has_toc: false
---
## RDF to RDB (and back) ##

So, everybody who has worked with linked data knows about conversions
from and to other formats. From relational databases (RDB) or flat
files, etc., to RDF, because, well, that is the format we need for
networked data. And the other way around as well, from RDF to RDB, for
example, because data visualization tooling works on relational data,
not linked data.

The main problem is that when we do conversions like that, we actually
copy data, be it in a different format. But the data we originally
only had in one system, we will have after the conversion in two
systems as two separate sets. This creates various problems:

- If the data is big, we’ll have two big sets.
- But more importantly, we’ll have two sets we’ll have to keep up to date.

The last point is usually the most difficult one, especially when the
data is in an operational system, where it is changed by data
transactions by users continuously. Usually, the only feasible way is
to copy data periodically from one format to the other, which creates
another complexity. We need to keep in mind the date and time of the
moment of the conversion and must remember that the most recent data
is not in both systems.

## Data at the source ##
 
In the Netherlands, the country where I live, there is a strong
architectural direction, called "data at the source" (in Dutch: "data
bij de bron"). The main idea is to avoid copies of data. The line of
thought here is that having no copies solves a lot of data handling
problems, among them the problems we indicated above.

Here in the pages of this blog, we’ll investigate options to use RDF data without the dreaded copying.

We’ll look at two options:

- [Ontop](../ontop/ontop), a tool that allows access to relational databases from SPARQL
  using a pass-through mechanism.
- [rdf_fdw](rdf_fdw), an extension for PostgreSQL that can convert data in RDF
  stores to PostgreSQL databases, also with a pass-through mechanism. 
