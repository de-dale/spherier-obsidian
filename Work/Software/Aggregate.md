---
ressource:
  - 🧠 Concept
relates:
  - "[[Domain-Driven Design Tactique]]"
---
> An AGGREGATE is a cluster of associated objects that we treat as a unit for the purpose of data changes.
>
> — Eric Evans, Domain-Driven Design blue book

L'[[Work/Software/Aggregate|Aggregate]] est un concept du [[Domain-Driven Design]] permettant de matérialiser un concept métier / rassembler des règles.

> Un Agrégat est un groupe d’objets associés qui sont considérés comme un tout unique vis-à-vis des modifications de données.
> L’Agrégat est démarqué par une frontière qui sépare les objets situés à l’intérieur de ceux situés à l’extérieur. Chaque Agrégat a une racine. La racine est une Entité, et c’est le seul objet accessible de l’extérieur.
> -- DDDViteFait

Il s'agit de quelque chose que l'on peut faire émergent en [[EventStorming]]
![[Work/ateliers/Event Storming/Aggregate]]