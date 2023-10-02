> Loi de Demeter

# 🧵 Thread de Tweets de moi-même

Wikipedia c''est bien, mais les articles universitaires c'est vraiment top ! Je viens de lire celui sur la Loi de Demeter, référencé par son article. La Loi de Demeter, ou "Principe de moindre connaissance" peut se résumer par "Ne parlez qu'à vos voisins les plus proches". [#OOP](https://twitter.com/hashtag/OOP?src=hashtag_click)

Loi de Demeter formelle : Pour toute classe C, pour toute méthode M de C, on ne peut appeler dans le scope de M, que les méthodes des objets : - en argument de M (dont C) - en variable d'instance de C - créés dans le scope de M (par M, ou par des méthodes appelées dans M

Pourquoi s'infliger ce genre de contrainte ? Comme souvent, pour : - Maximiser la Cohésion - Minimiser le Couplage

La cohésion est le degré auquel les éléments d'un tout vont ensemble. Deux éléments sont cohérents, quand ils sont utilisés ensemble, par un composant destiné à effectuer une seule tâche.

Le couplage est le degré d'interdépendance entre les composants d'un logiciel. Deux éléments de code, classes, composants ou modules sont couplés lorsque au moins l'un de deux utilise l'autre.

En pratique, l'article universitaire décrit 6 raisons concrètes. 
- Contrôler le couplage
- Masquer l'information
- Restreindre l'information
- Localiser l'information
- Maintenir de petites interfaces
- Induction structurale

### Contrôler le couplage 
Appliquer la loi de Demeter, permet aux méthodes de n'appeler que les méthodes qu'elles utilisent réellement. Cela permet de limiter les appelant des méthodes appelées, de mieux maitriser le couplage, et de donner une plus grande souplesse à votre logiciel.  

### Masquer l'information
En général, le non-respect la loi de Demeter s'illustre par la navigation dans grappe d'objets pour récupérer une info spécifique. La loi de Demeter encourage à masquer davantage les informations structurelles des objets et n'exposer que le nécessaire.  

### Restreindre l'information
Pour faire écho au point précédent, appliquer la loi de Demeter encourage à restreindre le scope (public, privé) des méthodes ou des classes. Il vaut mieux maitriser la propagation des informations à un scope donné (package, classe).  

### Localiser l'information
Respecter la loi de Demeter, encourage à limiter le scope des méthode et des classes. Ainsi, on va porter une plus grande attention à l'emplacement de nos méthodes et de nos classes : une information spécifique sera mieux localisée dans le logiciel.  

### Maintenir de petites interfaces
Utiliser la Loi de Demeter encourage à utiliser de petites interfaces spécifiques, qu'il est plus facile de remanier ou déplacer  

### Induction structurale
Quand on va écrire du code, on construit des phrases chargées de sens. Utiliser la loi de Demeter permet de construire des méthodes sémantiquement plus précises et ce sera plus facile de les induire (ie. de les deviner).  

Le Loi de Demeter vient avec son lot de compromis : Utiliser la loi de Demeter diminue la complexité des méthodes, mais multiplie la quantité de méthodes simples. Ce grand nombre de méthodes et de classes peut être difficile à maintenir et demande une bonne organiser modulaire.  

Le papier complet (disponible sur Wikipedia) : [https://www2.ccs.neu.edu/research/demeter/papers/law-of-demeter/oopsla88-law-of-demeter.pdf](https://t.co/uAyJvZHwi9)

## Ressources
- [Loi de Déméter](https://fr.wikipedia.org/wiki/Loi_de_D%C3%A9m%C3%A9ter "Loi de Déméter")
- https://twitter.com/fhiegel/status/1584560387571056640

