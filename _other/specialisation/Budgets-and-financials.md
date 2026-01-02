---
title: Budgets and Financials
layout: home
nav_order: 1
collection: Other Things
parent: Specialisation
---

## Budgets and financials
In most organisations Budgets are an essential part of the business process. I think they deserve a specialisation that makes them easier to udnerstand.
We can understand budgets in two ways: as a constraint and as a resource.

## Budget as a resource
If we see budget as something we can spend it clearly is a resource
adhering to the Archimate definition: "Represents an asset owned or
controlled by an individual or organization". When modelled like this
I think we can express the notion of a budget in general and as a
project budget much better:

![Sources](../../../../assets/Budget specialisation.png)

In the sketch the resource is specialized to budget and furher
specialized to Project Budget. The reason for the latter
specialisation is that the properties that are normally used in
Projects (and which we will use in later annotations) are different
from properties used for general (for example departemental) budgets.

## Budget as a constraint
However, is we want to express the idea that there is a maximum budget
for something we should specialize from the Archimate Constraint
element:

![Sources](../../../../assets/Budget as constraint specialisation.png)

## Adding visual indicators 
As can be seen I’ve added an extra icon the the specialized components
to make theire meaning more clear, in this case an indication of a
stack of coins. This can be easily be done with the specialisation
manager of Archi. 

In the case of the project budget I’ve also added a
simplief Gantt chart symbol (that might acually be overdoing it, but
the second symbol is, in my opinion definitely worth it. There is also
a possible overlap with the symbol for the Plateau element, which also
uses this symbol. However the relative position reduced the risk
confusion strongly).

## Adding the type as text
This is something I also thing helps viewers: to add in the last line
the Archimate archtype. Even when the symbols do not yet make sense the
’subtitle’ will help to make sense of the view.
