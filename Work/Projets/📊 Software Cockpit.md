---
ressource:
  - 🗓️ Projet
---
# Plan d'action

- [ ] Software Cockpit : Extraire proprement les informations du pom
- [ ] Software Cockpit : Extraire proprement les informations Kube

# Notes

- Intégrer la date de dernière analyse SONAR
- Récupérer les version déployées via le "deployments" de gitlab
- Poquer la récupération des issues gitlab pour construire des graphes d'équipe (pratiques, matrice de connaissance, tech radar)
	- Voir aussi si on peut construire des métriques à partir des issues (exemples : maintenabilité ressentie)

# Références

Logiciel permettant de disposer d'une visibilité sur le parc applicatif, de métriques, permettant d'identifier où mettre les efforts pour réduire la dette technique, le risque de sécurité

> // TODO : lien avec JIRA : récupérer les ACOT qui ont été identifiées pour un composant donné TOKEN_JIRA:ATATT3xFfGF0m92FTdIGI-XPm5HZenu28T0pHgBz84P9GxQXYm-sVN6d4A6n3vG7d8dQts8iAVB4hGtAk677vu4rLU1A1SMF9kp1ey2bWDWq46R4JQ8sAJVNfTRW8LcN-R4c9x7JZDXDVF13OKBSgJ6xSWg_r0yd2tpMYnlgsq2gcEhQwu-zgeE=B256E64B  
> // TODO : Tech radar : on peut lister et compter le nombre de technologies, et les comparer à un techradar  
> // TODO : savoir si on a l'agent new relic  
> // TODO : Nombre et durée des MR  
> // TODO : collecter les versions déployées vs : le code non déployé  
> //            => $ kubectl describe deployment api-carrier-delivery-engine-v1 --context=mdm-k8-cluster -n customer-delivery-rec --kubeconfig=''  
> //            => $ kubectl get deployment api-carrier-delivery-engine-v1 --context=mdm-k8-cluster -n customer-delivery-rec --kubeconfig='' -o jsonpath="{..image}"  
> //      => Comparer les versions avec le package semver  
> // TODO : lister les dépendances vers les autres contrats  
## Métriques par Florian ROINET  
  
> Comme discuté, la liste des métriques agrégées que j'observe mensuellement :  
> - % de projets où la QualityGate est activée (pré-requis : notes Sonar A-A-A-A)  
> - Volume de code sur mes systèmes fonctionnels  
> - Taux de couverture des tests auto  
> - Quali Sonar (SAST) : nombre de "Bugs statiques", Vulnérabilités+Hotspots de sécurité, CodeSmells  
> - Efficacité du workflow dev : durée moyenne de traitement des Merge Requests (délai review ; délai merge master)  
> - Sérénité des MEP : nombre de MEP normales vs urgentes  
> - Stabilité du Run : (via dashboard SH) -> Nb tickets mensuel, nb restant à traiter, âge du plus ancien etc.  
> - Intégration de l'usine logicielle : nombre de projets par  
> - Version de JDK  
> - Version de pipeline  
> - Version Spring  
> Puis je visualise ça graphiquement :  
> - Pour faciliter l'analyse  
> - Pour voir l'évolution dans le temps et les tendances  
> L'intérêt pour moi de tout ça / ce que j'en ressors :  
> - Identifier où mettre l'effort, dans un contexte qui laisse peu de place à l'ACO Technique  
> - Donner régulièrement de la visibilité à l'équipe, apporter matière à discuter de nos pratiques  
  
## Besoin  
  
> le temps passé par florian R. mensuellement multiplié par le nombre d'équipe + le reporting régulier que vous faites   
> pour nicolas D. + une toutouille supplémentaire ça serait acceptable comme impact chiffré ?


## Software cockpit @Pierre FEVRIER

- Vision by @[[Pierre FEVRIER]]
    - Besoins :
	    - Inventorier l’ensemble de nos composants et leurs caractéristiques pour être en maitrise de notre patrimoine logiciel
		      Ce travail est aujourd'hui manuel et non factorisé.​ 
		      L'objectif du projet est d'automatiser ce processus et d'en historiser les résultats.
	- One Pager:
		- Le patrimoine applicatif MDM est constitué de centaines de composants (=plus petite unité logicielle livrable) dont nous devons suivre l'obsolescence, les risques de sécurité ainsi que la maintenabilité.​
		- Risques à ne pas faire​
			  Passer à côté d'une faille de sécurité critique qui mettrait le SI en péril​
		- Populations​ Impactées​
			   Tous les acteurs de la DSI​
		- Le projet sera une réussite lorsque toute personne de la DSI pourra consulter simplement l'état d'obsolescence, les risques de sécurité et le niveau de maintenabilité d'un composant logiciel.​
			- Lot MVP : proposer un front qui regroupe les KPI prioritaires pour chaque composant logiciel de la DSI et qui permet de consulter la photo du patrimoine applicatif MDM.
			- Lot 2 : historiser chaque KPI remonté pour pouvoir consulter les tendances
- Présentation d’un outil permettant de générer un “inventaire” des versions utilisés sur des projets Java mis au point par @Fabien HIEGEL
- Un dashboard mis à jour manuellement par [[Florian ROISNET]]
Echange à retrouver via le replay.

Les pointeurs évoqués en séance :
- La conf Devoxx inspirante 
	  [Gestion de la dette d'architecture dans un contexte d'hypercroissance (Cyril BESLAY)](https://www.youtube.com/watch?v=F30CJnmzI8Y)
    - Le deck associé : [Arkup Meetup Nantes 2023 - Gestion de la dette d'architecture dans un contexte d'hypercroissance](https://speakerdeck.com/cicoub13/arkup-meetup-nantes-2023-gestion-de-la-dette-darchitecture-dans-un-contexte-dhypercroissance)


## Criticité Business 

**Criticité :**

- **CRITIQUE** : Le business est fortement impacté en cas de dysfonctionnement AVEC perte de chiffre d’affaire immédiat _(ex: MET : Les clients n’ont plus la possibilité de commander un produit)_
- **IMPORTANTE** : Le business est indirectement impacté en cas de dysfonctionnement SANS perte de chiffre d’affaire à court terme. _(ex: L’application de réapprovisionnement des magasins n’est plus disponible)_
- **MOYENNE** : Le business n’est pas directement impacté en cas de dysfonctionnement mais perte de temps pour les métiers _(ex: L’application permettant de faire l’inventaire des stocks en magasin n’est plus disponible)_
- **FAIBLE** : Le business n’est pas directement impacté en cas de dysfonctionnement et a un impact faible pour les métiers. _(ex: L’application de consultation des statistiques de qualité des produits en entrepôt n’est plus disponible)_

|  |  | **Impact sur le business (perte de chiffre d’affaire)** |  |  |
| ---- | ---- | ---- | ---- | ---- |
|  |  | **FAIBLE** | **MOYEN** | **IMPORTANT** |
| **Impact pour les utilisateurs métier (perte de temps)** | **FAIBLE** | *faible* | moyenne | ==**CRITIQUE**== |
|  | **MOYEN** | moyenne | **IMPORTANTE** | ==**CRITIQUE**== |
|  | **IMPORTANT** | **IMPORTANTE** | **IMPORTANTE** | ==**CRITIQUE**== |

## [[Axes de priorisation du Legacy]]

# Expérimentations


Récupération des données dur un repo

```yaml
stages:  
  - data  
  
data:collect:  
  image: node:latest  
  stage: data  
  script:  
    - cd src/apps  
    - npm ci  
    - GITLAB_PERSONAL_TOKEN="${GITLAB_PERSONAL_TOKEN}" SONARQUBE_PERSONAL_TOKEN="${SONARQUBE_PERSONAL_TOKEN}" npm run cockpit  
    - find data \( -name "*.json" -o -name "*.csv" \) -exec cp --parents '{}' ../.. \;  
    - cd ../..  
    # GitLab: Author 'supply-software-cockpit@maisonsdumonde.com' is not a member of team  
    - git add data  
    - git config user.name "supply-software-cockpit"  
    - git config user.email "fhiegel@maisonsdumonde.com"  
    - |  
      NOW=$(date +"%Y-%m-%d")  
      git commit -m "data(${NOW}): Collect data"  
    - git remote set-url --push origin "https://$TOKEN_NAME:$ACCESS_TOKEN@git.maisonsdumonde.net/core/dev/scm/supply-software-cockpit.git"  
    - git push origin HEAD:$CI_COMMIT_BRANCH  
  rules:  
    - if: $CI_COMMIT_BRANCH == 'collect-data' && $CI_PIPELINE_SOURCE == "push"  
      when: manual  
    - if: $CI_COMMIT_BRANCH == 'collect-data' && $CI_PIPELINE_SOURCE == "schedule"
```