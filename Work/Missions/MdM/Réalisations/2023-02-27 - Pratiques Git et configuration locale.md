**Pratiques Git et credentials**

- ⛔ Ne pas commiter les user/password
	- Ils restent dans 1password
- ⛔ Ne pas commiter les fichier de credentials
	- Il restent dans les Bucket des comptes de service GCP
- :ghost: Ajouter un répertoire secrets dans les ressources, à ignorer avec .gitignore, dans lequel mettre les différents fichiers sensibles que vous utilisez en local
- :books: Documenter dans vos README :
- Comment accéder aux crédentials nécessaires à votre projet

ACTION
  Par opportunité : Faire le ménage des credentials.

**Pratiques sur les fichier de configu.ration local “application-local.yml”**

- Rappel : Le profil “local” est normalisé dans la stack MdM, notemment pour l’affichage des logs
- :scissors: sample.application-local.yml  Permet d’avoir un template à copier/coller avec des placeholder pour mettre en évidence des trucs à remplir
	- à commiter le sample, il y a moins de risque à pusher une information sensible
- :arrow_forward: Runner une application en local vers la recette est une pratique controversée
	- On le fait parfois quand on veut valider fonctionnellement son dev avant de le merger sur master
	- C’est pratique de cibler la recette car on a de la donnée correcte
	- :arrows_counterclockwise: Alternative possible : utiliser des tag “Release Candidate”
	  ex : 1.0.0-rc1, 2.3.9-rc6
	  Ce sont des tags qu’on peut se permettre de supprimer une fois le dev mergé et taggé avec une version stable.
	- On pourrait avoir des outils permettant de générer des fichier de conf à partir des configuration déployées sur Kube, mais cela semble overkill

ACTION
  Par opportunité : utiliser des sample.aplication-local.yml à la place des application-local.yml en leur appliquant les autres bonnes pratiques liées à la configuration