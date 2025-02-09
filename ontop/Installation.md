---
title: Ontop Installation
layout: home
nav_order: 2
parent: Ontop
---

## Installation

The install process is described [here](https://ontop-vkg.org/guide/cli.html#setup-ontop-cli). It is a bit of a hassle to get it working, but finally it will work.

{: .warning }
Something that is not mentioned in the documentation is that the postgresql database needs a contrib for this to work.

If you get the error:

`it.unibz.inf.ontop.exception.OntopQueryEvaluationException: org.postgresql.util.PSQLException: ERROR: function digest(text, unknown) does not exist
  Hint: No function matches the given name and argument types. You might need to add explicit type casts.
  Position: 2207
`
  
You need to install the
[pgcrypto](https://www.postgresql.org/docs/current/pgcrypto.html)
contrib (of course). Use your package manager to do so. Here at
nerd-central we frown up-on general available OS-es like Linux and the such so we do not provide the actual command to do this. However seek and you shall find.

Once your package manager has completed you have to insert the extension in your schema. Do something like this in [psql](https://www.postgresql.org/docs/current/app-psql.html):

```sql
\c <the_database_where_you_are_connecting_to_from_Ontop>
SET search_path='public';
CREATE EXTENSION IF NOT EXISTS pgcrypto;
```

The response (when all is OK):

```sql
CREATE EXTENSION
```
