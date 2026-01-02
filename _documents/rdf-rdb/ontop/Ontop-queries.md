---
title: Ontop Queries
layout: home
nav_order: 3
parent: Ontop
---

## Ontop queries pecularities

So, now you have Ontop runnning from the command line. And you send your first query. And you get the response:

```it.unibz.inf.ontop.exception.OntopReformulationException: it.unibz.inf.ontop.model.type.impl.ArrayDBTermType$IllegalArrayComparisonException: A query should not check equality between two arrays```

This happens with queries like:

```sql
select distinct ?p  where { ?s ?p <http://px-alpha.com/dvd/actor> . FILTER (isIRI (?s)) }
```

What seems to be the main thing is the selection of both ?s and ?p. When there is just one variable being selected things work fine:

```sql
SELECT DISTINCT ?p 
WHERE { 
  ?s a <http://px-alpha.com/dvd/actor> ;
     ?p ?o .
}
```

Then again:

```sql
SELECT ?s ?p ?o
WHERE { 
  ?s ?p ?o 
}
LIMIT 10
```
Also works. So there seems to be an issue when selecting two variables with a filter expression.
