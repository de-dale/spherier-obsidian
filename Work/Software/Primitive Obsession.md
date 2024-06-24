---
ressource:
  - 🧠 Concept
relates:
  - "[[Anti-Pattern]]"
tags:
  - CodeSmell
---
[[Primitive Obsession]] est un [[Code Smell]] qui consiste à utiliser des types primitifs (nombre entiers, nombres décimaux, tableaux, chaines de caractère, etc.) pour représenter les idées du [[Domaine]].
Par exemple, on utilisera une String pour représenter un message, ou un Integer pour représenter un montant monétaire.

Pour répondre à ce Smell, utiliser des [[Value Object]] à la place des données primitives. Ensuite, regardez où votre code montre des [[Feature Envy]] qui pourraient être déplacée dans ce nouveau [[Value Object]]

Avec #IntelliJ on peut introduire un Value Object avec les outils de refactor :
- Wrapper un paramètre
- Wrapper le retour d'une méthode
- Introduire un objet delegate sur un champ

## Ressources
- https://refactoring.guru/fr/smells/primitive-obsession