---
title: Semantics of decompositions
layout: home
nav_order: 5
parent: About decompositions
---

## Semantics of Decompositions ##
The usual way of creating whole-part relationships is the `hasPart` relation. There is no standardized definition of the `hasPart` relation. Here are some examples:

| Ontology    | Relationship        | Context                                              |
| ----------- | ------------------- | ---------------------------------------------------- |
| BFO         | `has_part`          | General part-whole relationships                     |
| OBO         | `part_of`           | Biological structures and processes                  |
| PROV-O      | `hadPrimarySource`   | Provenance of data and documents                     |
| Schema.org  | `hasPart`           | Products, services, and other web entities           |
| NEN2660     | `hasPart`           | Civil products                                       |

> **Semantic Nuances:** 

An interesting aspect of decompositions arose when, in a use case, there was a suggestion to also have predicates like `canHavePart`. At the class level, a predicate like that makes sense: we can indicate that something may contain something else. However, at the instance level, there is something strange. The statement `my_bicycle canHavePart my_front_wheel` actually does not have any factual value. The use case was in an asset management context, and there the question is whether the wheel is on my bicycle, which requires a yes or no answer. There seems to be no value in the fact that it can be there.

However, a variant like `I mayContain the_current_flu_virus`, which is also a 'may' or 'can' kind of predicate, does have value: people might avoid contact with me because I cannot exclude having the contagious virus.

Thus, it seems that the `canHave`, `mayContain`, etc., predicates have different value when used in instance relations.

