---
ressource:
  - 🧠 Concept
relates:
  - "[[Couplage]]"
  - "[[Cohésion vs. Couplage]]"
---

La **[[Cohésion]]** est le degré auquel les éléments d'un tout vont ensemble.

Deux éléments sont **cohérents**, quand ils sont utilisés ensemble, par un composant destiné à effectuer une seule tâche.
Un composant possède une faible cohésion lorsqu'il contient des éléments sans rapport les uns avec les autres.

Les méthodes et les champs d'une classe ou les classes d'un composant, devraient avoir une forte cohésion.

Une **forte cohésion** dans les classes et les composants permet d'obtenir du **code facile à comprendre et bien plus lisible**.


- **Cohésion élevée** : La cohésion élevée existe lorsque les fonctionnalités d'un module sont étroitement liées entre elles. Cela signifie que les fonctionnalités d'un module partagent une finalité commune.
- **Cohésion faible** : La cohésion faible existe lorsque les fonctionnalités d'un module sont peu liées entre elles. Cela signifie que les fonctionnalités d'un module n'ont pas de finalité commune.

[[Cohésion vs. Couplage]]
[[Couplage]]

### Quelques principes derrières la Cohésion

- Release Reuse Equivalency Principle (REP): _The granular of reuse is the granular of release._
 > REP states that the granule of reuse, a component, can be no smaller than the granule of release. Anything that we reuse must also be released and tracked. It is not realistic for a developer to simply write a class and then claim that it is reusable.
- Common Closure Principle : Les classes qui changent ensemble sont packagés ensemble
- Common Reuse Principle : Les classes qui sont utilisées ensemble sont packagés ensemble

#### Mesure de la cohésion 
> A class is the most cohesive when the members of a class have the maximum connectivity among them; that is, every normal method in a class interacts with all of the instance variables in the clas
http://www.sdml.cs.kent.edu/library/Chae98.pdf