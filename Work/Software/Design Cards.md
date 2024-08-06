---
ressource:
  - 🃏 Cartes
author: 
link:
  - https://design-types.net/cards_get_them.html
trello: 
relates:
  - "[[Design Knights]]"
  - "[[Software Design]]"
---
## Card-based Discussions

**Use Case**
Use this when discussions about software design are not productive because:
• some participants have difficulties to ex- press their thoughts 
• the discussion itself lacks sound argumentation or 
• a single developer dominates the discussion. 

**Preparation**
1) Start with reading the cards carefully and get familiar with the arguments. 
2) Start with the basic set ( ) and build a deck of not more than 20 cards. 
3) Each developer participating in the discussion should have an own deck. 
**Basic Rules**
1) When you play a card, explain how this argument is applied in the concrete situation. 
2) You may only play one card at a time. Then it's your colleague’s turn. Either use one card from your deck or the card your col- league has just played. 
3) You can also play a question or action card but also only one at a time.

## Dimensions
There are four dimensions: 
- simple vs. powerful (green) 
- abstract vs. concrete (blue) 
- pragmatic vs. idealistic (red) 
- robust vs. technologic (yellow)
Each dimension represents two contrary but related perspectives on design and each argument card provides a distinct aspect relevant from this perspective

- **simple** stands for simple solutions, no magic, nothing sophisticated but easy to read and maintain.
- **powerful** stands for foresighted solutions, generic and flexible. 
- **abstract** stands for having the big picture in mind and keeping the bird’s eye view. 
- **concrete** stands for knowing the details, being able to breathe code likea fish can breathe water.
- **pragmatic** stands for creating value with a very customer-focused perspective. 
- **idealistic** stands for focusing on quality and professionalism, for avoiding dirty hacks and 80 percent solutions. 
- **robust** stands for stability and reduction of risks. 
- **technologic** stands for the potential new tech- nology offers.

# Axes

## Simple vs. Powerful

### Simple

Developers with this attitude prefer simple solutions which are easy to write and to maintain.

The main idea is avoiding complexity. To prefer simple solutions means to implement only necessary and requested things without any frills. Simple code is easier to read, better to maintain, and cointains fewer bugs. Typical followers know about the power of simplicity. The key to handling complexity is not to master it but rather to avoid it. They prefer small and clear modules with few dependencies. They use libraries and frameworks if this makes the code easier to read and write and they don't use them if this only means that the reader of the code needs to know how all these libraries work. Explicit solutions are preferred to indirect, declaratrive ones. This means that simple solutions are not overly generic but they communicate the intent well.

On the other hand simple design tends to be less foresighted. This makes frequent changes and refactorings necessary. While this is not a problem for a single class, it may become one when interfaces to other teams are affected. Simple and explicit solutions often tend to be tightly coupled to requirements, used libraries and external dependencies. Decoupling introduces complexity (additional abstraction layers, indirect calls, etc.) but it also provides flexibility. This flexibility is sometimes underused by simple developers.

Simple developers typically follow the following principles: 
- [KISS](http://www.principles-wiki.net/principles:keep_it_simple_stupid)
- [MIMC](http://www.principles-wiki.net/principles:more_is_more_complex)
- [YAGNI](http://www.principles-wiki.net/principles:you_ain_t_gonna_need_it)
- [RoE](http://www.principles-wiki.net/principles:rule_of_explicitness)
- [PLS](http://www.principles-wiki.net/principles:principle_of_least_surprise)

Rather disregarded principles for these developers are:
- [GP](http://www.principles-wiki.net/principles:generalization_principle)
- [LC](http://www.principles-wiki.net/principles:low_coupling)

### Powerful

Developers with this attitude prefer powerful, flexible, and foresighted solutions.

The main idea is to create flexible and foresightes solutions. Generalized solutions can be applied for several use cases by just customizing or configuring them. Followers typically include flexibility and extensibility naturally into software design. Powerful developers like runtime configurability, powerful frameworks, decoupling, and the use of many design patterns. They think ahead and include thoughts on extensibility, performance, and portability into their design process. This keeps structures and interfaces stable and helps reducing effort imposed by changing requirements inthe future.

On the other hand powerful solutions take much time especially for their initial creation. Some of the flexibility might never be used so one could argure that introducing it was unnecessary effort. Powerful developers may tend also to get lost in providing flexibility instead of fulfilling requirements. Powerful code is flexible and foresighted but it is also hard to read and to understand. Furthermore complex and powerful solutions are more error-prone than simple ones.

Powerful developers typically follow the following principles: 
- [GP](http://www.principles-wiki.net/principles:generalization_principle)
- [ECV](http://www.principles-wiki.net/principles:encapsulate_the_concept_that_varies)
- [IH/E](http://www.principles-wiki.net/principles:information_hiding_encapsulation)
- [DIP](http://www.principles-wiki.net/principles:dependency_inversion_principle)
- [LC](http://www.principles-wiki.net/principles:low_coupling)

Rather disregarded principles for these developers are: 
- [KISS](http://www.principles-wiki.net/principles:keep_it_simple_stupid)
- [MIMC](http://www.principles-wiki.net/principles:more_is_more_complex)
- [YAGNI](http://www.principles-wiki.net/principles:you_ain_t_gonna_need_it)
- [RoE](http://www.principles-wiki.net/principles:rule_of_explicitness)

## Abstract vs. Concrete

### Abstract

Developers with this attitude think in terms of abstractions and concepts.

Abstract developers always have the big picture in mind. They think in terms of abstraction layers, patterns, package dependencies, architectural constraints, etc. Structure is very important and abstract developery keep the structure clean and clearly arranged. Single lines of code are not impotent. You shouldn't look at a software system with a magnifying glass. It has to work as a whole and it can be understood as a whole. Abstract solutions follow clear concepts that are easy to understand and fundamental to the whole system. Followers have a very good overview over the whole system. Furthermore they are also able to give advice on consequences of particular changes. Often abstract developers also like having natural, requirements-based object-designs where the software structure mimics the real-world concepts. This can make understanding the code even easier and may lead to fewer code changes when requirements change.

On the other hand abstract developers typically don't like working with legacy code that has bad structure. They feel the need to understand the system as a whole and will try to refactor the code such that there is a clear structure. If there is time for that and the system will be maintained further, this is a good thing. In the other cases an abstract developer will feel lost and will be unhappy with making changes to that code which he doesn't quite understand.

Abstract developers typically follow the following principles: 
- [LC](http://www.principles-wiki.net/principles:low_coupling)
- [TdA/IE](http://www.principles-wiki.net/principles:tell_don_t_ask_information_expert)
- [PSU](http://www.principles-wiki.net/principles:principle_of_separate_understandability)
- [IH/E](http://www.principles-wiki.net/principles:information_hiding_encapsulation)
- [SLA](http://www.principles-wiki.net/principles:single_level_of_abstraction)
- [MP](http://www.principles-wiki.net/principles:model_principle)
- [UP](http://www.principles-wiki.net/principles:uniformity_principle)

Rather disregarded principles for these developers are: [RoE](http://www.principles-wiki.net/principles:rule_of_explicitness), [ECV](http://www.principles-wiki.net/principles:encapsulate_the_concept_that_varies), and [YAGNI](http://www.principles-wiki.net/principles:you_ain_t_gonna_need_it)

### Concrete

Developers with this attitude directly think in terms of code.

Concrete developers directly transfer requirements into code. They are also good at working with and refactoring legacy code that they do not understand completely. They don't have to understand the whole system in all its details and they know that this attitude wouldn't scale either. As soon as a system has a certain level of complexity, one mind cannot understand it fully. Nevertheless a concrete developer can work quite well with such a system. When they refactor they heavyly rely on the boyscout rule. They improve code bottom-up rather than planning it top-down.

On the other hand concrete developers may overoptimize unnecessary details and tend to lose sight of the big picture. They may violate achitectural constraints and weaken the overall structure because thinking in terms of packages, layers and dependencies is not in their focus.

Concrete developers typically follow the following principles: 
- [DRY](http://www.principles-wiki.net/principles:don_t_repeat_yourself)
- [HC](http://www.principles-wiki.net/principles:high_cohesion)
- [SRP](http://www.principles-wiki.net/principles:single_responsibility_principle)
- [ECV](http://www.principles-wiki.net/principles:encapsulate_the_concept_that_varies)
- [OCP](http://www.principles-wiki.net/principles:open-closed_principle)

Rather disregarded principles for these developers are: 
- [MP](http://www.principles-wiki.net/principles:model_principle)
- [TdA/IE](http://www.principles-wiki.net/principles:tell_don_t_ask_information_expert)
- [PSU](http://www.principles-wiki.net/principles:principle_of_separate_understandability)
- [LSP](http://www.principles-wiki.net/principles:liskov_substitution_principle)

## Pragmatic vs. Idealistic
### Pragmatic

Developers with this attitude focus on time to market.

The main motivation of such developers is to fulfill the requested requirements as soon as possible. It's the result that counts so tasks are only done if there is a valuable benefit. This approach prevents complexity and overengineering. Furthermore they can use the saved time to implement even more features and deliver benefit to the customer even faster. Followers do not like to reinvent the wheel and use templates, code snippets, etc. to avoid implementing everything by their own. This normally leads to faster solutions and success. Freed from technical or structural sensitivities followers of this dimension adapt very fast to any new environment, rules or specifications for example to a new team. They are also able to bring others down to earth and redirect them to the primary goal.

On the other hand pragmatic developers tend to neglect code quality. So while pragamtic developers are really fast at the beginning, they may be slower in the long run as maintainability decreases, bugs show up more often and the code gets less readable.

Pragmatic developers typically follow the following principles: 
- [YAGNI](http://www.principles-wiki.net/principles:you_ain_t_gonna_need_it)
- [RoE](http://www.principles-wiki.net/principles:rule_of_explicitness)
- [KISS](http://www.principles-wiki.net/principles:keep_it_simple_stupid)
- [MIMC](http://www.principles-wiki.net/principles:more_is_more_complex)

Rather disregarded principles for these developers are:
- [UP](http://www.principles-wiki.net/principles:uniformity_principle)
- [GP](http://www.principles-wiki.net/principles:generalization_principle)
- [MP](http://www.principles-wiki.net/principles:model_principle)
- [LSP](http://www.principles-wiki.net/principles:liskov_substitution_principle)
- [IH/E](http://www.principles-wiki.net/principles:information_hiding_encapsulation)
- [DIP](http://www.principles-wiki.net/principles:dependency_inversion_principle)
- [LC](http://www.principles-wiki.net/principles:low_coupling)
- [HC](http://www.principles-wiki.net/principles:high_cohesion)
- [TdA/IE](http://www.principles-wiki.net/principles:tell_don_t_ask_information_expert)
- [EUHM](http://www.principles-wiki.net/principles:easy_to_use_and_hard_to_misuse)
- [IAP](http://www.principles-wiki.net/principles:invariant_avoidance_principle)

### Idealistic

Developers with this attitude prefer clean solutions.

The main motivation of these developers is the observation that while bad quality can be ignored for a short period of time, it is a serious threat in the long run. So idealistic developers like doing things either right or not at all. Idealistic developers care for the software they write and fight for it with all their expertise and professionalism. It is their job to fight this fight against the odds of deadlines, management, and project schedules. It is not enough to finish a project on-time. If the software dies shortly after the "successful" completion of the project, it is still a failure. Idealistic developers know that and will produce high-quality software that works even after the project managers have left for another project.

On the other hand idealsitic developers sometimes lose focus on the real requirements and on economical aspects. Software needs to be maintainable but in most cases it doesn't need to be perfect. Idealistic developers sometimes spend too much time on perfection. Furthermore discussions with idealistic developers sometimes can be exhausting and are not always productive. Idealsitic developers work well with others who think similarly but working with other developers who are also idealistic but rather different in in the other dimensions can become quite difficult.

A unique property of idealictic developers is that their idealism increases the advantages and disadvantages of the other attributes. So a simple idealistic developer will strive for perfection in simplicity and a powerful idealistic developer will create even more powerful software, etc.

Idealistic developers typically follow the following principles: 
- [UP](http://www.principles-wiki.net/principles:uniformity_principle),
- [PSU](http://principles-wiki.net/principles:principle_of_separate_understandability),
- [DRY](http://www.principles-wiki.net/principles:don_t_repeat_yourself),
- [IH/E](http://www.principles-wiki.net/principles:information_hiding_encapsulation), 
furthermore being idealistic adds even more weight on the principles you favor because of the other dimensions

Rather disregarded principles for these developers are: 
- [YAGNI](http://www.principles-wiki.net/principles:you_ain_t_gonna_need_it)
- [RoE](http://www.principles-wiki.net/principles:rule_of_explicitness)
although this heavyly depends on the other dimensions

## Robust vs. Technologic
### Robust

Developers with this attitude prefer stabe solutions which stood the test of time.

Software needs to be stable, maintainable, and robust. It's the responsibility of the software developer to ensure that the software has this qualities. Technologies come and go. Most of them are just hypes, just another magic cure for an illness which almost nobody really has, or just a variation of an old idea. Some of them are valuable and some of them aren't. When they arise it is very difficult to tell that apart. But sooner or later time will show what will survive, what can be safely adapted and what isn't even worth a try. New technology may be fancy and fun but often ist's not wise to adapt them too early. Even if they prove to be a good idea, in the beginning they will be volatile, badly documented and not well understood. Robust developers know about that, they are patient and only adapt those technologies which are worthwhile. This saves them time as they don't have to relearn everything every now and then and as the experiments are done by other people. This free time can be used to harden the software, to implement decent logging, monitoring, and exception handling. Robust developers program defensively, document wisely, and strive for homogeneous, standardized solutions.

On the other hand robust developers easily get left behind. They fear the future and rather stick to old and outdated technology. Thus they don't profit from what others already have achieved and do their own thing just as they've always done it. They don't like changing their ways of thinking and it takes considerable time for them to adapt to new working environments. Furthermore always thinking about what could go wrong, all the defensive programming, parameter checking, and exception handling take their time to implement and impose a considerable amount of complexity. To others they seem like the ones who don't evolve and slow down everything.

Robust developers typically follow the following principles: 
- [ML](http://principles-wiki.net/principles:murphy_s_law),
- [EUHM](http://www.principles-wiki.net/principles:easy_to_use_and_hard_to_misuse),
- [UP](http://www.principles-wiki.net/principles:uniformity_principle),
- [RoE](http://www.principles-wiki.net/principles:rule_of_explicitness), 
- [IH/E](http://www.principles-wiki.net/principles:information_hiding_encapsulation)

Rather disregarded principles for these developers are: 
- [KISS](http://www.principles-wiki.net/principles:keep_it_simple_stupid)
- [LC](http://www.principles-wiki.net/principles:low_coupling)

### Technologic

Developers with this attitude prefer technically advanced solutions.

Technologic developers embrace the fact that lifelong learning is an essential part of their job. Technology evolves faster and faster, new technologies arise, new methodologies become popular, and bad habits slowly die out. New technology can make you more productive and enable you to do things that weren't possible before. They can be your key advantage over your competitor. Technologic developers are open-minded for technological improvement and new ideas. Likewise they continuously try to improve themselves just like they try to improve their code.

On the other hand technologic developers risk riding the wrong horse. Sometimes they experiment too much, invest too much time in learning the wrong technologies and risk the stability and maintainability of their code. Although they are very creative, this ceativity may lead to unnecessarily complex solutions and especially to ones which are hardly understandable by those who don't know all the technologies used. Technologic developers need to play around and feel uncomfortable when they don't get enough freedom. They don't play it safe, they take risks. Sometimes they win and sometimes they lose.

Technologic developers typically follow the following principles: 
- [GP](http://www.principles-wiki.net/principles:generalization_principle)
- [LC](http://www.principles-wiki.net/principles:low_coupling)
- [ML](http://principles-wiki.net/principles:murphy_s_law)
- [DRY](http://www.principles-wiki.net/principles:don_t_repeat_yourself)

Rather disregarded principles for these developers are: 
- [RoE](http://www.principles-wiki.net/principles:rule_of_explicitness)
- [UP](http://www.principles-wiki.net/principles:uniformity_principle)
- [MIMC](http://www.principles-wiki.net/principles:more_is_more_complex)

# 🃏 Liste des cartes

## KISS - Keep it Simple Stupid

> Simple

**Short Description:**  
*Simple means readable, maintainable and less error-prone. Overengineering is harmful.*  
Simple signifie lisible, maintenable et moins sujet aux erreurs. La suringénierie est néfaste.

**Long Description:**  
*Complex code typically contains more bugs and it has to be maintained (maybe even by other people). To others it may seem obscure which can lead to frustration and bad code quality. Striving for simplicity means to avoid inheritance, low-level optimization, complex algorithms, fancy (language) features, configurability, etc.*
Le code complexe contient généralement plus de bogues et doit être maintenu (peut-être même par d'autres personnes). Pour d’autres, cela peut sembler obscur, ce qui peut entraîner de la frustration et une mauvaise qualité de code. Rechercher la simplicité signifie éviter l'héritage, l'optimisation de bas niveau, les algorithmes complexes, les fonctionnalités (langagières) sophistiquées, la configurabilité, etc.

Le principe KISS prône la **simplicité** dans la conception et l'exécution. L'idée est d'éviter toute complexité inutile et de se concentrer sur l'essentiel. En d'autres termes, il s'agit de trouver la solution la plus simple et la plus efficace à un problème donné.

## YAGNI - You Ain’t Gonna Need It

> Simple
> https://design-types.net/c/YAGNI

**Short Description:**  
It’s currently not necessary, and we even have to maintain it!

**Long Description:**  
Code needs to be maintained. The more you have, the more complexity there will be. Adding features and capabilities that are not used (yet), wastes time twice: When you write the code and when you change or just read it. This becomes even more painful when you finally try to remove this dead code. So avoid runtime-configuration, premature optimization, and features that are only there “for the sake of completeness”. If they are needed, add them later.

**YAGNI** est l'acronyme de **"You Ain't Gonna Need It"**, ce qui signifie en français "Vous n'en aurez pas besoin". C'est un principe issu de l'Extreme Programming (XP) qui préconise de **ne pas ajouter de fonctionnalités à un logiciel tant qu'elles ne sont pas absolument nécessaires**.

## EUHM - Easy to Use and Hard to Misuse

> Simple
> https://design-types.net/c/EUHM

**Short Description:**  
It shouldn’t require much discipline or special knowledge to use or extend that module.

**Long Description:**
Some day there will be a new colleague who hasn’t read the docs. Some day it will be Friday evening right before the deadline. No matter how disciplined or smart you are, some day somebody will cut corners. So better have the obvious way of usage be the correct one. Have the compiler or the unit tests fail in case of errors and keep sure that changing a module does not require much understanding.

Le principe "Easy to Use and Hard to Misuse" (Facile à utiliser et difficile à mal utiliser) est un concept de conception qui vise à créer des interfaces utilisateur et des systèmes qui sont à la fois **intuitifs** pour les utilisateurs novices et **robustes** face aux erreurs potentielles.

**L'objectif principal est de minimiser les risques d'erreurs d'utilisation et d'améliorer l'expérience utilisateur globale.**

## RoE - Rule of Explicitness

> Simple
> https://design-types.net/c/RoE

**Short Description:**  
Explicit solutions are less error-prone and easier to understand and debug.  

**Long Description:**  
Implicit solutions require the developer to have a deeper understanding of the module, as it is necessary to “read between the lines”. Explicit solutions are less error-prone and easier to maintain. So better avoid configurability, unnecessary abstractions and indirection (events, listeners, observers, etc.).

**La règle de l'explicitation**, bien qu'elle n'ait pas de traduction littérale aussi concise en français que l'anglais "Rule of Explicitness", est un principe fondamental en programmation qui prône la **clarté** et la **concision** dans le code. En essence, cette règle suggère que le code doit être écrit de manière à ce que son **intention** soit **évidente** pour quiconque le lit, même si cette personne n'est pas familière avec le projet dans son ensemble.
"Explicit over Implicit" : Privilégier l'explicite à l'implicite en programmation
Le principe "Explicit over Implicit", souvent traduit par "Privilégier l'explicite à l'implicite", est une pratique de programmation qui encourage à rendre le code aussi clair et explicite que possible. Cela signifie que les intentions du programmeur doivent être clairement exprimées dans le code, laissant le moins de place possible à l'interprétation.

## RoP - Rule of Power

> Powerful
> https://design-types.net/c/RoP

"Qui peut le plsu, peut le moins"

**Short Description**
Foresighted, generic solutions are reusable and future requirements will be addressed, too.  

**Long Description**
A powerful solution is better than a less potent one. Foresighted solutions reduce the necessity of refactoring and are more stable over time. Generic solutions often need less code and additionally offer extensibility by design. So better use abstractions, indirection, GoF patterns, polymorphism, etc.

## FP - Flexibility Principle

> Powerful
> https://design-types.net/c/FP

Short Description:  
We have to make sure that we can change that later on.  
Long Description:  
While it is often not necessary to implement a fully generic solution, in many cases it is important to be flexible. Even if a generic solution isn’t implemented right away, it must still be possible to do so. E.g. if you don’t want to implement runtime-configurability, at least have a constant ready to be made configurable. Make sure that the solution does not spoil or hinder future changes or enhancements.

## NFR - Non-Functional Requirements

> Powerful
> https://design-types.net/c/NFR

Short Description:  
We have to think about NFRs now. Adding these qualities later will be very hard.  
Long Description:  
Software needs to be efficient, scalable, secure, usable, maintainable, testable, resilient, reliable, compliant with (data privacy) regulations, etc. These qualities have a huge impact on the architecture. You might need to choose certain technologies for performance, use microservices for scalability, or provide redundant subsystems for reliability. Thinking about this later results in waste and additional cost/effort.

## ECV - Encapsulate the Concept that Varies

> Powerful
> https://design-types.net/c/ECV

**Short Description**
Encapsulate the Concept that Varies

**Long Description**
If you have to change your software, you’d like those changes to be isolated, so you don’t have to change half your system. So put the chang-ing parts into separate modules. Isolate chang-ing APIs via gateway classes, data access tech-nology using DAOs, encapsulate algorithms using the strategy pattern, etc. Conversely, don’t use abstractions for those parts that won’t change.

## LC - Low Coupling

> Abstract
> https://design-types.net/c/LC 

Voir aussi [[Couplage]].

**Short Description**
Tight coupling creates ripple-effects and makes the code less maintainable.

**Long Description**
If you decouple, you don’t need to know internal details about other parts of the system. Furthermore, it makes you independent of changes in those other parts and it even enables reuse. So better reduce the number of dependencies and assumptions about other modules, use narrow interfaces, additional layers, indirection, dependency injection, observers, messaging, etc.

## SRP - Single Responsibility Principle

> Abstract
> https://design-types.net/c/SRP

Voir aussi[[Single Responsibility Principle|SRP]]

**Short Description**
One module should do one thing only.

**Long Description**
If there is more than one reason to change a certain module (method/class/artifact/...), i.e. the module has more than one responsibility, then code becomes fragile. Changing one responsibility may result in involuntary changes to the other. Furthermore, changing the module is more difficult and takes more time. And even when you don’t change the module at all, understanding it is more complex. So better separate concerns into separate modules.

## ADP - Acyclic Dependencies Principle

> Abstract
> https://design-types.net/c/ADP

**Short Description**  
Cyclic dependencies create rigid structures.

**Long Description**
Cyclic dependencies result in all sorts of nasty consequences: tight couplings, deadlocks, infinite recursions, ripple effects, bad maintainability, etc. The larger the cycle, the worse the consequences will get and the harder they are to understand and to break apart. So avoid them by using dependency inversion, publish-subscribe mechanisms or just by assigning responsibilities to modules hierarchically.

## IOSP - Integration Operation Segregation Principle

> Abstract
> https://design-types.net/c/IOSP

Short Description  
A module should either contain business logic or integrate other modules but not both.

Long Description
Either a module (method/class/...) is an operation, i.e. it contains business logic and/or API calls or it is an integration, i.e. it calls other modules. That means operations should never call other modules and integrations should have no business logic and no API calls. Operations are easy to read, test, and reuse. And integrations are very simple, too. This ensures that modules are small and systems well-structured.

## DRY - Don’t Repeat Yourself

> Concrete
> https://design-types.net/c/DRY

Short Description:  
Duplication makes changing the code cumbersome and leads to bugs.  
Long Description:  
Having a functionality more than once means to update or bugfix it at every occurrence which is more error-prone and more effort. Refactorings like method or class extraction may help as well as inheritance, higher-order functions, polymorphism, and some design patterns.
## IH/E - Information Hiding/Encapsulation

> Concrete
> https://design-types.net/c/IH_E

Short Description:  
Only what is hidden, can be changed without risk.  
Long Description:  
There are 3 levels of IH/E: 1) Having a capsule means, that you have methods for accessing the data of the module. 2) Making the capsule opaque means that you can only access the data through the methods (i.e. all fields are private). 3) Making the capsule impenetrable means that you avoid returning references to mutable internal data structures. Either you make them immutable or you create copies in getter/setter methods.
## PSU - Principle of Separate Understandability

> Concrete
> https://design-types.net/c/PSU

Short Description:  
You shouldn’t need to know other parts for understanding this one.  
Long Description:  
Each module (method/class/artifact/service/...) should be understandable on its own. Understanding becomes a lot more difficult if you cannot apply divide and conquer. Furthermore, if something is not separately understandable, this typically means either that a part of the functionality does not belong here or the module has the wrong abstraction.

## TdA/IE - Tell don’t Ask/Information Expert

> Concrete
> https://design-types.net/c/TdA_IE

Short Description:  
Functionality should be where the data is.  
Long Description:  
Instead of asking a module for data, processing it, and putting it back afterwards, better just delegate. This reduces complexity in those modules which are already large (and may even become god classes). So avoid getters and setters in favor of methods containing domain logic. In other words: Logic should be implemented in that module that already has the necessary data, that is the information expert.

## CF - Customer Focus

> Pragmatic
> https://design-types.net/c/CF

Short Description:  
This is not what the customer pays us for!  
Long Description:  
If something is not requested, there has to be a very good reason to do it. Anything in addition costs additional time (also for removing or maintaining it). It creates the additional risk of more bugs and makes you responsible for it. Continuously remember what was requested e.g. by looking into the requirements or asking the customer. 
## ICC - In the Concrete Case

> Pragmatic
> https://design-types.net/c/ICC

Short Description:  
Your arguments are valid but in the concrete case the advantages won’t be important.  
Long Description:  
Many arguments hold true in general but when we look at the decision to be made, the effects they describe are sometimes negligible. Yes, low coupling is important, uniformity is helpful, and flexibility is desirable. But these aspects are sometimes crucial and sometimes irrelevant. So better focus on arguments that are relevant in the concrete case instead of insisting on aspects just to satisfy idealistic pettiness.

## EaO - Early and Often

> Pragmatic
> https://design-types.net/c/EaO

Short Description:  
Going online soon means to get value and feedback soon.  
Long Description:  
Business success is often built on being faster than competitors. Building minimum viable products and 80%-solutions facilitate a faster time to market. Moreover the best feedback for improvement comes after a release and is rarely designed up front. So avoid perfectionism, release early and often, and accept a certain amount of technical debt.
> 
## UFT - Use Familiar Technology

> Pragmatic
> https://design-types.net/c/UFT

Short Description:  
Using well-known technology results in faster outcome and fewer time-consuming bugs.  
Long Description:  
Well known technologies are easier to handle because you can focus on the job and you know all the pitfalls. If you use unfamiliar technology, you most likely won’t do that well at first. This results in even more bugs and worse design. So better use those technologies that all (current and future) developers are most familiar with.

## PoQ - Principle of Quality

> Idealistic
> https://design-types.net/c/PoQ

Short Description:  
Bad quality kills us in the long run!  
Long Description:  
It may be faster now, but we need to be fast tomorrow, too. Bad quality frustrates maintainers, makes fixing bugs harder and leads to huge efforts for changes. This often starts by being careless once. Don’t let a vicious circle begin. Use metrics, adhere to the architecture, have a high test coverage, apply code reviews and refactor continuously. Don’t be lazy.

## UP - Uniformity Principle

> Idealistic
> https://design-types.net/c/UP

Short Description:  
Solve similar problems in the same way.  
Long Description:  
Following UP reduces the number of different solutions. There are fewer concepts to learn, fewer problems to solve and fewer kinds of defects that can occur. So have a consistent structure, a consistent naming scheme and use the same mechanisms and libraries everywhere. Prefer using the same approaches and not just similar ones as subtle differences lead to bugs.

## MP - Model Principle

> Idealistic
> https://design-types.net/c/MP

Short Description:  
Program close to the problem domain.  
Long Description:  
Software should model and mirror the concepts and actions of the real world. So avoid everything that works “accidentally”. If it works accidentally, it breaks accidentally. So be precise with semantics. If you need to delete an order in a data migration routine, call deleteOrder and not cancelOrder—even if that currently does the same. cancelOrder might get enhanced such that it creates a reverse order which wouldn’t be correct for data migration anymore.
## PSPG - A Penny Saved Is a Penny Got

> Idealistic
> https://design-types.net/c/PSPG

Short Description:  
It might not be a big advantage, but it’s not a big cost either.  
Long Description:  
Making little improvements a habit sums up to a big advantage. This is the reason behind the boy scout rule (“Leave the campground cleaner than you’ve found it”). You don’t have to clean the whole forest but if everyone leaves the campground just a little cleaner, we will have a clean forest in the end. So if it’s not a big deal, update libraries, improve documentation, and refactor th

## ML - Murphy’s Law

> Robust
> https://design-types.net/c/ML

Short Description:  
Avoid possibilities for something to go wrong or to get misused.  
Long Description:  
If there is a possibility for something to be used in the wrong way (like supplying parameters in the wrong order), it will eventually happen. So better avoid possible future bugs by using defensive programming, immutability, a common naming scheme, avoiding duplication and complexity.


## IR - Instability Risk

> Robust
> https://design-types.net/c/IR

Short Description:  
Bleeding edge often leads to blood and pain.  
Long Description:  
New technology often comes with teething problems. Using too unstable software, beta versions of libraries, or anything that hasn’t stood the test of time is risky. There may be unknown bugs, nasty little quirks and compatibility issues no one has heard of, yet. This also means that if you encounter these problems, you will be one of the first to face them.


## FF - Fail fast

> Robust
> https://design-types.net/c/FF

Short Description:  
Program defensively or you’ll have a hard time debugging.  
Long Description:  
If you don’t check your inputs, cascading failures can occur. This results in security problems and error messages which are hard to decipher because they are not thrown at the position of the actual fault. This may even lead to situations where teams have to investigate failures which are not theirs. So log and throw an error as soon as you realize a problem. The earlier the better, so throwing a compile-time error is preferable to runtime checks.


## RoS - Rule of Standardization

> Robust
> https://design-types.net/c/RoS

Short Description:  
Adhering to standards makes systems easier to understand and reduces bugs.  
Long Description:  
Sticking to standards reduces complexity. If you are familiar with the standard, understanding systems that adhere to it will be much easier. Also, standards ensure a certain degree of interoperability and maturity. So use standard technologies, standard architectures, standard coding styles, standard formatting, standardized checklists, etc. If there are no formal standards, create your own in-house standard.

## TP # Technological Progress

> 	Technologic
> https://design-types.net/c/TP

Short Description:  
Progress must not be ignored in a competitive environment.  
Long Description:  
New technology is not only motivating but also comes with benefits like more features, more performance, better maintainability, and fixed bugs. Furthermore, old technology won’t be supported for much longer and new people don’t know the old stuff anymore. Continuously challenge existing solutions by evaluating alternatives.

## FRD - Frequency Reduces Difficulty

> Technologic
> https://design-types.net/c/FRD

Short Description:  
If it hurts, do it more often!  
Long Description:  
Typically, it’s easier and less effort to go small steps continuously than to wait until there is a huge gap to bridge. The pain will be bigger the more you postpone it—break the cycle and update to new versions, refactor regularly, merge and release early and often. Doing something more often, leads to more practice and fewer mistakes.

## DRW - Don’t Reinvent the Wheel

> Technologic
> https://design-types.net/c/DRW

Short Description:  
Focus on real challenges instead of old ones.  
Long Description:  
If something has already been solved, it’s probably solved in a better way than we will manage to do in the time we have. No one would ever reimplement a cache or a search algorithm except it is one’s core competency. So focus on the challenges of your core business and use standards, libraries, and frameworks. They are the core business of those people who create and maintain them. They’ve solved many problems that we haven’t even thought of, yet.
## EbE - Experience by Experiments

> Technologic
> https://design-types.net/c/EbE

Short Description:  
We’ll never know if we don’t try!  
Long Description:  
Discussing advantages and disadvantages theoretically can be helpful but at a certain point you will never know which variant is better if you don’t try. So if you have a standard solution to a problem, try the other one. Carefully but regularly try out new frameworks and libraries, new coding guidelines, architectural/design patterns etc. in real-world projects. Failed experiments will be refactored and successful experiments will stay and become the new standard.

## qfoc - Focus

> Question
> https://design-types.net/c/qFoc

Short Description:  
Are we still on the right track or have we lost focus?  
Long Description:  
Discussions are weird sometimes. You start with the clear aim to decide whether solution A or B is better and end up with a discussion on something completely different. You easily get lost in side issues or you heavily argue on something unimportant (“bike-shedding”). So clarify the main topic of your discussion and keep the focus on it.

## qTS - Third Solution

> Question
> https://design-types.net/c/qTS

Short Description:  
Are we discussing all relevant possibilities?  
Long Description:  
Sometimes we argue heavily if solution A or B is better when in fact there is a third solution C that may be preferable. So regularly ask yourself (and your colleagues) whether there is a solution that needs to be discussed, too.

## qTRT - The Right Time

> Question
> https://design-types.net/c/qTRT

Short Description:  
What will happen if we don’t decide right now?  
Long Description:  
A design decision should be taken as late in the project as possible. But it’s likewise harmful to take it too late. In order to find out if a decision really needs to be made now, think about what will happen, if the decision is deferred.
## qSta - Stakeholders

> Question
> https://design-types.net/c/qSta

Short Description:  
Do we have the needs of all stakeholders in mind?  
Long Description:  
Some decisions have influence on many stakeholders—some of which are often forgotten. Also, think about QA, Ops, etc.
## qCon - Consequences

> Question
> https://design-types.net/c/qCon

Short Description:  
What will happen if we make the wrong decision?  
Long Description:  
Think about possible impacts, chances of occurrence, and possibilities to revert. If the consequences are not bad at all, then it might be better to shorten the discussion. If the consequences are severe, there should be some means of mitigation in place. In any case think about the consequences of a decision.
## qMU - Mutual Understanding

> Question
> https://design-types.net/c/qMU

Short Description:  
Do we really understand each other’s points of view?  
Long Description:  
Sometimes a discussion gets stuck because of misunderstandings or misinterpretations. Commonly that’s because everyone is busy explaining their own point of view without trying to understand the other. If that’s the case, it is necessary to realize that. Otherwise, there will be no progress in the discussion.
## qFS - From Scratch

> Question
> https://design-types.net/c/qFS

Short Description:  
"What would be the “real solution” if we’d start from scratch?  
Long Description:  
Often the solutions we come up with are tied to the current state of the software. Our thinking is restricted such that we do not consider certain possibilities. In such cases it is helpful to neglect the circumstances of the current system for a moment—think outside the box. Even if the greenfield solution you then come up with is not directly applicable, it’s often a starting point for an alternative.
## qBSU - Best Solution for the User

> Question
> https://design-types.net/c/qBSU

Short Description:  
Do we really address the real user’s needs?  
Long Description:  
Not in every case the person who specifies what to do is identical to the user of the system. Wrong interpretations or misunderstandings may lead to unsuitable solutions that do not satisfy the real user’s needs. Every now and then, you should ask yourself if you are still designing a system that really helps those who will eventually use it.
## aMed - Mediator

> Action
> https://design-types.net/c/aMed

Short Description:  
We cannot agree. Let’s get some help!  
Long Description:  
Sometimes a discussion gets stuck. In these cases it is often advisable to ask another colleague for an opinion or mediation. Usually a colleague who hasn’t already participated in the discussion, adds a new, unbiased perspective.
## aTD - Team Decision

> Action
> https://design-types.net/c/aTD

Short Description:  
The decision is too important to take alone. Let’s have the whole team decide!  
Long Description:  
Important decisions which affect many people like architectural decisions, big refactorings, and external APIs should be taken by the whole team. First, this typically results in better decisions. Second, the team will be much more committed to the decision. And third this fosters knowledge transfer.
## aDaC - Divide and Conquer

> Action
> https://design-types.net/c/aDaC

Short Description:  
Actually we are mixing up two aspects or two decisions. Let’s discuss them separately.  
Long Description:  
Design decisions get complicated or stuck if there is actually more than one decision to make. The discussion shifts from one topic to the other and back again. This gets even worse if nobody realizes that there is actually more than one problem. Step back, find out which decisions or problems there are and discuss them separately.
## aRes - Research

> Action
> https://design-types.net/c/aRes

Short Description:  
Let’s have a look if there is already a suitable solution.  
Long Description:  
When making a decision, make sure that you know all relevant solutions. Many problems have already been solved. So before inventing an own algorithm, have a look at libraries and scientific papers. For certain design decisions have a look at standards and patterns. Also, consider researching code snippets for common programming issues. Maybe there is even commercial-off-the-shelf (COTS) or open-source software you can leverage.
## aFC - Flip a Coin

> Action
> https://design-types.net/c/aFC

Short Description:  
That’s not worth the discussion!  
Long Description:  
In some cases the difference between several solutions is negligible. Or both the solutions have their pros and cons without one being superior to the other. It is then better to just take the decision by flipping a coin than to waste time in a lengthy and pointless discussion.
## aDA - Devil’s Advocate

> Action
> https://design-types.net/c/aDA

Short Description:  
There is no real discussion, and we risk missing a point. Let’s appoint a devil’s advocate.  
Long Description:  
Sometimes you agree too fast on a solution—probably because you all have a similar way of thinking. In such a case you can appoint someone who has to argue against that solution. A similar problem occurs when none of you has a strong tendency towards any of the solutions. In such a case, for each solution appoint a representative who tries to argument for this and against the other solutions.
## aPO - Product Owner Decides

> Action
> https://design-types.net/c/aPO

Short Description:  
This has a significant impact on the business, so we have to talk with the product owner.  
Long Description:  
Some technical decisions influence the product itself. Often there is an impact on cost and time and sometimes there are even legal issues. Trade-offs include hosting an application in the cloud (flexibility and time vs. privacy and cost), adding a caching layer (performance vs. complexity and cost), make-or-buy (time vs. flexibility and cost), etc. In those cases the decision is not merely a technical one. Involve the PO.
## aCD - Client Decides

> Action
> https://design-types.net/c/aCD

Short Description:  
The client who calls the API knows best how the ideal API should look like.  
Long Description:  
APIs need to be intuitive to those who use it and sometimes it’s hard to predict if that’s the case. Some decisions have an impact on how a module can be used. Some use cases may get simpler and others may get harder and less intuitive. Better stop assuming you know what’s best for the clients. Just ask and involve them in your decision.
## 🔗 Ressources
- https://www.printerstudio.com/sell/designs/software-design-cards.html
- https://design-types.net/downloads/DesignCards_v1.0_a4.pdf