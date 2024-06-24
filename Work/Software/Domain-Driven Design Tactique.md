---
ressource:
  - 🧠 Concept
---
Le DDD tactique est l'espace des solutions

Conception dirigée par le Modèle

# DDDViteFait

Une meilleure approche est de lier étroitement modélisation du domaine et conception.
Le modèle devrait être construit en gardant un oeil sur les considérations logicielles et conceptuelles. On devrait intégrer les développeurs dans le processus de modélisation.

![[ddd-architecture-en-couches.excalidraw]]

**Interface utilisateur (couche de présentation)**
Responsable de la présentation de l’information à l’utilisateur et de l’interprétation des commandes de l’utilisateur.

**Couche application**
C’est une couche fine qui coordonne l’activité de l’application.
Elle ne contient pas de logique métier. Elle ne recèle pas l’état des objets métier, mais elle peut détenir l’état de la progression d’une tâche applicative.

**Couche domaine**
Cette couche contient les informations sur le domaine. C’est le coeur du logiciel métier. L’état des objets métier est renfermé ici. La persistance des objets métier et peut-être aussi leur état est délégué à la couche infrastructure.

**Couche infrastructure**
Cette couche agit comme une bibliothèque de soutien pour toutes les autres couches. Elle fournit la communication entre les couches, implémente la persistance des objets métier, contient les bibliothèques auxiliaires de la couche d’interface utilisateur, etc.

Les invariants sont ces règles qui doivent être maintenues à chaque fois que les données changent. C’est dur à accomplir quand beaucoup d’objets ont des références vers les objets dont les données
changent.