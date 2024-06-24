---
tags:
  - mdm
  - mdm/project
  - ⏸️pause
---

# Contexte

Dans le cadre de la mise ne place du MET, on a "sécurisé" le composant logiciel + les données de paramétrage, avec des "Tests auto".

Ces tests ont pour vocation de remplacer une batterie de tests maunels à faire sur chaque évolution du paramétrage. ET de tester le comportement du logiciel du MET, car on n'a pas de tests de plus bas niveau dessus.

> [!tip]+ Page Confluence : "Automatisation des tests"
> https://maisonsdumonde.atlassian.net/wiki/spaces/CORE/pages/2380398614/Automatisation+des+tests

# Suivi 

- [ ] Avoir les outils permettant de créer et maintenir des tests auto
	- [ ] Finir le projet d'exemple 
	- [ ] Revoir ce qu'on met dans le projet exemple : 
		- est-ce que je vais jusqu'à déployer un Pod pour bénéficier des secrets dans Kube ?
		- est-ce qu'on s'arrête à runner les tests dans les runners Gitlab ? (et on s'expose à des problèmes de credentials)
	- [ ] Finir la documentation
		-  [🧪Automatisation des tests](https://maisonsdumonde.atlassian.net/wiki/spaces/CORE/pages/2380398614/Automatisation+des+tests)
		- [ ] Définir le reste à faire 
- [x] Corriger le problème de lancement des tests ✅ 2023-09-25
	- Impossible de récupérer les scénario XRay depuis le curl "classique" des api v2
	- Impossible de créer une issue JIRA avec le rapport Cucumber
	- ✅ Vu avec Patrice : nouveaux credentials générés
