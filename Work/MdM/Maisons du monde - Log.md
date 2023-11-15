## Tasks

```dataview
task 
FROM "Work/MdM/Logs" OR "Work/MdM" OR #Project
WHERE !completed
SORT file.name
GROUP BY file.link
```
# Logs

## [[2023-11-09]]

**Validation post-MEP TRP**
- Validation recette/métier
- Validation MEP / PROD
- Idées 
	- Réduire le temps entre la validation de l'US et la validation de la DMEP
	- Définir une personne suit suit les MEP
	- Checklist d'action
	- Diminuer le temps d'attente
	- Comment on valide la MEP ?
		- Hypercare + durée ?
			- New Relic : regarder nos dépendances
		- VSR (Vérification Service Régulier)
	- Qui valide la MEP ?

**Départ de Franck**
- Tour de table
	- FL s'engage à soutenir le véto proposé par les PO Supply en cas d'implication dans les gates.
	- Demande PO : être averti en amont des projets pour avoir les infos et estimer la capacité de réalisation de l'équipe. Compenser l'absence d'un RD par de la communication.
	- Valoriser ce que fait/réalise la Supply auprès des métiers
	  => Aujourd'hui, on constate un GAP de communication. "Ils n'ont pas accès à vous"
- "S'organiser sans RD dans la SUPPLY"

## [[2023-11-08]]

CODEV
- Présentation des interactions infra
	- Demande de changement dans SH au lieu de Demande de changement 🎉
- Présentation FDI
	- Les FDI sont à revoir "régulièrement" pour s'assurer qu'elles sont à jour
	  => FDI à linker dans la revue de Prod + état des lieux 
  - Revue de prod
	  - Question Post-Mortem : aujourd'hui, on a un dossier dans SCM et il existe un dossier partagé
	    => Supprimer le dossier SCM ?

NewRelic
- Comment afficher les deployments dans NR ?
  => David Creuse le sujet pour nous donner une réponse

## [[2023-11-07]]
- Discussion avec Mehdi
- Seconde Chance : focus sur
	- le calcul de délais dans Seconde Chance
	- l'éligibilité des services dans le cadre de seconde chance
- Discussion 5mins avec [[Florian LEFEUVRE]] :
	- [ ] atelier à préparer en urgence pour jeudi matin
	- [ ] Délégation Poker vs RACI
## [[2023-11-06]]

- Présentation Observabilité à l'équipe TRP
- Revue des incidents
	- On a convenu de mettre un espace pour que les équipes renseignent les incidents hors SH, pour en discuter ensemble
- Seconde Chance avec TRP
	- On a passé en revue les points sur le contrat
	- On a convenus que les assets "api-service-catalog" et "api-xxx-delays" devaient gérer leurs propres règles autour de Seconde Chance, et que 
## ![[2023-10-30]]
## ![[2023-10-26]]

## ![[2023-10-25]]
## ![[2023-10-23]]
## ![[2023-10-20 Devfest]]
## ![[2023-10-19]]

### [[2023-10-18]] 

- [ ] STK : Post Mortem sur la "MEP avortée"  (7236)
- [ ] STK : Post Mortem sur la "MEP ratée" 

Moi pas content après archi qui se défausse de l'accompagnement de l'équipe sur ce sujet
### [[2023-10-13]]

Groupe Qualité de code
- Remaniement de la façon de faire
- [x] TDD à présenter ✅ 2023-11-08
### [[2023-10-11]]

Revue de production 
- [ ] Rédiger le Post mortem pour stock
### [[2023-10-09]]

- Lenteurs du MET
	- MEP de la 1ière correction
	- Problème persiste
		-   [x] Etablir une [[Matrice Hikari]] des applications

### [[2023-10-05]]

- TRP : Refinement
- [[2023-10-05 Point équipe IT CORE]]

### [[2023-10-04]]

Partage transverse 
- [[2023-10-04 CODEV MDM]]
- [[Point de partage Dev Supply]]

[[Gestion des incidents]]
- Revue des incidents SUPPLY
- Travail sur l'Observabilité
- [x] Planifier un point avec [[Pierre GUIKOVATY]] sur les SLI/SLO et les sondes Zabbix ✅ 2023-11-08
- [ ] Planifier un point avec  [[Stéphane DRUGEAULT]]  sur les SLI/SLO et les sondes Zabbix
### [[2023-09-27]]

[[Gestion des incidents]]
- Point avec David MAUMENE **planifié** au [[2023-10-03]]

[[Animation Supply]]
- Planification du [[Point de partage Dev Supply]]
- Planification des conversation individuelles
	- Benoit
	- Maxime
	- Michael
- [[Animation Supply#Clarification du rôle de Lead Dev]]
	- Clarification demandée à l'ensemble des RDD pour partager sur ce qu'est un Lead Dev dans leurs domaines
### [[2023-09-25]]

- Organisation Dev Supply A23
	- TRP avec Maxime
		- [[BG - 2023-09-25 - Organisation SUPPLY-STK-A23]]
	- STK avec Benoit
		- [[MxC - 2023-09-25 - Organisation SUPPLY-TRP-A23]]
	- [x] Demander les droits de PROD pour Maxime ✅ 2023-09-26
	- [x] Demander les droits de PROD pour Benoit ✅ 2023-09-26
- [x] STK : Contrat d'interface pour Rhinov ✅ 2023-09-25
- [x] Lister les bases de données Legacy DIGIT
### [[2023-09-21]]

[[Gestion des incidents#Réunion support dans le domaine Supply]]
### [[2023-09-19]]

[[Projet Tracking]]
Florian LEVEVRE a rapidement parlé d'un projet Tracking, central pour la Supply sur la période Automne 2023.
Pilote du Projet : Jean-Marc DUPONT.
Kickoff : à venir.

[[Gestion des incidents]]
![[Gestion des incidents#2023-09-19]]

Composants en lien avec le Legacy DIGIT
- Relance LT et Archi Supply

[[Work/MdM/Projects/Test Automatisés|Test Automatisés]]
 - Vu avec Patrice pour faire avancer les choses
- Support XRay contacté