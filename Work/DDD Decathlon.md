---
ressource: 
author: 
link: 
trello: 
relates:
  - "[[Domain-Driven Design]]"
---
# Tour de table

- Fabien 
- Julien Coach technique cheez Shodo, plut sur partis
	 Accompagne les crlienrt sur leurs process
- Cédric : magasin, depuis 7 ans sur l'IT encaissement
	 - Product Manager
- Pierre Martial Security Officer 2 ans chez décathlon
- Anthony
	- EM
- Khaled
	- Product Manager : vision de la nouvelle solution d'necaissanemn
- Robin
	- Dev plutôt Java
- Florian
	- Dev plutôt Java
	- EM
	- Staff engeener => plutôt tech

- Cédric
- Pierre
- Anthony
- Khaled
- Robin
- Florian
# Rappel de l'après midi

Acculturation au DDD
Qui en a déjà entendu parler ?

- Cédric => Pas dans la culture
- Pierre
- Anthony => OUI
- Khaled => entendu parler, mais en attente de résultats
- Robin
- Florian => OUI
# Début de l'acculturation

Aligner le Business, l'orga et la tech
=> Meilleur alignement entre ce qu'on produit et ce dont on a besoin

Definition du DDD ?
> Tout ce qui a un impact sur l'opérationnel fait partie du business
> Toutes les personnes que tu vas interviewer font partie de ton business

Sécurité : une propriété du soft comme la Qualité
=> Sécu une de leurs craintes
=> Thread Modeling

Pourquoi le DDD dans votre contexte ?
- Anthony : poser une bonne organisation au sens large
	=> plus difficile:  se reposer les bonnes questions au fil de la vie du projet
- Pierre : remettre l'église au milieu du village

Tactique : comment j'écris mon code (technique)
Stratégique : comment je m'organise pour avoir le métier et ce que l'on va produire 

## Prez : Pourquoi le DDD ?

Architecture : on ne voit pas ce que ça fait.
	On ne comprends pas le jargon tech

DDD amène de la clarté sur les 3 types de complexités (les 2 premiers pour limiter la 3)
Démarrer du métier avant de commencer à faire des choix techniques et de penser framework.
Métier : qui doit driver le reste.

Modélisation générique peut amener des problèmes 
	- charge mentale
	- langages différents dev <=> PM (langage non aligné)
		- => sclérose
	- bien nommer les choses == faciliter les choses
		- éviter la "dette de design"
- Amener de la pérénité dans els softs et sortir du jargon tech

Design du produit logiciel a un impact sur le métier
Modéliser : on a l'impression que c'est plus de travail, mais en fait non.

Relation assez proche avec les gens du métier

Stratégie : exposer l'espace du problème 

## Prez : L'art de la modélisation

3 écrans : des modèles du métier
Parfois, on a besoin de'avoir une expertise de "comment presentments choses" pour exprimer correctement un besoin
=> Equipe produit : caractériser/qualifier le besoin

Le mot seul ne suffit pas : il faut également le contexte
Un même mot peut désigner des choses différentes en fonction du contexte

Polyonymie : un même concept et différents termes
=> on va éviter de multiplier les termes pour désigner une seule chose dans le contexte (diminuer la charge mentale et désambiguïser)
=> rendre explicite ce dont on parle

Question de Khaled :
On a un dictionnaire local et un dictionnaire global d'entreprise
=> comment on fait ?
=> ce que décrit : c'est un changement de contexte

Aligner la défintion entre tous les contextes, ça n'a pas de sens (exemple de la tomate)
Aligner tout le monde : il ne faut surtout pas faire ça.
Si on essaie d'aligner, on va coupler tout le monde

code defensif

Attention à ne pas tomber dans le piège du réalisme.

Comment détecter que le modèle n'est pas orthogonal avec les besoins.

# Prez: EventStorming

Objectif : avoir une discussion pour découvrir le métier
Architecture fonctionnelle / Architecture business
Architecture organisationnelle
prendre en compte l'organisation pour réfléchir aux effets délétères de la loi de conway
Estèce que l'organisation est orthogonale à ce qu'on veut mettre ne place ? Est-ce qu'on va subir des effets négatifs de la loi de conway?

Savoir à quel point on doit se protéger / laisser le modèles des autres transpirer chez nous
Définir les relations métier entre les contextes
Failure technique pour impacter la failure business

Personnes qui connaissent l métier
=> Filtrer en entrée

Vision du caching : ils savent ce qu'ils veulent
Taggué comme "tech"

Question : date
21-23