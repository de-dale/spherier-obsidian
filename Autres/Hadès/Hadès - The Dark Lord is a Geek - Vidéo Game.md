---
ressource:
  - 🗓️ Projet
link:
  - https://trello.com/b/jFv2ydtr/had%C3%A8s-the-dark-lord-is-a-geek
---
# Pitch

Créer  un jeu rtx / 4x en javascript où le joueur explore un monde souterrain pour faire grandir son donjon en quête des conditions de victoires
Pitch : jeu de gestion / 4x où vous incarnez un magicien sui veut montrer un "Magical social network".  
Pour ça, il doit construire une tour de magie.

# Ressources

- Or / euros / dollar
- mana
- électricité ?
- place

Idées :
- gain de mana par sacrifices
- voies bien/mal : faire de sa tour une échoppe ou un donjon, et traiter les aventurier/monstres en fonction de choix éthiques  
    => politiques en fonction des races comme stellaris
- proxy élémentaire pour attaques "man in the middle" sur les invocations
- créer des portails pour annexer des Mondes et agrandir sa tour. Plusieurs options :
    - emporter le "coeur du plan" pour faire grandir la Tour
    - annexer le monde pour utiliser ses ressources
    - fraterniser avec le plan pour utiliser une partie de ses ressources, et prendre le temps de synchroniser les énergies. Une fois les énergies synchro, faire grandir la Tour
- résister aux raids des héros
# Elements 

Les éléments permettent de rajouter un peu de Lore dans le jeu, ainsi qu'une gestion Pierre-Feuille-Ciseaux très simple

```graphiz
graph TD
A[Feu] --> B[Métal]
B --> C[Ténèbres]
C --> D[Poison]
D --> E[Pierre]
E --> A
B --> D
D --> B
C --> E
E --> C
A --> C
```

[[⛰️ Pierre]]
[[🔥 Feu]]
[[☠️ Poison]]
[[⚔️ Métal]]
[[🌑 Ténèbres]]

# Salles 
## Ressources

Salles au Trésor  
Mine  
Fonderie  
Armurerie  
Forge  
Bibliothèque  
Entrepôt  
Salle du trône  
Atelier  
Salle des potions / alchimie

## Vital

Dortoir  
Réfectoire  
Cuisine  
Cellier

Antre  
Portail  
Couveuse  
Invocation  
Sanctuaire

## Évolution

Salle d'entraînement  
Salle d'armes  
Piliers de feu  
Vivarium d'araignées / serpent  
Atelier de sculpture


# Races 

Liste non exhaustive, à agrémenter de truc du folklore

Humains & Cagoulés
Sorciers
Elfes & elfes noirs
Gobelins & Hobegobelins
Orcs  
Trolls & Géants
Salamandres  
Reptiles  
Dragon, Serpent
Insectes & Insectoides
Guêpes, libellules

Araignées

Nains  
Gnomes  
Lutin
Gremelins
Minotaures
Gargouilles (Imp => Gargouille => Balrock)
Démon

Féées
Sylphe, Nymphe, Dryade
Chimère
Lycanthopes, Gnoll


# Créatures

Formien, vegepygmé et peuple champignon  
Ettercap  
Draguerre  
Mites  
du coup, je cherche des trucs genre Gobelin, Homme-Rat, Kibold, Goules ; des montres bas level avec un minimum d'inté et de sociabilisation  
Troglodyte  
Drow  
Duergar  
Sniferblin ou gnome des profondeurs,  
Gobelin  
Kobold  
Nain

Morts-vivants

Gobelin, Orchestré, Troll, sorcier  
Gnome, Korrigan  
Nain, Elfes, Loup, Centaure, Faune, Satyre  
Goule, Squelette, Liche, Ombre, Terreur, Vampire  
Minotaure, Cerbère, Cyclope, Méduse/Gorgone  
Homme-rat, Ratskelins, Chimère  
Wurm, Guivre, Dragon  
Démon

# Victoire

Différents moyens de gagner une partie

- créer la grande Toile magique (construction)
- créer le grand réseau social magique
- conquérir la tour adverse
- tenir des positions pendant une période
- survivre à la lave / éboulement
- battre au prestige / devenir un dieu / course
mz'ger