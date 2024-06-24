# Notes de réunion (par Bertrand)

==Que doit être le support dans la supply de demain ? 
  
## Rôle et organisation du support dans le domaine Supply 

### Selon le support  
  
- Prise en charge des tickets applicatifs (90% des cas créés par le métier)  
  - Interface entre les métiers et les équipes
  - Uniquement de la PROD
- Panel d’applicatifs large  
  - Legacy -> peu maîtrisé par les équipes de dév 
  - Savoir chercher les docs sur Confluence (pas tout le temps à jour)
- Top des applis  
  - PFN  - STK -> flux de descente de commande (BP pas générés, etc.)  
  - TRP -> affectations des transporteurs  
  - Sujets précis par vagues suite aux MEP
- 50% des tickets liés à des erreurs des utilisateurs  
- Bons échanges avec les équipes de dév sur les bugs possibles sur les nouveaux développements  
- TRP représente le plus gros volume d’incidents  
#### Irritants  
- Pas forcément de visibilité sur tous les flux (ex. : DSCP)  
- différence de vision du découpage entre le métier et les équipes  
  - process vs SF  
  - support doit faire le transcodage entre les deux pour cibler correctement les actions  
### Selon les équipes de dév
#### STK  
  
- Les équipes sont sollicitées sur des points techniques précis  
- Certains incidents sont traités directement par les équipes  
  - Hypercare sur les nouveaux composants
- Observabilité via Teams -> pris en charge directement par l’équipe  
#### TRP  

- Escalade vers l’équipe si besoin via Jira  
- Gestion de certains tickets directement par l’équipe  
  - notamment pour la gouvernance, les alertes remontées par le monitoring
- Pbs douane -> encore des déclarations de pb par mail au lieu de SH  
  - les tickets concernés semblent ne pas tomber au support appli
#### EDI  
  
- **Gestionnaires transport font les analyses eux-mêmes -> ce n’est pas leur rôle  
  - N’ont pas de connaissance sur le sujet  - Pas d’accès aux outils (logs, etc.) ou pas de connaissance des outils- Pas de caf pour l’accompagnement des gestionnaires  
- Impact 4C important -> Client + Cash  
  - Process de reprise lourds (pour Distri, principalement)=> **Qui a la responsabilité du support des flux qui concernent Distri  ?  
  - Le support n’a pas les accès aux applicatifs  - Il n’y a pas de proximité avec les équipes techniques Distrimag  - Sujet important à craquer en termes d’organisation  
  
#### Autres irritants  
- Certains développeurs n’ont pas les droits en production  
  - you build it, you cannot run it…  
- exemples : alerte DLQ arrive dans l’équipe de dév, mais il faut transmettre les informations de correction au support car pas de droits sur les bases de prod pour corriger  
- Si besoin de manipulation sur les déploiements, ce sont les équipes de dév qui s’organisent avec l’équipe d’exploit -> ce n’est pas en visibilité de l’équipe support  
  
- Support ODI  
  - Connaissance portée par quelques sachants uniquement  - Manque des sources de certains packages ODI  - **sujet ODI global à traiter à part  
  
## Que faut-il mettre en place comme accompagnement d’Amélie suite au départ de Tiphaine ?  
  
- Accompagnement par les équipes de dév  
  - moins de caf pour le delivery des autres sujets
- Connaissance transverse sur le support des domaines -> où sera la connaissance ?  
  - Notamment le ré-aiguillage des tickets si besoin
  - **Passage de connaissance à faire  
- L’incidentologie sur PFN et DSCP est en train d’être revue avec le domaine qui a récupéré la responsabilité


# Notes de réunion par moi-même