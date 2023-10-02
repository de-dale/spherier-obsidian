# Audit du MET

## Contexte

Florian demande un audit Tech du MET.

- Conception Logicielle
- Complexité
- Paramétrage
- Tests (Aspect Tech)
- Organisation

## Synthèse



# Ce qu'est le MET (Moteur d'éligibilité transporteur)

> Page Confluence de référence
> https://maisonsdumonde.atlassian.net/wiki/spaces/CORE/pages/1191739940/Moteur+ligibilit+Transport+MET

## Liste des composants
![[MET-carto-20230520.png]]
- api-carrier-delivery-engine
	- -
		- api-delivery-carrier
			- api-carrier
		- api-delivery-delay
		- api-delivery-carrier-prioritization
		- api-delivery-services-catalog
	- api-warehouse-product
	- api-preparation-array
		- api-shipping-point-engine
		- api-warehouse-stock-level
		- api-warehouse-stock-availability
		- api-warehouse-availability-date
		- api-prereservation
		- api-stock-external-supplier

- [x] Script de détermination des dépendances

# Analyse générale

- [x] Répartition du code
- [x] Facteurs de santé
	Facteur de santé Nb. VC %
	**Robustesse** 660 33,6%
	**Sécurité** 846 43,0%
	**Efficience** 157 8,0%
	**Evolutivité** 1 062 54,0%
	**Transférabilité** 17 0,9%
	TOTAL 1 967

## Conception logicielle

### Micro services

#### Pro

- Scalabilité fine
  - Maîtrise (?) des coûts de run
- Indépendance 
  - pour le delivery
    - Simplification des développements
  - Des bases

#### Cons

- Scalabilité / coût d'échelle 
  - pour les montées de version
  - pour les Contrats d'interface

- [x] Maturité des équipes ?

### Détails des projets

Architecture en couche
Modèle anémique
Modèle des contrats / Modèle métier / Modèle de persistance

## Complexité

### Complexité obligatoire

Besoin métier

### Complexité essentielle

Programmation réactive 
Kubernetes
Spring

### Complexité accidentelle

Overdesign ?

## Paramétrage

Quel est notre maîtrise du paramétrage ?

Gros du travail fait manuellement :
- Fichier Excel
- Rédaction des User Story
- Écriture de requêtes SQL
- Vérifications et tests
- Rédaction de templates de tests (depuis Sept. 2021)

Au début du projet, le paramétrage était prévu pour être immuable

## Tests

Maturité de l'équipe sur les tests
Rappel de la pyramide des tests et de quelques typologies de tests
- Tests unitaires
- Tests d'intégration
- Tests de composants
- Tests de contrats
- Tests end to end

## Organisation

Rappel de la Loi de Conway + pointeur vers le talk de julien

Communication équipe de réalisation <=> métier
Run, notamment avec le MCT
Adoption de l'Agilité
Multiples réorganisations (Marc, Fabian)
Métier "drivé par la technique"


# Analyse par composant

- api-carrier-delivery-engine
	- -
		- api-delivery-carrier
			- api-carrier
		- api-delivery-delay
		- api-delivery-carrier-prioritization
		- api-delivery-services-catalog
	- api-warehouse-product
	- api-preparation-array
		- api-shipping-point-engine
		- api-warehouse-stock-level
		- api-warehouse-stock
		- api-warehouse-availability-date
		- api-prereservation
		- api-stock-external-supplier

# Accelerate
💡Idée : reprendre les Capabilities, et noter leurs applications
[[Accelerate]]

![[Accelerate#Liste des Capabilities]]


# Interviews

## 2023-05-10rc

Deux équipes+
- Transport (mais Reverse et XPL)
- Stock

Intervenants / Responsables changeants
- Jean-Marc (JMD)
- Fabian
- Bruno Garcia
- Florian

> Remarque : aller voir Fanny HOAREAU pour la vision fonctionnelle du MET et LEO

### **Brique technique** 
ce qui a été fait en 1er

Micka a été mandaté à son arrivée pour étudier le MCT et rétro-engeneerer un schéma d'archi
Schéma d'archi du MET a été fait par l'archi qui a discuté avec le métier
	puis des discussion d'équipes (Dev+PO+Archi) pour en ressortir des notions (Transporteur/Délais/Produit)
	support des discussion : le fichie de paramétrage

Les US ont été faites ensuite à parti du schéma d'archi
> 💭 Moi ça me choque, mais il faut détailler pourquoi

PG qui ne savait pas découper des US
PG qui découvrait le métier de PO

Stack technique a drivé le schéma d'archi, au travers des composants à utiliser et par l'architecture en micro-services

#### Microservices
=> Le MCT est un monolithe, c'est une expérience qu'on voulait pas reproduire
=> a aidé l'équipe a faire du découpage technique et fonctionnel
=> N'était pas compris par JMD, qui était contre
=> Aujourd'hui, il semble que les µservices étaient une bonne idée

> 💭 Coût d'échelle ?

#### Architecture en couches

> Le fait de construire les API en trois couches api-model/model/persistant-model, ça avait été poussé par Micka ? ou par quelqu'un d'autre, autre chose ? C'était plutôt positif pour toi ? ou plutôt un frein ?

Poussée par les normes de la DSI
A priori assez facile à comprendre et à mettre en place.

#### Programmation réactive
Programmation réactive arrive en Sept 2021, avec les contraintes de perf enfin exprimées de la DIGIT.

> 💭 Communication ?

### Organisation

#### Agilité
Agilité toute fraiche
Equipe agile dès le début, mais tous n'étaient pas au même niveau de maturité.
Agilité par comprise par JMD, qui a nommé un Chef de projet pour le MET

Pratiques
- Rituels Agiles dès le début
- Review de code systématique
- Prémices de la CI de l'usine logicielle MdM
- CAB
- Très peu de TU, qui sont vraiment arrivés en Sept. 2021
- Pair avec Micka sur la mise en place de projets

Culture du blame
- 17000€ 
- Trop de pauses
- Se faire incendier par des problèmes en recette

Culture du partage modérée
- [x] Comment étaient partagée les connaissances ?

### Données 
#### Paramétrage
Vision initiale : un seul paramétrage qui ne change pas (ou peu)
Dans les faits, il a beaucoup changé et cela a beaucoup coûté à l'équipe

> 💭 Utilisation du paramétrage pour d'autres choses que du paramétrage
> 💭 Détournement du paramétrage (Litiges, bâtonnage)
> 💭 Manque de discernement sur l'expression de besoin / la valeur à apporter aux Users => Manque de discussion métier / équipe
> 💭 Manque de visibilité quand aux conséquences de la modification du paramétrage

