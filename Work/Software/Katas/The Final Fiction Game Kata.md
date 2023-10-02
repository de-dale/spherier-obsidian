#software/kata 
# Game Engine

C'est quoi ?
C'est une plateforme orientée donnée, qui transforme de la donnée en une autre et l'affiche à l'écran. Un Jeu propose un moyen d'interagir sur ces données.

- Entrypoint : suetup et configure l'engine
- Application layer : gère les events
- Window layer : transforme les inputs en events
- Renderer : la partie qui affiche des trucs à l'écran
	- redner API
- Debugging
- EntityConverterSystem


# The Final Fiction Game Kata  

Voir aussi [[RPG Combat Kata]]
  
Un jeu de rôle (Role Playing Game ou RPG en anglais) est un jeu où un joueur (parfois plusieurs) choisit d'incarner un personnage (parfois plusieurs) dans un monde immaginaire. Chaque personnage est amené à prendre des décision pour évoluer dans le jeu.
Souvent, un jeu de rôle est découpé en trois phases de jeu distinctes : l'Exploration, le Combat et les Discussions (et autres interactions sociales)

Le but de ce kata, est de développer un moteur de jeu permettant de simuler les combats. 

L'exercice propose plusieurs chemins. 
- Inside Out : où chaque étape est très détaillée 
- Outside In : où l'étape est décrite de façon plus macroscopique
	  L'idée est de pouvoir donner des inputs pour laisser libre court à la créativité de chacun pour aller au bout du kata.

# Inside Out
  
## Attaquer  
  
- Un personnage peut subir des dégats  
- Quand un personnage subit des dégats, le montant des dégats est déduit de son total de points de vie  
- Un personnage peut attaquer un autre personnage  
- Lorsque l'attaque contre une personnage réussi, le personnage ciblé subit les dégats de l'attaque  
- Chaque personnage peut choisir entre différentes attaques  
  - Attaque légère : 90% de chances de réussir et inflige 5 dégats  
  - Attaque standard : 60% de chances de réussir et inflige 15 dégats  
  - Attaque lourde : 30% de chances de réussir et inflige 30 dégats  
- Lorsque les points de vie d'un personnage atteignent zéro, le personnage devient hors comabt et ne peut plus attaquer.  
  
## Factions  
  
Dans un combat, il y a deux camps :  
- les adversaires et les alliés  
  
Les personnages ne peuvent attquer que leurs adversaires

# Deuxième rédaction

## 1v1 Déterministe

Dans cette étape, on cherchera à résoudre un combat entre deux personnages en un contre un.
1. Les deux personnages peuvent être différents.
   Le premier personnage qui met l'autre hors combat, gagne l'affrontement.
2. Les deux personnages sont identiques.
   Le premier personnage à jouer gagne l'affrontement.
2. Les deux personnages peuvent être différents.
   Le premier personnage dont le cumul des attaques, dépasse les points de vie de l'autre, gagne l'affrontement.

Indices :
- Le combat peut être découpé en tours de jeu
- à chaque tour de jeu, chaque personnage attaque une seule fois
- L'ordre dans lequel jouent les personnages à chaque tour, est déterminé au début du combat, et ne change pas par la suite
- Lorsque les points de vie d'un personnage atteignent zéro, le personnage devient hors combat.
- Quand un personnage est hors combat, il ne peut plus attaquer.
- A la fin du tour, quand son adversaire est hors combat, le personnage gagne la partie

## 1v1 Tactique

Dans cette étape, on cherchera à résoudre un combat entre deux personnages en un contre un.
Les deux personnages peuvent avoir des styles de jeu différents. Il ne suffit pas de commencer pour gagner. 

Indices :
- Les deux personnages sont dotés d'une IA identique
	- L'IA a pour vocation de déterminer les actions du personnage à son tour de jeu
- A son tour de jeu le personnage choisit une attaque parmi les trois attaques suivantes
  - Attaque légère : 90% de chances de réussir et inflige 5 dégats au défenseur
  - Attaque standard : 60% de chances de réussir et inflige 15 dégats au défenseur
  - Attaque lourde : 30% de chances de réussir et inflige 30 dégats au défenseur
- Au début de chaque tour de jeu, on détermine lequel des deux joueurs commence.

# Features à prioriser
- Résolution de l'attaque
- Choisir parmis d'autres actions que l'attaque
	- Se défendre
	- Se soigner
- 2v2
	- Introduire la notion d'alliés et d'adversaires
	- Permettre de choisir la cible
	- Ajouter une attaque permettant de cibler plusieurs adversaires
- Position tactique
	- Devant / Milieu / Arrière
	- Nouvelle action : changer de position
	- Modificateurs de position (Bonus/Malus en fonction de la cible et de la position de l'attaquant)
	- Ajout de la notion de "portée" sur les actions
- Pierre / Papier / Ciseau
	- Introduire la notion de type
	- Modificateur des dégat des attaques en fonction du type de l'attaque et du type de la défense
- Affichage
	- Afficher la barre de PV en pourcentage
	- Ajouter l'action "consulter les infos de mes alliés" 