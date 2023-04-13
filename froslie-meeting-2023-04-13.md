# Froslie meeting 2023-04-13

## Agenda
max gives a small project status update
chris gives a tour of his cool markdown parser and things he has learned
jenny and alec will give a update on their PR's and what the plan is for the end of the semester.

## Status Update

on track to finish three large PR's by the end of the semester.

## Markdown parser showcase

the old markdown parser had library it depended on going unmaintained, and so the decision was made to rewrite it in rust.

Currently have a skeleton that parses the AST(abstract syntax tree) of the markdown document, allowing them to perform checks on the abstract syntax tree, such as checking the validity of links.

## Progress on IP tables and future steps.

alec and jenny are working on implementing the ability to configure IPtables with kata-ctl, are more than halfway done with the implementation.

have implemented a subcommand to kata-ctl, as well as the ability to get and set IPtables for the running container.

when you first start a container, there is no firewall restrictions in place. The new kata-ctl command allows controlling the containers 'internal' IPtables from the host.

## Q&A

froslie asked about what the review process looks like, and how much time will pass between us finishing a task and the review passing through.

I asked how we explain what kata is and how to 'market' our project at the expo.
Froslie said that we should spend a good amount of space on explaining what kata is, what the deveopment process looks like, and how the open source development model enforces rigorous development process.
