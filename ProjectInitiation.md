# Kata Containers Project Initiation Document.

Team Members:
* Alec Pemberton
* Gabe Venberg
* Juanaiga Okugas
* Maxwell Wendlandt

## Buisness Need

<!-- Kata is an open source hybrid container/VM runtime.

Kata-ctl.
the successor to kata-runtime (used to be the runtime, but is now only a utility)
For the new runtime-rs, kata needs a rust version of the kata-runtime utility that covers the new featureset.

rust runtime. Will have minimum viable product, but obviously more than the minimum viable product is eventually needed. We have an existing 'reference implementation', meaning the old go implementaiton, but the new implementaiton will not be a 1 for 1 translation, as the goal is to also improve cloud hypervisor integration.
the runtime has a built in hypervisor, but in order for it to achive feature parity with the go runtime, it should also be able to use an external hypervisor. -->

<!-- This should be the most stable and most important part of the document.  It should be 2-3 short paragraphs with a summary of the customer and the business need that you are intending to solve with the Capstone project.  This information should come from the customer through content they have provided or through discussions with the customer.  This should answer the ‘why’ question. -->

## Intended Solution

<!-- For kata-ctl, we will be working with the old go codebase in order to map the featuresets of kata-runtime to kata-ctl.
The go codebase is... hairy in places, so some minor re-architecting of the program might be needed.

for runtime-rs, we will be working off of james' minimum viable product and adding what features are needed.

additionally, we will be working on misclanious issues on the github repository in order to familiarize ourselves with the kata codebase and community. -->

<!-- This should be 1-2 paragraphs describing a high level solution.  Many projects have clear requirements and a constrained solution to document here.  For projects that have research / exploratory / proof of concept elements, this section will be more focused on the process to reach a solution.  This should answer the ‘what’ question.
Having an architecture diagram showing the key components that you will be building is an important part of this section.  This diagram will evolve over the project as more details emerge, but having it here is a good way to drive clarity. -->

## High Level Project Plan

<!-- Break the project down into the two key milestones as a starting point for the project.  This will evolve as the project goes, so don’t expect things to go as planned.  One important concept for Dev Phase 1 is the ‘steel thread’ that will demonstrate some part of the project in an end to end fashion.  Users and user stories can be introduced here to identify the high priority scenarios for the project.  Map these into Dev Phase 1 and Dev Phase 2. -->

## Technology Requirements

<!-- This section should indicate what technology frameworks are required for the project by the client.  This would include things like the use of cloud computing from a specific company, frameworks like .Net or React, programming languages, emulators, test frameworks, etc.  It’s important to highlight any client requirements that the project team doesn’t have access to directly.  Are there subscriptions or licenses required?  Suggested training for the technology requirements should also be considered. -->

## Project and Infrastrucutre Requirements

<!-- This section should include infrastructure needs for the project such as specific tools for backlog tracking or issue tracking.  You should clarify what documentation is required by the client beyond the project initiation and backlog documents that the class requires.  You should expect some additional requirements or design documents, for example.  How should requirements be specified?  Are UML or other diagrams required for the design?
The section should include technical infrastructure such as source code control expectations, build frameworks, etc.  Again, it’s essential to highlight any client requirements that the project team doesn’t have access to.  Training should be considered as appropriate. -->

## Key Challenges and Risks

<!-- Every project has a set of unknowns and risks and it’s important to prioritize these early in the project.  List the key challenges and risks in this section. -->

No one in the group has much experience with most of the software we are meant to work with. As of now, we are all facing the challnege of learning Git, Rust, and Kata Containers itself. Another challenge we will inevitably face is rebasing the code itslef. After learning Rust, we will need to convert whatever Go code is assigned to us into Rust. This will undoubtedly bring up several challenges down the road.
