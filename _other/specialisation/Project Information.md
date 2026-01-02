---
title: Project Information
layout: home
nav_order: 1
collection: Other Things
parent: Specialisation
---

Also in the area of project information specislisation can help. 

## Specializing workpackages
Especially when using waterfall project management techniques (and you would/should when endstates are clear), the archimate elements can be specialized to more meaningfull objects:

| WBS Element     | ArchiMate Element    | Specialization (Stereotype) | Logic / Relationship                                                      |
|-----------------|----------------------|-----------------------------|---------------------------------------------------------------------------|
| Project         | Work Package         | «project»                   | The top-level container for all actions.                                  |
| Phase           | Work Package         | «phase»                     | A Work Package composed of smaller work packages via Composition.         |
| Deliverable     | Deliverable          | «deliverable»               | A passive structure element produced by a Work Package.                   |
| Work Package    | Work Package         | «work package»              | The smallest assignable unit of work in ArchiMate.                        |
| Task / Activity | Work Package         | «task»                      | Modeled as the lowest-level Work Package or sometimes a Business Process. |
| Milestone       | Implementation Event | «milestone»                 | An instantaneous state change (e.g., "Phase Gate Passed")                 |
|-----------------|----------------------|-----------------------------|---------------------------------------------------------------------------|


In Archimate, for the specialized elements:

![Sources](../../../../assets/Project specialisations.png)


## Phases and Projects (The Containers)

Since ArchiMate only has one primary behavior element for implementation—the Work Package, you distinguish between a "Project" and a "Phase" by nesting them.

- Example: A Work Package named "Construction Project" composes a Work Package named "Foundation Phase."

![Sources](../../../../assets/wp1example.png)	

Or:

![Sources](../../../../assets/wp2example.png)	


{: .note }
*Deliverables (The "What")*\
In Waterfall, every level of the WBS should result in a deliverable. In ArchiMate, you use the Realization Relationship to show this:\
\
The Work Package (Behavior) Realizes the Deliverable (Passive Structure).\
\
*Relationship to the Core*\
\
To show how these "Normal" project elements affect your actual business, you link them to the Core Layers:
\ 
Work Package → Realizes → Capability (Strategy Layer)\
\
Deliverable → Realizes → Application Component or Business Object (Core Layers)\


