---
ressource:
  - ✉️ Discussion de forum
author:
  - "[[Valentina Cupac]]"
link:
  - https://groups.google.com/g/growing-object-oriented-software/c/_HpFjf_L_D0
trello: 
relates:
  - "[[Test Unitaire]]"
---
Cet article répond à la quesiton "c'est quoi l'unité dans un test unitaire" ?

> Hi Steve,
>
> Thanks for your helpful clarifications in the past.
>
> I now have some additional questions - clarifications regarding formal definitions.
>
> **Current mainstream definition**
>
> In the book Unit Testing (https://freecontent.manning.com/what-is-a-unit-test-part-2-classical-vs-london-schools/), the distinction regarding the definition of a unit was as follows:
> London school --> Unit is "A class."
> Classical school --> Unit is a "A class or a set of classes."
> (That's also the approach in Fowler's article https://martinfowler.com/bliki/UnitTest.html class isolation)
>
> **London school - Original definitions**
>
> Going back to the original GOOS book I found these quotes when searching for cluster & composite:
>     * Chapter 5 "Unit tests... exercise objects, or small clusters of objects"
>     * Chapter 6: "Internals v. Peers. we must decide what is inside and outside each object... Much of the point of an object... is to encapsulate access to its internals through its API" and "An object communicates with other objects in the system by sending and receiving messages... the objects it communicates with directly are its peers"... also "The composite object's API must hide the existence of its component parts and the interactions between them, and expose a simpler abstraction to its peers."
>
> **Conclusion**
>
> Based on the above, this leads me to the following conclusion (by the original definition in GOOS) that, in the London school.
>     * In many places on the internet (and books) the statement is that the class (object) is the unit in London school
>     * But based on the actual definitions in GOOS, the **composite** class (**composite** object) is the unit
>
> This composite class may consist of just one class or it might consist of a cluster of classes. So the word Internals is referring to those internal classes which are inside the cluster, but not exposed externally.
>
> I'm interested to hear your thoughts about this interpretation, i.e. if it's correct statement of the interpretation from the GOOS book.
>
> Thanks in advance,
> Valentina
>
> P.S. Also thanks to Joseph too for providing useful insights today regarding mocks.
> ---
> ###
> Chengwei Lin
>
> From my study of GOOS, the entry point of a unit test is always a class (calling a method of it), but the verification often involves its interaction with its dependency class(es). The main purpose of unit tests is for us to design well-defined interfaces between classes, based on SRP (Single Responsibility Principle) and by the help of mock objects. So the resulting OO design is loosely coupled.
>
> To me, it seems understanding the above purpose of unit tests is more important than struggling with the precise definition and the boundary of a unit.
>
> Just a sharing of my thought.
>
> Thanks,
>
> Chengwei
> ---
> ### Steve Freeman
> 
> Agreed.