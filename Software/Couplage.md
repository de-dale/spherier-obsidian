# Couplage
Le **[[Couplage]]** est le degré d'interdépendance entre les composants d'un logiciel.

Deux éléments de code, classes, composants ou modules sont **couplés** lorsque **au moins l'un de deux utilise l'autre**.
Moins ces éléments connaissent de choses de l'autre, moins ils sont couplés.

Un composant faiblement couplé avec son environnement peut être facilement modifié ou remplacé.
Un composant fortement couplé avec son environnement est plus difficilement modifiable ou remplaçable.

[[Cohésion]]
[[Cohésion vs. Couplage]]
[[Équation du couplage]]

### Quelques principes derrières la Cohésion
- Acyclic Dependencies Principle (ADP) : The dependency graph of packages must have no cycles.
  Allow no cycles in the component dependency graph._
- Stable-Dependency Principle (SDP) : Depend in the direction of stability.
- Stable-Abstractions Principle (SAP) : Abstractness increases with stability.
  A component should be as abstract as it is stable.