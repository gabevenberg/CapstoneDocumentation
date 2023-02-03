# Kata Containers Project Initiation Document.

Team Members:
* Alec Pemberton
* Gabe Venberg
* Juanaiga Okugas
* Maxwell Wendlandt
* Christopher Robinson

## Business Need

The "Why" for this project is that they need our help to convert the current code base that they are using which is written in the language called "rust", and they want us to take that code and convert it into the new language called "rust". Reason being is rust will be more efficient for them and is better suited for their newest feature set. After it all gets converted this will take the place of their service called "Kata-runtime".

If we happen to finish the Kata-ctl project our mentor is going to switch us to another project called Rust Runtime. Which already is coded but out job is to transcribe the "go" code to the new rust like before. We will not necessarily be coding 1 to 1 translation they want to help improve cloud hypervisor integration so if there is more efficient ways to do things we are supposed to implement them. Also need to make an external hypervisor work with the runtime, the runtime has a built in hypervisor, but in order for it to achieve feature parity with the go runtime, it should also be able to use an external hypervisor. On the customer side of things this will allow users access to light weight VMs that have the efficiency of a container with the security of a virtual machine (like the first project).

## Intended Solution

<!-- For kata-ctl, we will be working with the old go codebase in order to map the featuresets of kata-runtime to kata-ctl.
The go codebase is... hairy in places, so some minor re-architecting of the program might be needed.

for runtime-rs, we will be working off of james' minimum viable product and adding what features are needed.

additionally, we will be working on misclanious issues on the github repository in order to familiarize ourselves with the Kata codebase and community.-->

<!-- This should be 1-2 paragraphs describing a high level solution.  Many projects have clear requirements and a constrained solution to document here.  For projects that have research / exploratory / proof of concept elements, this section will be more focused on the process to reach a solution.  This should answer the ‘what’ question.

Having an architecture diagram showing the key components that you will be building is an important part of this section.  This diagram will evolve over the project as more details emerge, but having it here is a good way to drive clarity. -->

The Kata Containers project aims to enhance the current code base by transitioning it from the Go programming language to Rust. This transition is motivated by the desire to create a more efficient and performant solution that can support new features. Rust is a modern, systems-level programming language designed for high performance, low overhead, and improved security.

One of the key benefits of Rust is its ability to prevent crashes and null pointer dereferences, which are common security risks in Go. This makes Rust a great choice for the Kata Containers project, as it helps ensure the runtime's security and reliability. Additionally, Rust has better performance characteristics than Go, including faster runtime, lower latency, and increased parallelism, which are essential for systems-level programming.

In conclusion, the transition to Rust is an important step for the Kata Containers project, as it provides a platform for a more efficient and performant solution that can support new features. The team's objective is to translate code from the language Go to Rust in the development of Kata-CTL and Runtime-rs as they will be the successor to Kata-runtime and Runtime respectivly. The goal is to provide users with virtual machines that offer the performance and efficiency of containers with the security and isolation of a traditional virtual machine.

## High Level Project Plan
In our meetings with our mentors for this project, we were all able to figure out the key milestones for the starting point of this project: our first milestone would be learning the computer language rust and our second milestone is to be able to contribute our code to Kata wherever they need us. In depth, Kata Containers is looking for our team to help contribute code to their projects that will help translate their code to Rust and revamping Kata docs. We were given a timeline that they calculated to help us keep on track, which helps give us an idea what our first and second key milestones will be. For our first milestone, for four weeks of this project, we are to solely learn and code with Rust. In our first and second meeting, our mentors had given us resources and advice to better learn and understand the language, as many of us were not familiar with the language. The four weeks gives us time to not only learn, but be able to ask questions to our mentors for them to clarify and help us understand if we had any questions. During the four weeks, we are to setup a Linux environment and download Kata to start working with the Kata containers. Another part of the first milestone is to write our first one-liner PR. This one-liner PR is to check if git was configured correctly and get in contact with the PR reviewers.
 
For the second milestone, after having Kata downloaded and git configured, we are to start writing and making more significant contributions to their code. Currently, Kata is looking for our team to help contribute code to Kata-CTL, which will be written in the Rust language. Kata-Ctl will be the successor of Kata-runtime, a utility, where it will be converted to the rust language. This is mainly what Kata Containers would like from our team to contribute.
<!-- Break the project down into the two key milestones as a starting point for the project.  This will evolve as the project goes, so don’t expect things to go as planned.  One important concept for Dev Phase 1 is the ‘steel thread’ that will demonstrate some part of the project in an end to end fashion.  Users and user stories can be introduced here to identify the high priority scenarios for the project.  Map these into Dev Phase 1 and Dev Phase 2. -->

## Technology Requirements
Due to Kata being a Linux and VM based project, building and testing the software that we are writing will require access to a Linux development environment for all team members.
In previous years, this was not a problem, as everyone in the team had personal Linux machines.
However, this year, only one team member has a pre-existing Linux machine.
Two other team members have desktops at home and are willing to dual boot from an internal drive.

However, the final two team members only own laptops, and are not able to dual boot.
Unfortunately, the university provided VMs are unsuitable for the tasks, as they themselves are virtual machines, and do not have nested virtualisation available.
This leaves us with two options.

First, we could directly provide two development laptops to the team members.
These machines need not be very high spec, 4-8gb of ram and any cpu after around 2015 should work well.
This is the preferred solution.

Secondly, we could have a server running that both team members (or potentially all of us) can remote into, via ssh or remote desktop.
The server would need to either be running on bare metal, or support nested virtualisation.
Additionally, certain permissions may be required, at the very least permission to create and manage virtual machines, and potentially up to root access.
The machine would also require a network connection to the outside world, including the ability for use to remote in from off the NDSU network.
The server would need at least 1 core per user, and at least 4gb of ram per user.

The first option is certainly more ideal, but the second option will be easier to pitch to IT, as they retain physical control of the hardware. (on the other hand, they may be a bit uppity about us having root access to a device that is visible to the outside.)


<!-- This section should indicate what technology frameworks are required for the project by the client.  This would include things like the use of cloud computing from a specific company, frameworks like .Net or React, programming languages, emulators, test frameworks, etc.  It’s important to highlight any client requirements that the project team doesn’t have access to directly.  Are there subscriptions or licenses required?  Suggested training for the technology requirements should also be considered. -->

## Project and Infrastructure Requirements

<!--
* git
* github
	* github issues
	* github pull requests
	* github projects
* cargo
* no real design docs
* markdown documentation
-->

While the Kata community does not use traditional UML diagrams or other such formal documentation,
the project is extremely well documented with markdown documents describing how Kata works and how it is used.
For any code that we write that changes functionality, we would be expected to update the relevant documentation as well.
Documentation of design and design process primarily exists through the heavy usage of the GitHub workflow, using issues that are fixed by pull requests with discussion at every step of the pull request process thoroughly documents the rationale behind any change.

As for source control, git is used to document all code changes and history, as well as using the aforementioned GitHub and pull requests to document the reasons behind them.

The build system is extremely simple on our end, simply running cargo build in order to compile the program locally. Kata does have a CI system in place, so further checks will be carried out before any code is merged into the master branch.

<!-- This section should include infrastructure needs for the project such as specific tools for backlog tracking or issue tracking.  You should clarify what documentation is required by the client beyond the project initiation and backlog documents that the class requires.  You should expect some additional requirements or design documents, for example.  How should requirements be specified?  Are UML or other diagrams required for the design?
The section should include technical infrastructure such as source code control expectations, build frameworks, etc.  Again, it’s essential to highlight any client requirements that the project team doesn’t have access to.  Training should be considered as appropriate. -->

## Key Challenges and Risks

<!-- Every project has a set of unknowns and risks and it’s important to prioritize these early in the project.  List the key challenges and risks in this section. -->

No one in the group has much experience with most of the software we are meant to work with. As of now, we are all facing the challnege of learning Git, Rust, and Kata Containers itself. Another challenge we will inevitably face is rewriting the code itself. After learning Rust, we will need to convert whatever Go code is assigned to us into Rust. This will undoubtedly bring up several challenges down the road.
