# Tasks

```dataview
TASK 
FROM "Work/Missions/Decathlon" AND -#⏸️pause
WHERE !completed
SORT tags DESC
```
# Logs

- 🎯 Objectifs
	- 
- 👥 Mob-Programming
	- 
- 🎓 Learning-Hour
	- 
- ♻️ Rétro

Questions en suspens

- [x] 🎓 Learning-Hour : Primitive Obsession ✅ 2024-05-28
- [x] 🎓 Learning-Hour : Open Api & Quarkus ✅ 2024-05-28
- [ ] 🎓 Learning-Hour : Contextive ?
- [ ] Aborder la question des tests et de la stratégie de tests

## [[2024-05-28]]

- 🎯 Objectifs
	- Avancer sur le Back-end pour converger vers du code satisfaisant qui ressemble à un truc fini
	- Discuter du frontend pour voir si les concepts ont été correctement transposés
- 👥 Mob-Programming
	- Modéliser le demande de la Transaction (au moins : ajouter un Item à la transaction)
- 🎓 Learning-Hour
	- Open Api & Quarkus & Contract First
	- Primitive Obsession & les moyens de lutter
- ♻️ Rétro
	- L'équipe est globalement satisfaite des 5 jours passés ensemble
		- C'était idéal pour démarrer quelque chose en équipe
		- L'équipe a le sentiment d'avoir beaucoup appris 
	- Nous aurions été plus efficace avec une préparation en amont
		- Préparer une UserStory sur laquelle l'équipe aurait pu converger plus rapidement que ce que l'on a fait
		- Avoir des ressources à disposition en amont (par exemple: le replay de la présentation DDD du 14 février, des articles, vidéos ou d'autres ressources similaires)
## [[2024-05-24]]

- 🎯 Objectifs
	- continuité sur les domaines
		- Catalog
		- Transaction
		- Acquisition
	- Mapping
- 👥 Mob-Programming
	- Fini le Catalog
	- Avancé sur l'Acquisition
- 🎓 Learning-Hour
	- Maven enforcer plugin
	- ArchUnit
- ♻️ Rétro
	- Impression qu'on a mois passé de temps à discuter des hypothèses fonctionelles
	- Fatigue
		- Peur qu'on n'arrive pas au bout du useCase d'ici mardi
		- Micro service vs. monolithe
	- Focus technique : c'était cool
		- Voir davantage de sujets comme ArchUnit, ça serait chouette
	- Voir maven et ArchUnit, c'était très cool
	- Q : Comment mettre en palce l'archi hexa sur el Front ?

Remarques à moi-même
- mieux adresser la question des Exceptions
- ArchUnit
- Shared Kernel
## [[2024-05-23]]

- 🎯 Objectifs
	- Aller au bout sur l'Acquisition pour en faire un exemple
	- Se poser sur le Nommage
	- Expliquer la "bonne pratique" AcquisitionService vs. GetItemByEan
- 👥 Mob-Programming
	- Avancer sur l'Acquisistion
	- Sortir la notion de "transaction" du Domaine Acquisition : AcquisitionRepository
- 🎓 Learning-Hour
	- Patterns du DDD :
		- Value Object
		- Entity
		- Aggregate
		- Factory
		- Repository
		- Service
- ♻️ Rétro
	- On s'est posé la question du nommage, et il n'y a pas nécessairement les concepts dans le nom
	- On discuter trop sur des hypothèses fonctionnel, et on perd le focus de pourquoi on est ensemble (apprender le DDD sur un exemple)
		- Résultat pas forcément pertienent vs. tracer qu'on est sur uen hypothèse et avancer sur les concepts de DDD
	- Q: Lib pas dans le domaine + maven-enforcer
	- Q: Domaine Catalogue
	- Q: est ce qu'on peut voir un projet plus abouti ?
		- https://github.com/nlarche/battleship
		- https://github.com/nlarche/permaproject
		- https://gitlab.com/beyondxscratch/hexagonal-architecture-java-springboot

Auto rétro :
- j'ai trop le clavier
- coup de mou en début d'aprem

## [[2024-05-22]]

- 🎯 Objectifs
- 👥 Mob-Programming
	- Avancer sur l'Acquisistion
- 🎓 Learning-Hour
	- Anti Corruption Layers
- 👥 Mob-Programming
	- Avancer rapidement sur la mise en place d'un second domaine : Catalog
- Atelier Naming sans Fabien
- ♻️ Rétro
	- pas de rétro car Fabien a du parti tôt

Auto rétro :
- j'ai trop le clavier
- coup de mou en début d'aprem
- Trop tracé sur le Catalog : j'ai du en larguer quelques uns
- Pas parlé de l'intérêt du DSL sur le repository

## [[2024-05-21]] - Kick off Accompagnement tactique

- 🛠️ Matrice des connaissances
	- Objectif : expliciter les connaissances de l'équipe sur tout ce qui est nécessaire au fonctionnement de l'équipe
- 📺 Re-présentation du contexte
	- Présentation de ce qui a été fais en Eventstorming
	- Présentation de l'Ubiquitous Language
	- Présentation du code commencé par l'équipe en place
- 👥 Mob-Programming
	- Choix de l'User-Story : "Ajouter un Item bloqué à la transaction"
	- Development + Conception en Mob-Programming sur le domaine de l'Acquisition
- 🎓 Learning-Hour
	- Architecture Hexagonale
- ♻️ Rétro
	- Globalement contents
	- On a passé trop de temps sur la Matrice des connaissances
	- Pressés d'avancer

Auto rétro
- Archi Hexagonale : ma présentation est vraiment pas folle

https://excalidraw.com/#room=56555d429096c478a063,R5Jsph3EhpY0Rf5dYUatxA

Tout de table
- **Anwar** : Dev plutôt Back ~3semaines
	- DDD ce que c'est
	- Aligner l'équipe sur les pratiques techniques
- **Guillaume** : Dev plutôt front rejoins l'équipe il y a 1 mois
	- Attente : Ce qu'est le DDD et voir comment l'appliquer, cuirieux
- **Corentin** : Absent et jeune papa
- **Florian** : Dev plutôt Java, EM
	- Implémentation dans le code de ce qu'on a vu ensemble
	- Schéma à revoir ensemble
- **Robin** : Dev plutôt Java
	- Aller plus loin dans les concepts
	- Curieux pour arranger le projet
- **Emmanuel** : Développeur Back sur Nantes dans l'équipe depuis 2 semaines
	- Alignés sur le DD et ce que ça nous apporte
	- Faciliter le Dev + Code review

> Pour faire suite aux différents ateliers de [Domain Driven Design](https://www.google.com/url?q=https://decathlon.atlassian.net/wiki/spaces/COMMERCE/pages/434209143/Domain%2BDriven%2BDesign&sa=D&source=calendar&ust=1716706679797270&usg=AOvVaw2uPh7qe7VuGiErFWcbVMkO), Fabien va nous accompagner sur la mise en place tactique (application au niveau de l'architecture).  
> Plus d'informations à venir (participants des sessions, agenda détaillé, ...)  
> ℹ️ Ce sera à distance

## [[2024-05-15]]

- [x] Préparation du déroulé
- [x] Excalidraw de support ✅ 2024-05-21
      https://excalidraw.com/#room=56555d429096c478a063,R5Jsph3EhpY0Rf5dYUatxA
	- [x] Matrice de compétences ✅ 2024-05-21
	- [x] des post-its : L'image qui explique tout ✅ 2024-05-21
- [x] #decathlon  Rassembler les présentations ✅ 2024-05-21
	- [x] DDD Tactique ✅ 2024-05-21
	- [x] Mob-Programming ✅ 2024-05-21
	- [x] Archi hexa ✅ 2024-05-21
	- [x] TDD ✅ 2024-05-21

## [[2024-05-11]]

EventStorming sur Lille 
