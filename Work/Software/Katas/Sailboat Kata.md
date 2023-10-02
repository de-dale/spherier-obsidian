#software/kata 

> 🌶️ Débutant 
> 🕓 1h

![[sailboat-kata-overview.png]]
Vous êtes à la barre d'un petit voilier, qui cherche à atteindre une île. Votre bateau se déplace au tour par tour en fonction du vent, lequel change à chaque tour.

L'objectif de ce kata est de développer une fonction permettant de calculer la position du bateau à chaque tour.

## Déplacement du bateau

On modélise la position du bateau comme une grille à deux dimension, réputée infinie.

Le bateau se déplace avec les règles suivantes :
- Si le vent et le bateau sont sur deux axes orthogonaux, alors le bateau avance de 2 cases
- Si le vent et le bateau sont alignés, alors le bateau avance de 4 cases
- Si le vent et le bateau sont opposés, alors le bateau avance de 1 case
![[sailboat-kata-examples.png]]
## Ajustement du vent

A la fin de chaque tour, le vent change de direction, en suivant les règles suivantes :
- 25% de chance de tourner dans le sens horaire
- 25% de chance de tourner dans le sens anti-horaire
- 50% de chance de ne pas changer de direction

La force du vente évolue également, en suivant les règles suivantes :
- 25% de chance de gagner 30km/h
- 25% de chance de diminuer de 30km/h
- 50% de chance de ne pas changer de force
- si le vent dépasse 150km/h, une tempête se déclenche
- si le vent descend à 0km/h, un calme plat se déclenche

## Navigation

Avant de se laisser pousser par le vent, le navigateur oriente le bateau dans le sens qui lui semble optimum pour atteindre l'île.

Au début de chaque tour, le navigateur du bateau recalcule la direction du bateau pour se rapprocher au mieux de l'île.

Il peut faire tourner le bateau dans le sens horaire ou anti-horaire (ou ne pas modifier la direction) en fonction de la force du vent, de la position de l'île et de la position du bateau, de manière à optimiser le trajet.

## Backlog des sujet

> 💡Liste des idées, pas forcément à implémenter dans le kata

- Direction du vent
- Force du vent
- Modification du vent
- Vitesse
- Accélération
- Forme des voiles

Excalidraw : https://excalidraw.com/#json=C69Y9RquQZ53EvDke5W4s,pW6Dlg7VNop4KqFO8Ju8pw