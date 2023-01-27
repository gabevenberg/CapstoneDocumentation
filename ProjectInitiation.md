# Kata Containers Project Initiation Document.

Team Members:
* Alec Pemberton
* Gabe Venberg
* Juanaiga Okugas
* Maxwell Wendlandt

## Buisness Need

<!-- This should be the most stable and most important part of the document.  It should be 2-3 short paragraphs with a summary of the customer and the business need that you are intending to solve with the Capstone project.  This information should come from the customer through content they have provided or through discussions with the customer.  This should answer the ‘why’ question. -->

## Intended Solution

<!-- This should be 1-2 paragraphs describing a high level solution.  Many projects have clear requirements and a constrained solution to document here.  For projects that have research / exploratory / proof of concept elements, this section will be more focused on the process to reach a solution.  This should answer the ‘what’ question.  
Having an architecture diagram showing the key components that you will be building is an important part of this section.  This diagram will evolve over the project as more details emerge, but having it here is a good way to drive clarity. -->

## High Level Project Plan

<!-- Break the project down into the two key milestones as a starting point for the project.  This will evolve as the project goes, so don’t expect things to go as planned.  One important concept for Dev Phase 1 is the ‘steel thread’ that will demonstrate some part of the project in an end to end fashion.  Users and user stories can be introduced here to identify the high priority scenarios for the project.  Map these into Dev Phase 1 and Dev Phase 2. -->

## Technology Requirements
Due to Kata being a Linux and VM based project, building and testing the software that we are writing will require access to a Linux development environment for all team members.
In previous years, this was not a problem, as everyone in the team had personal linux machines.
However, this year, only one team member has a pre-existing linux machine.
Two other team members have desktops at home and are willing to dual boot from an internal drive.

However, the final two team members only own laptops, and are not able to dual boot.
Unfortunately, the university provided VM's are unsuitable for the tasks, as they themselves are virtual machines, and do not have nested virtualization availible.
This leaves us with two options.

First, we could directly provide two development laptops to the team members.
These machines need not be very high spec, 4-8gb of ram and any cpu after around 2015 should work well.
This is the preferred solution.

Secondly, we could have a server running that both team members (or potentially all of us) can remote into, via ssh or remote desktop.
The server would need to either be running on bare metal, or support nested virtualization.
Additonally, certan permissions may be required, at the very least permission to create and manage virtual machines, and potentially up to root acess.
The machine would also require a network connection to the outside world, including the ability for use to remote in from off the NDSU network.
The server would need at least 1 core per user, and at least 4gb of ram per user.

The first option is certanly more ideal, but the second option will be easier to pitch to IT, as they retain physical control of the hardware. (on the other hand, they may be a bit uppity about us having root acess to a device that is visible to the outside.)

<!-- This section should indicate what technology frameworks are required for the project by the client.  This would include things like the use of cloud computing from a specific company, frameworks like .Net or React, programming languages, emulators, test frameworks, etc.  It’s important to highlight any client requirements that the project team doesn’t have access to directly.  Are there subscriptions or licenses required?  Suggested training for the technology requirements should also be considered. -->

## Project and Infrastrucutre Requirements

<!-- This section should include infrastructure needs for the project such as specific tools for backlog tracking or issue tracking.  You should clarify what documentation is required by the client beyond the project initiation and backlog documents that the class requires.  You should expect some additional requirements or design documents, for example.  How should requirements be specified?  Are UML or other diagrams required for the design?
The section should include technical infrastructure such as source code control expectations, build frameworks, etc.  Again, it’s essential to highlight any client requirements that the project team doesn’t have access to.  Training should be considered as appropriate. -->

## Key Chalenges and Risks

<!-- Every project has a set of unknowns and risks and it’s important to prioritize these early in the project.  List the key challenges and risks in this section. -->
