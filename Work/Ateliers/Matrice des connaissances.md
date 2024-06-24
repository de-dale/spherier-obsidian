---
ressource:
  - 🛠️ Atelier
🕓 Durée: 🕓1h
👥 Participants: 👥2-n
🎯 Objectif:
  - 🤝 Partager
🌶️ Difficulté: 🌶️ Simple
tags:
  - Atelier
  - Knowledge
relates:
  - "[[Knowledge]]"
  - "[[Knowledge Management for Software Developers]]"
---
Cartographier le savoir de votre équipe

Dans le cadre du départ de l'équipe et de son intégration à la nouvelle équipe produit l'équipe APPRO a proposé d’extraire des différentes connaissances pour faciliter leur partage

Afin d'expliciter les connaissances es personnes qui partaient, j'ai eu l'occasion de dérouler un atelier de **matrice des connaissances**.
Influencé par d'autres ateliers j'ai utilisé un format qui a été assez bien reçu et je vous le partage ici.

🎯 **Objectif** : #🔭Découverte #🌶️Débutant
	Mettre en évidence les compétences et les connaissance des personnes de l'équipe et mettre en évidence des actions à mener pour limiter les risques liés à la perte
🕓 **Durée** : #1h🕓
👥 **Participants** : #👥2-n

# Déroulé

* Introduction 🕓 5mins
* Idéation 🕓 10 mins
* Convergence **🕓** 20-30 mins
* Evaluer les connaissances 🕓 5mins
* Evaluer les risques 🕓 5mins

## Introduction

Rappeler l'objectif.
Présenter l'atelier.
Présenter le déroulé

## Idéation

![[matrix-competences-ikagai.png]]
Sur un Ikigai (image du post) avec les Axes Technique / Interaction et Fonctionnel / Outillage, on positionne des post-its avec tout ce qui nous passe par la tête en terme de connaissance utile ou nécessaire à l'équipe.

### Détail des axes

* **Technique** : tout ce qui est lié au développement, aux Frameworks, au spécificité de code ou de pratique autour du logiciel
* **Interaction** : toute connaissance/compétence faisant intervenir une interaction avec une autre équipe
* **Fonctionnel** : tout ce qui a trait au fonctionnel/métier que l'on utilise
* **Outillage** : tout ce qui est relatif aux outils que l'on utilise.

## Convergence

Relire ensemble toutes les idées pour s'assurer que tout le monde comprenne bien le sujet dont il est question. Dédoublonner les post-its. Créer de nouveaux post-its. Regrouper les sujets similaires ensemble

## Evaluer les connaissances

Tout le monde évalue avec une note de 1 à 3 sa connaissance personnelle du sujet porté par le post-it :
* 🎓🎓🎓 Sujet bien connu
* 🎓🎓 Connaissances superficielles
* 🎓 Entendu parler du sujet (au moins au cours de l'atelier)

Chacun s'exprime sur chaque post-it. On n'est pas là pour juger de la note, mais pour avoir une idée du ressentis global de toutes et tous.

## Evaluer les risques
Tout le monde évalue avec une note de 1 à 3 sa impression personnelle de la criticité du sujet pour l'équipe :

* 🚨🚨🚨 Connaissance **Indispensable**
* 🚨🚨 Connaissance **Nécessaire** / Utile
* 🚨 Connaissance Utile / de **Confort** pour le projet

Chacun s'exprime sur chaque post-it. On n'est pas là pour juger de la note, mais pour avoir une idée du ressentis global de toutes et tous.

# Post traitement

## Compiler les données

Une fois qu'on a collecté les données, il faut déterminer ce qu'on en fait. Pour ça, j'ai mis les données dans un tableau en calculant le total "Connaissance" et le total "Criticité".

![[matrix-competences-data-as-table.png]]

## Tracer la matrice

Ca permet ensuite de de construire une matrice à la Eisenhower. On place les éléments en fonction de la connaissance disponible dans l'équipe, et de la criticité et en cas d'égalité, on se débrouille pour tout faire apparaître (quitte à déplacer d'autres éléments).

![[matrix-competences-data-as-matrix.png]]
L'objectif est d'avoir quelque chose d'exploitable et non pas quelque chose de mathématiquement parfait. C'est souvent plus important d'avoir les éléments positionnés relativement les uns par rapport aux autres que des éléments parfaitement placés.

D'ailleurs, j'ai construit ça à la main car je n'ai pas trouvé d'outil chouette qui le ferait à ma place. Les outils que j'ai trouvé me superposent les éléments qui ont les mêmes coordonnées, alors que je voudrais pour voir les ordonner pour tout faire apparaître.

Si vous avez un outil qui pourrais le faire, je suis preneur.

Après avoir positionné les éléments les uns par rapport aux autres avec une équipe on a rajouté un code couleur pour savoir si une info est plutôt technique ou fonctionnelle. Si on veut avoir une info très précise, on peut retravailler les données brutes sur l'étape #1 (l'Ikigai où on a les axes) et rajouter une échelle de notation.

L'important est surtout de savoir si
* une compétence/connaissance est maîtrisée par une ou plusieurs personnes
* une compétence/connaissance est nécessaire à une ou plusieurs personnes

Le résultat donne un truc comme ça :

![[matrix-competences-data-as-matrix-with-colors.png]]

## Analyser la matrice

Là, on arrive à la fin de l'exercice, on a une matrice qui appartient à l'équipe. Où toutes les infos utiles/nécessaires/critiques à l'équipe sont renseignées. Et que l'on peut faire évoluer : pas forcément besoin de refaire tout l'exercice, mais déplacer/repositionner les éléments.

Et surtout, on est en mesure de tracer des **quadrants :**
* ce qui est **très critique** et **peu connu** (↖️ en haut à gauche) : il y a un gros risque à ne pas faire de passation de connaissance => urgent de réfléchir à un plan d'action
* ce qui est **très critique** et **très connu** ( ↗️ en haut à droite) : risque mitigé est c'est le coeur de métier de l'équipe. Est-ce qu'on a ce qu'il faut pour onboarder rapidement de nouvelles personnes et pour faire en sorte que la connaissance ne se perdre pas ?
* ce qui est **peu critique** et **très connu** (↘️ en bas à droite) : des choses qui sont utilisés dans le quotidien de l'équipe. A priori, peu d'action à mener sur ce quadrant, mais c'est chouette d'identifier ces forces
* ce qui est **peu critique** et **peu connu** (↙️ en bas à gauche) : ce sont souvent des connaissances satellites à l'équipe, qui sont connues par d'autres équipes, ou dont on fait très rarement l'usage. Pas d'action ;à prévoir. S'il y a une montée en compétence/connaissance à faire, on se débrouillera le moment venu

# Vrac

Dans le cadre du départ de l'équipe et de son intégration à la nouvelle équipe produit l'équipe APPRO a proposé d’extraire des différentes connaissances pour faciliter leur partage

# Déroulé

Après avoir idée sur le modèle (ressemblant à un ikigai),; nous avons sorti un ensemble de connaissances. Pui nous avons évalué notre maîtrise de chacun de ces sujets et notre perception de leur criticité.

Le résultat est récapitulé dans le tableau ci-dessous

* 🎓 : La connaissance estimée de chacun sur le sujet
	* 🎓🎓🎓 Sujet bien connu
	* 🎓🎓 Connaissances superficielles
	* 🎓 Entendu parler du sujet
* 🚨 La criticité estimée par chacun sur chaque sujet
	* 🚨🚨🚨 Connaissance **Indispensable**
	* 🚨🚨 Connaissance **Nécessaire** / Utile
	* 🚨 Connaissance Utile / de **Confort** pour le projet

![[atelier-matrice-compétences.excalidraw]]

https://excalidraw.com/#json=12C5SBexAcF28_eCcwGs_,rpY6F2bYi05PMdaLR0KfZg

Deuxième partie

https://excalidraw.com/#json=12C5SBexAcF28_eCcwGs_,rpY6F2bYi05PMdaLR0KfZg
