Le **[[Couplage]]** est le degré d'interdépendance entre les composants d'un logiciel.

Deux éléments de code, classes, composants ou modules sont **couplés** lorsque **au moins l'un de deux utilise l'autre**.
Moins ces éléments connaissent de choses de l'autre, moins ils sont couplés.

Un composant faiblement couplé avec son environnement peut être facilement modifié ou remplacé.
Un composant fortement couplé avec son environnement est plus difficilement modifiable ou remplaçable.

- **Couplage fort** : Le couplage fort existe lorsque deux modules sont fortement liés l'un à l'autre. Cela signifie que le changement d'un module peut avoir un impact important sur l'autre module.
- **Couplage faible** : Le couplage faible existe lorsque deux modules sont faiblement liés l'un à l'autre. Cela signifie que le changement d'un module a peu ou pas d'impact sur l'autre module.

[[Couplage indirect]]

[[Cohésion]]
[[Cohésion vs. Couplage]]
[[Équation du couplage]]

### Quelques principes derrières le Couplage
- Acyclic Dependencies Principle (ADP) : The dependency graph of packages must have no cycles.
  Allow no cycles in the component dependency graph._
- Stable-Dependency Principle (SDP) : Depend in the direction of stability.
- Stable-Abstractions Principle (SAP) : Abstractness increases with stability.
  A component should be as abstract as it is stable.