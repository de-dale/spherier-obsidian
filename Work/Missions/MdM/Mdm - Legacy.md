# Comment je défini mon héritage ?

Pour définir notre héritage, nous allons nous appuyer sur des indicateurs pour mesurer à quel point un composant logiciel ou d’infrastructure est identifié comme “Legacy”.

Grace à ces indicateurs nous allons pouvoir afficher les risques pris à ne pas moderniser ces composants mais aussi comprendre pourquoi nous ne l’avons pas encore fait (ex - coûts de modernisation versus stabilité du composant versus risques).

* Indicateurs :
    * **Maitrise / Compétences / Documentation** : cet indicateur mesure notre niveau de maitrise d’un composant logiciel ou d’infrastructure.
        * Avons nous encore les bonnes compétences pour le maintenir et le développer ?
        * Avons nous de la documentation pour assurer son maintient en condition opérationnel et son développement dans les meilleures conditions ?
        * Nous parlons ici de gestion documentaire, d'on-boarding, d’off-boarding, de gestion du changement et de matrice des compétences.
    * **Obsolescence / Fin de vie / Maintenance / Support** : cet indicateur mesure le cycle de vie d’un composant et ce que ça implique.
        * Plus le temps passe et plus se pose la question des risques pris à conserver un composant sous sa forme originelle (ex - risque de panne car l’usage a changé, plus de maintenance, …).
        * Est-il toujours utilisé par un métier Maisons du Monde ?
        * Peut-il y avoir des lenteurs liées à la profondeur d’historique des données du composant ?
        * L'éditeur existe-t-il toujours (ex - arrêt d’activité pour raison économique, rachat, …) ?
        * Un éditeur met-il toujours des correctifs à disposition ?
        * Un éditeur fournit-il toujours du support ?
        * Y’a-t-il toujours la possibilité de contracter une maintenance chez un éditeur ?
        * Il faut savoir que plus le temps passe plus le coût de la maintenance peut être élevée car l'éditeur doit investir pour continuer à garantir le bon bon niveau de service.
        * Si nous parlons d’un composant open-source, on parlera plus d’intégrateurs/ESN pouvant assurer le support de la version du composant que nous utilisons, d’acquisition du composant par un éditeur (ex - Oracle et MySql), de projet abandonné faute d’avoir une communauté active pour le porter ou de fin de vie de la version de notre composant car la communauté doit porter ses efforts sur les versions récentes.
    * **Sécurité** : cet indicateur permet de mesurer le niveau de sécurité du composant en prenant en compte plusieurs facteurs.
        * Exposition du composant (ex - site web Maisons du Monde versus notre solution de comptabilité).
        * Mises à jour régulière du composant, surtout celles liées à la sécurité.
        * Présence ou non d’une solution de protection du composant (ex - datadome).
        * Difficulté de mise en conformité du composant vis à vis de certaines règles (ex - NIS2).
    * **Complexité / Interdépendance** : cet indicateur mesure à quel point il peut être difficile de faire évoluer un composant, à quel point il est important et présent dans notre SI.
        * On parlera ici de problématiques d’intégration de nouveaux composants car il sera difficile de les interconnecter avec le composant “Legacy” ou de problématiques d'évolution car sa conception et son usage sont complexes et nécessitent un bon niveau de connaissances que nous n’avons peut-être plus depuis le départ de certains collaborateurs.
        * On parlera aussi de coûts élevés pour moderniser le composant car il se trouve au centre de notre SI et plusieurs équipes seront nécessaires pour réaliser le projet.
    * **Stabilité / MCO** : cet indicateur mesure la stabilité du composant et son coût en actions à réaliser au quotidien pour le maintenir en condition opérationnelle.
        * Les composants “Legacy” sont souvent des systèmes complexes nécessitant de nombreuses tâches à faible valeur ajoutée qui mobilisent les équipes. Les composants modernes permettent plus d’industrialisation, d’automatisation et font gagner les collaborateurs en productivité.
        * Les composants “Legacy” peuvent être sujets aux pannes plus régulièrement si certaines tâches quotidiennes ne sont plus réalisées (ex - plus de mises à jour car plus de correctifs disponibles, plus d’actions d’exploitation car perte de connaissances suite au turn-over de l’équipe et pas de documentation, architecture non résiliente car non prévu dans le projet vis à vis de l’usage, …).

# Quel est mon héritage, quels sont les risques et pourquoi je ne me lance pas ?

* Une colonne composant logiciel ou d’infrastructure identifié comme “Legacy”.
* Une colonne par indicateur et 3 couleurs pour mesurer le niveau de risque :
    * Vert : risque faible.
    * Orange : risque moyen.
    * Rouge : risque fort.
* Une colonne pour indiquer si des travaux sont déjà engagés.
* Une colonne impact(s) visible(s).
* Une colonne commentaire(s).

| **Composant logiciel / d’infrastructure “Legacy”** | **Sécurité** | **Maitrise**<br>**Compétences**<br>**Documentation** | **Obsolescence**<br>**Maintenance**<br>**Support**<br>**Fin de vie** | **Complexité**<br>**Interdépendance** | **Stabilité**<br>**MCO** | **Des travaux de modernisation sont ils déjà engagés ?** | **Impact(s) visible(s)**                                                                                                               | **Commentaire(s)** |
| -------------------------------------------------- | ------------ | ---------------------------------------------------------- | -------------------------------------------------------------------------------- | ----------------------------------------- | ---------------------------- | -------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------- | ------------------ |
| ODI                                                |              |                                                            |                                                                                  |                                           |                              |                                                          | Bloquant pour le projet Pimp My ERP<br>Impact direct sur notre capacité à mettre à jour la base de données Oracle GNXPROD en 19C ! | **JAVA 1.5**       |
