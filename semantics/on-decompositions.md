---
title: About decompositions
layout: home
nav_order: 1
parent: Semantics
---

# Decompositions and Semantics

## Introduction

In the context of semantic data processing, decomposition refers to the process of breaking down complex entities or systems into smaller, more manageable components. This approach facilitates a deeper understanding of the subject matter, enables more efficient analysis, and supports effective problem-solving.

## Decomposition - A Definition

According to the Cambridge Dictionary, decomposition is "the action of breaking, or breaking something, into smaller parts." In the context of information systems, it involves analyzing and dividing a whole into its constituent elements to understand their individual characteristics and relationships.

## Benefits of Decomposition

* **Improved Understanding:** By breaking down complex systems, we can gain a deeper understanding of their intricacies and underlying mechanisms.

* **Enhanced Problem-Solving:** Decomposition enables systematic analysis and problem-solving by addressing complex issues in smaller, more manageable pieces.

### Key Characteristics of Decompositions

* **Viewpoint-dependent:** Decompositions are inherently subjective and created from a specific perspective.

* **Informal Nature:** Unlike formal ontologies, decompositions are often less structured and more flexible.

### Decomposition Examples

* **Project Management:** Decomposing a project into tasks and sub-tasks.

* **Engineering:** Dividing a complex system into subsystems, components, and sub-components and then into documents that contain the data about the components.

* **Business Processes:** Breaking down a business process into individual steps and activities.

* **Shipping:** Decomposing in break-bulk and container transport, then in ships (for break-bulk) and containers and packages.

{: .note }
The second and fourth example contain different 'things' on different levels. That is not a mistake. If a decomposition like this works for the users, it may be a very good solution. The important thing here is: decompositions serve those that use them and these are tailored to their needs. 

### Decompositions vs. Ontologies/Taxonomies

While related, decompositions differ significantly from ontologies and taxonomies:

* **Ontologies:** Formal representations of knowledge, emphasizing precise definitions and relationships between concepts (e.g., subclass, instance-of).

* **Taxonomies:** Structured classifications of concepts based on hierarchical relationships (e.g., broader, narrower, related).

* **Decompositions:** Focus on breaking down a whole into its constituent parts from a specific viewpoint, often less formal than ontologies or taxonomies.

## The 'Universal' Decomposition

The notion of a single, "universal" decomposition for all purposes is a misconception. Different perspectives and objectives necessitate different decompositions. Decompositions are goal-oriented: we create them for a certain goal, to help us with a certain problem or question. And they are context related. The examples above show this: the engineering example and the shipping example originate from the same company working on a single product.

It is important to stress the fact that a universal decomposition is a misconception, because it can create significant obstacles like:

* **Confirmation Bias**: Once someone invests time and effort in creating a specific decomposition, they tend to favor it. This confirmation bias makes it difficult to objectively evaluate alternative approaches.

* **Cognitive Rigidity**: Deeply ingrained thinking patterns and expertise can limit the ability to see problems from new perspectives. When someone has spent years working with a particular decomposition, it becomes their "mental model," making it hard to consider other valid approaches.

* **Communication Barriers**: Different decompositions often reflect different perspectives, priorities, and goals. If individuals are too attached to their own decomposition, it can hinder effective communication and collaboration.

* **Resistance to Change**: Change can be disruptive, and people naturally resist changes to their established ways of thinking and working. This resistance can make it difficult to adopt new decompositions, even if they offer significant advantages.

{: .note } 
The universal decomposition notion often leads to long discussions where people try to convince each other of the 'best solution'. Understanding that there will almost always be multiple decompositions, and that they are goal-oriented and context dependent helps to reduce these, often fruitless, discussions.

## Multiple Simultaneous Decompositions

As indicated above, organizations often employ multiple decompositions to address various perspectives and requirements. For example, an engineering team might use a decomposition based on the systems that can be distinguished in a product, while a maintenance team might use a decomposition based on physical location or the machines that make up a production line.

Given the fact that these simultaneous decompositions exist, two interesting questions arise:
- What is the nature of a decomposition, what makes them what they are?
- How do decompositions relate to each other?

### The Nature of Decompositions

A key aspect of decompositions is that they are goal-oriented. Alongside the goal, there is usually a method or process for carrying out the decomposition. And they are relevant in a certain context. A few examples will help illustrate this:

**Location Decomposition in Construction Sites**

Construction sites are often divided into a grid of 10-by-10 meter squares to prevent multiple activities from occurring in the same location simultaneously. This is based on the principle that construction work often takes place at a certain elevation, and activities such as welding at 20 meters, for example, can create hazardous conditions below the work area. Linking the 10x10 meter grid elements to the planned activities helps mitigate these hazards for on-site workers.

The goal here is to avoid hazardous conditions, and the method is dividing the site into a 10x10 meter grid in areas where construction work is being performed. The context is a construction site, during the build phase.

**Work Breakdown Structure (WBS)**

This is one of the most common applications of decomposition: project planning. A complex task is divided into smaller, more manageable tasks, which are then allocated to the teams responsible for carrying out the work.

The goals here include:

* **Enhanced Project Control:** Smaller, more manageable tasks allow for better progress tracking and early identification of potential roadblocks. This facilitates timely adjustments and minimizes the risk of project delays.

* **Improved Resource Allocation:** By understanding the specific requirements of each sub-task, resources (time, budget, personnel) can be allocated more effectively.

The method used typically involves:

* Dividing tasks into sub-tasks that are small enough to be completed within a specific timeframe
* Dividing tasks in a way that makes dependencies between them clear
* Dividing tasks according to required skill levels
* Ensuring each task has a clear deliverable
* Defining clear acceptance criteria for completed tasks

The context is project management; the decomposition is relevant for the project management team.

> **Important:** In general, a good decomposition is defined by a clear goal (or set of goals) and a method that guides the creation of the individual decomposition elements and a definition of its context.

The following sketch may clarify this somewhat more. It shows the structures (in most cases decompositions) that were used in the creation, operation, and maintenance of big industrial equipment.

![Sources](../assets/Decomp80p.png)

From the sketch it will be clear that the context can be bounded by phases, but can also be bounded by business process.

### The Relationship Between Decompositions

As we have seen: multiple simultaneous decompositions can (and usually will) exist. An interesting question is: are they related and if so, how?

**Decompositions and Instances**

Important here is: decompositions are imaginary things. They are not real. The entire structure is something we make up to make certain things easier to understand. In general, at some point, we link a decomposition element to something in the real world.

For example, take the drivetrain of a car, where the first level of a decomposition could be:
- Engine
- Transmission
- Driveshaft
- Differential
- Axles
- Wheels

The engine could be further composed of:
- Cooling system
- Ignition system
- And so on

The sketch below shows a slightly more detailed decomposition:

![Decomposition example](../assets/Decomposition sketches-Page-1.png)
*Decomposition example, all arrows indicate a hasPart relation.*

In my car (the one that is in front of my house) there is an actual engine, with a serial number (for example VM12345). The engine contains 4 spark plugs, one for each cylinder.

![Decomposition example](../assets/Decomposition sketches-Page-2.png){: width="250" }
*Decomposition of the spark plugs in my car*

In semantic terms, the actual spark plugs would be the instance. They have a number (plug 1..4) which corresponds to the cylinder number and are part of the engine with serial number VM12345.

In general, we link instances to decomposition elements. These instances are real-world things that we connect to a decomposition element.

The information we now have of spark plug 3 is:

![Decomposition example](../assets/Decomposition sketches-Page-3.png){: width="500" }

The way to connect this instance to the decomposition above is by adding a new field which has a value that points to the correct decomposition element.

![Decomposition example](../assets/Decomposition sketches-Page-4.png)

> **Note:** There are a few things to clarify. First: we're assuming that a spark plug can also be used in something that is not a car (like a motorcycle). Otherwise, we could just have added the spark plug to the decomposition. A drawback of this approach is that the decomposition needs to be absolutely complete and accurate for the domain, otherwise data entry for unforeseen cases is impossible. In general, the more robust approach is to allow the user to choose a decomposition element and, given the fact that users make mistakes, to check for entries that are unusual.  
>
> Secondly: we're assuming that each individual spark plug will have data. That will only make sense if there is a reason to monitor or maintain each plug individually. If we would only replace all of them at the same time, and replace them all if one is faulty, then we would probably be treating the plugs as a group.

### Linking Decompositions Over Instances 

The example before showed a single decomposition coupled to an
instance. We can easily extend that by adding multiple fields that
reference different decompositions. This technique is sometimes called
multiparenting. Another term that is sometimes heard is dimensions
(they can be close to the dimensions seen in snowflake-based data
lakes).

Hier moet een plaatje komen.

### The Value of Decomposition Linkage

OPTIE2

Let’s consider a somewhat more complex example: a decomposition setup that is used in the power industry, defined by ISO-81346, also known as RDS-PS.

The primary goal of RDS-PS is the create reference number of objects in power-systems like power-plants, wind-turbines, et cetera. So it is concerned with the individual things, And it uses
multiple decompisitions to in the creation process of the reference numbers.

The main idea is that there are four general aspects that matter for all objects in a plant: 
  - the system of which the object is a part
  - the inferent function of an object
  - the location of an object 
  - the type of the object.

<4 assig plaatje>

There are extensive rules and agrements on the methods that should be
used to create the decompositions that are created to link the aspects
to the object.

Here it can be seen that there are indeed more decompistions that are
used together. And they are not only used in the data of the object,
they are used in the reference tag of the obejct as well. See the
below scetch (taken from xxxxx). The identifying code of the obejct is
created from the decompistions, where the path (from the top of the
decomposition to the entry that is referenced) is included in the
reference.

hier: wire plaatje

## Completeness, Granularity, and Decomposition ##

**Status: Work in Progress**

A decomposition does not necessarily need to include all possible
instances or types. The level of detail (granularity) depends on the
specific use case and the objectives of the analysis.

## Semantics of decompisitions ##
The usual way of creating the whole-part relations is the `hasPart`
relation. There is no standardized defintion of the `hasPart`
relation. Just some examples:

| Ontology    | Relationship       | Context                                              |
| ----------- | ------------------ | ---------------------------------------------------- |
| BFO         | \`has_part\`       | General part-whole relationships                     |
| OBO         | \`part_of\`        | Biological structures and processes                  |
| PROV-O      | \`hadPrimarySource\` | Provenance of data and documents                   |
| Schema.org  | \`hasPart\`        | Products, services, and other web entities           |
| NEN2660     | \`hasPart\`        | Civil products |

> **Semantic nuances:** 

The interesting part of decompositions turned up when, in a use case,
there was a suggestion to also have predicates like `canHavePart`.  On
a class level a predicate like that makes sense: we can indicate that
something may contain something else. On the instance level there is
something strange. The statement `my_bicycle canHavePart
my_front_wheel` actually does not have any factual value. The use case
was in an asset management context, and there the question is if the
whell is in my bicycle, which is a yes or no answer. There seems to be
no value in the fact that it can be there.

However a variant like: `I mayContain the_current_flu_virus`, which is
also a ’may’ or ’can’ kind of predicate, does have value: people might
avoid contact with me, because of the fact that I cannot exclude
having the contagious virus.

So it seems that the `canHave` `mayContain` etc predicates have different value when used in instance relations.
