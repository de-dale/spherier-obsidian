---
ressource:
  - 🧩 Serious Game
author: "[[Fabien HIEGEL]]"
tags:
  - SeriousGame
---
Jeu provenant d'une discussion avec [[David FRANCK]] sur le jeu TDD "les règles du jeu sont plus difficiles que les règles du TDD"

**Mon objectif par ce jeu :** 
- Faire découvrir le TDD (et peut-être d'autres pratique) avec des choses qui émergent par le jeu via un mécanisme de combo, le combo récompense les "bons" comportements

https://docs.google.com/presentation/d/1I6rXWwpuLeUPOcZ-i9GuQqp75Dn5czNxCmTYjkz0O_I/edit#slide=id.gcb6157e1b1_0_0

![[TDD Deck Building 2023-06-26 16.16.53.excalidraw]]
# Idées en vrac

On a 3 ressources
- des Sous : Le Budget. Quand on n'a plus de sous, on a perdu
	- Les cartes sur la table coutent des Sous
	- Piocher coute des Sous 
	- Avoir des User Story entamées coute des sous
- De l'Effort que l'on achète avec des Sous
	- Les cartes en main coûtent de l'Effort
- De la Valeur Ajoutée, que l'on achète avec de l'Effort ou avec des Sous
	- La Valeur Ajoutée pourrait permettre d'avoir des Sous

TDD = Combo
=> RED:GREEn/Refactor permettent de rejouer

## Déroulé d'un tour de jeu

1. Chacun joue
	1. Chaque joueur
	2. Chaque projet
2. On fait la rétro
	1. chacun peut acheter autant de cartes et les mettre dans sa défausse
3. Calcul du budget
	1. On compte les Sous qui entrent
	2. On compte les sous qui sortent
		1. 1x💲/ Projet
		2. 1x💲/ Joueur

## Cartes

- (base) : +1 Effort
- (base) : +2 Effort
- (base) : -1 Effort => +1 VA
- (base) : -2 Effort => +2 VA
- RED (1E) => peut poser une carte <2E sans en payer le coût
- GREEN (2E) => ?
	- Si jouée gratuitement, permet de piocher gratuitement
	- Si jouéé gratuitement permet d'acheter gratuitement
	- Si jouéé gratuitement donne de l'effort
- REFACTOR (2E) => Permet de défausser de la VA pour acheter des cartes au milieu
- RED/GREEn/REFACTOR : Rembourser el coût en Effort / piocher gratuitement
- Découper des US : permet de mettre de la VA en prod
- Deployer : mettre de la VA en prod
- CI : réduire les événements lors d'un deploy
- Usine logicielle : réduire l'effort pour faire des trucs
- Test unitaire
- TNR manuelle
- TNR automatisée
- Tests exploratoire
- Refinement
- Example Mapping
- Rétrospective
- Formation : monter le niveau d'une carte, puis retirer "Formation de la partie"

## Evénements
- Refill : Le Codir remet des sous sur la table pour faire avancer le projety
- Coupûre budgétaire
- Bug: un bug arrive en prod / en dev
- Déscoper : Une US est déscopée. Tout ce qui est en dev dessus est défaussé
- On boarding : on acceuille un nouveau
- Démission : une personne part
- Revue fonctionnelle : de la Valeur ajoutée en DEV est défaussée si pas testée

# Victoire
quand toutes les US du projetysont finies