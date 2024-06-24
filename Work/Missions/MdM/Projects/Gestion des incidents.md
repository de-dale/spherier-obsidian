---
tags:
  - mdm
  - mdm/project
---
# TODO

```tasks
not done
path includes {{query.file.path}}
hide backlink
```
# Contexte

Banettes dans SupportHero qui s'accumulent.

On dispose d'un compte générique SupportHero pour qu'on soit autonome 
- Objectif : gagner en vélocité sur la résolution des incidents
- Sondage Supply : Qui utilise le compte générique ?

Tickets qui sont escaladés côté JIRA sont traités
Tickets qui vont dans Zabbix ne sont pas traités
=> Qui les consulte ?
=> Qui ferme les tickets SH ?
=> Capitaliser les incidents dans SH pour résoudre plus rapidement les incidents.

**Plan d'action**
- Revue des incidents
- Améliorer le process => se faire aider par Nicolas DELPORTE ?
- Chez nous : Tiphaine BOU

Difficulté (yohann) : savoir si un humain va traiter les tickets N2/N3
- N1 : Tiphaine et Amélie
- Rôle tournant

**Objectif :**
- S'organiser pour traiter les incidents en N2/N3
- Résoudre les tickets dans SH 
	=> Valeur ajoutée de SH ?
- Documenter le process
	- Comprendre les process des différentes squad

# Suivi

## [[2023-09-25]]

Réunion avec Bertrand sur le sujet "Monitorer les DLQ"

- [x] Provoquer une réunion avec David MAUMENE ⏫ ✅ 2023-09-27
	- Sujet du monitoring / observabilité / supervision des DLQ & topic Supply
	- Comprendre la cible et expliciter les étapes
## [[2023-09-21]]

###  Réunion support dans le domaine Supply
"[[2023-09-21 - Le support dans le domaine Supply]]"

## [[2023-09-19]]

Début de "projet" dans Obsidian
## [[2023-09-14]]

Grande discussion avec Tiphaine sur le contexte de la gestion des incidents.
Revue de SupportHero, des dashboards et des vues dont on dispose.

- [x] Exploration de SupportHero ✅ 2023-09-19
	- [x] Accéder à Zabbix
	- [x] Accéder à Grafana
		- Par LDAP

- [x] Faire l'état des lieux des notifications STK
	- Il y a des notifications qui tombent directement dans Teams
	  => On ne peut pas les comptabiliser
	- Quelle est la plusvalue de contourner SupportHero ?
- [x] Faire l'état des lieux des notifications TRP
	- Il y a beaucoup de notification par mail
	  => Quelle est la plusvalue de contourner SupportHero ?
	- Il y a une sorte d'alerting pour
		- Les camions bloqués en douane
		- Edi agena
		- Mail de supervision "api-warehouse-cancellation"
		- Mai "no-reply"