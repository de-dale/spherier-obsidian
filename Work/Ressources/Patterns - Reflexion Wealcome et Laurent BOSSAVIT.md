---
ressource:
  - 💬 Slack
relates:
  - "[[Design Patterns]]"
---

**Matthieu Clin**  [il y a 7 jours](https://wealcome.slack.com/archives/C3Y0Q43RV/p1700738070050619)  

> Bonjour à tous !
> Comment faites-vous pour progresser en pattern ? Et surtout comment faites-vous pour faire progresser les autres sur ce point ? Vous avez des exercices ? Une méthode ?Un point qui me titille avec mon équipe ces dernières semaines c'est la compréhension des patterns (dernier exemple le strategy pour choisir la méthode d'upload selon des paramètres au runtime) et encore plus d'implémentation...Le seul souvenir que j'ai pour ça c'est les cours de diagramme très pénible a faire sur papier.

---

![](https://ca.slack-edge.com/T3Y0Q3UA3-UR9DTT3EV-4784e53fc041-48)

**Edouard**
> [www.refactoring.guru](http://www.refactoring.guru/)C'est la meilleure ressource que je connaisse, et elle est gratuite.

![](https://ca.slack-edge.com/T3Y0Q3UA3-U05CNBQ1VV4-gc855088944b-48)

**Matthieu Clin**
> Merci !Vous faites des exercices ensemble sur le sujet ?

**Vincent Therry**  [il y a 7 jours](https://wealcome.slack.com/archives/C3Y0Q43RV/p1700746285575439?thread_ts=1700738070.050619&cid=C3Y0Q43RV)  
> Connaitre l’implementation d’un pattern par coeur n’a pas d’intérêt à mon sens. les techno évoluent vite etc.  
> Par contre il faut connaitre le nom des patterns et la logique derrière et savoir reconnaitre lorsqu’on a besoin d’appliquer tel ou tel pattern.  
> C’est exactement ce que propose refactoring.guru je crois + quelques implem dans des langages

**Vincent Therry**  [il y a 7 jours](https://wealcome.slack.com/archives/C3Y0Q43RV/p1700746309537299?thread_ts=1700738070.050619&cid=C3Y0Q43RV)  
> faire des exos ensemble, je ne vois pas l’intérêt à part si l’équipe est très junior

**Vincent Therry**  [il y a 7 jours](https://wealcome.slack.com/archives/C3Y0Q43RV/p1700746343806459?thread_ts=1700738070.050619&cid=C3Y0Q43RV)  
> dans la vraie vie on reçoit des specs fonctionnelles et on a arrive à les coder sans s’entrainer. Pourquoi il serait différent d’écrire un pattern si on a le diagramme du pattern sous les yeux

**Edouard** 
> Je pense que le mot clé intéressant dans la phrase de Matthieu n'était pas "exercices" mais "ensemble".  
> Et je pense que si l'équipe ne connaît pas tous les design patterns, (ce que j'ai vu dans la majorité des équipes où j'ai bossé), alors ça peut être super intéressant de faire de petites présentations sur des cas concrets de la base de code de l'équipe.

**Matthieu Clin**  
> Pour une problématique donnée, trouver les patterns qui pourraient aider et les implémenter ne semble pas trivial pour beaucoup de monde. Du coup ils ne le font pas et code quelque chose loin d'être optimale.Je pensais faire des présentations mais sans pratique ça ne marchera jamais à mon avis


**Laurent Bossavit**  [il y a 7 jours](https://wealcome.slack.com/archives/C3Y0Q43RV/p1700749184858119?thread_ts=1700738070.050619&cid=C3Y0Q43RV)  

> Fondamentaux > patterns
> Historiquement le mouvement des patterns n'avait pas pour vocation de diffuser des solutions toutes faites mais d'encourager à une pratique essentiellement littéraire, consistant à décrire en "pattern form" les apprentissages glanés localement par les équipes de dév. (Cf les nombreuses conférences PLoP et les publications associées.)
> 
> Evidemment on a tout compris de travers par paresse intellectuelle. !😅 Je commencerais par travailler sur les "4 rules of simple code" et chercher des exemples de complexité croissante montrant comment les patterns ont été des moyens d'aboutir à cet idéal: du code découplé, sans redondance, expressif et minimaliste une fois les autres critères satisfaits.
> C'est intéressant aussi de décortiquer la notion même de pattern et faire apparaître les éléments clés du "pattern form": 
> - une situation problématique, 
> - les forces en présence dans la situation,
> - la solution qui résout ces forces, 
> - les problèmes résiduels qui restent après l'application de la solution,
> - les patterns voisins qui viennent intervenir sur le résiduel.
> 
> Il vaut mieux le voir en mob/ensemble/team programming ou en coding dojo que chercher à l'apprendre par coeur à partir des bouquins…

**Laurent Bossavit**

> Et en parlant de bouquins le GoF était déjà une terrible distorsion par rapport à l'esprit d'origine de la communauté des patterns.

**Laurent Bossavit**

> En fait le mieux ça pourrait même être de commencer par travailler sur les fondamentaux et la notion de "solution à un problème récurrent" en se focalisant sur les patterns qui **émergent de l'équipe et de son expérience**, sans même chercher à leur enseigner aucun pattern "classique".Une équipe qui aura appris à formaliser ses propres patterns (et la logique de construction qui est derrière) n'aura ensuite aucun mal à évaluer et acquérir les patterns classiques.

**Matthieu Clin**

> Je comprends ce que tu proposes, c'est effectivement le plus beau chemin mais celui qui est le plus compliqué à paver ! Tu as eu l'occasion de le pratiquer dans tes équipes ?

**Laurent Bossavit**

> Disons que ça fait bien longtemps que j'ai abandonné l'idée de transmettre de la connaissance "telle quelle" sur les patterns. Dans les équipes que j'ai cotoyées j'essaie plutôt de travailler sur les fondamentaux, du code qui passe ses tests d'abord (donc écrire des tests, avant ou après, de préférence avant), ensuite du code avec peu de duplication, qui soit expressif et en dernière priorité le plus concis possible. Bref mon socle c'est les "4 règles de simplicité" de Beck et c'est déjà du taf.
> 
> Le travail d'écriture sur les patterns c'est quelque chose que j'ai eu moins souvent l'occasion de faire en direct au taf, ça demande déjà de la maturité, c'est plus un truc que j'ai fait de temps en temps en unconference style SoCraTes. Par contre en clientèle ou avec des collègues dévs, qu'on soit en ensemble/mob ou en binôme, j'insiste souvent pour avoir un minimum de prise de notes en mode "qu'est-ce qu'on a appris ici"… et quand ça matche un pattern ça donne l'occasion d'en parler.

**Matthieu Clin**

> C'est un travail continue c'est sûr. C'est ce que je ressens également. Mon équipe s'est récemment agrandit et je remarque la différence de niveau. Ce qui est a la fois gratifiant et frustrant (d'avoir a recommencer).Comment travailles tu l'aspect "test" si les principes ne sont pas maîtrisé et que ça donne n'importe quoi. Pour faire progresser sur ce point (les tests) j'ai l'impression qu'il faut un monde avant (dont les paterns mais surtout solid).

**Laurent Bossavit**

> J'ai pas eu ce sentiment mais si tu as des exemples qui te viennent de trucs sur lesquels les gens bloquent j'adore échanger là dessus, ça me permet de comprendre ce qu'on leur a mal expliqué et souvent j'en tire des idées pour améliorer ma façon de présenter.
> 
> A la base le domaine de prédilection des tests c'est les fonctions pures, même dans le monde objet on peut commencer par se concentrer là dessus. Plus tu internalises "State is Evil" moins tu as de souci au niveau des tests. Dans le prolongement de ça on apprend à voir les classes comme des petits programmes avec de l'état, qu'on cherche à minimiser (state is evil) et à garder local plutôt que d'en faire profiter les autres classes (don't touch others' state, aka Law of Demeter). On va préférer la composition à l'héritage, ça simplifie les tests aussi. Déjà avec ça on s'en sort pas mal.

**Matthieu Clin**

> Je n'y manquerais pas la prochaine fois, merci pour ta proposition !

**Pat Och**

> [[Laurent Bossavit]] ta réponse est magique ! 🙏

**Pat Och** 

> [[Laurent Bossavit]] stp as tu une ressource à nous conseiller sur les 4 "rules of simple code"

**Laurent Bossavit**

> Cet article est pas mal: [https://martinfowler.com/bliki/BeckDesignRules.html](https://martinfowler.com/bliki/BeckDesignRules.html)

> When developing Extreme Programming in the 90's, Kent Beck developed four rules of simple design: Passes the tests, reveals intention, no duplication, and fewest elements. (43 ko)

**Matthieu Clin**

> Vu que vous êtes là messieurs ! ! 😂
> 
> La première étape c'est d'avoir un code testable avant d'aller plus loin. Vu qu'un test unitaire c'est sur un "module" (plusieurs classes tout ça tout ça) qui est délimité par des interfaces (ou au moins des objets injectables).Comment fais-tu Laurent pour démarrer ? Tu définis en amont les contours pour guider le dev ? Ou tu pars du principe que même si ça reste une classe ce n'est pas grave et c'est un début et on verra plus tard pour faire mieux ?

**Laurent Bossavit** 

> Je sais pas si j'ai compris la question 🤔
> Pour démarrer généralement (il y a des exceptions) je pars d'un besoin métier, exprimé avec un test un peu macro autour des objets concernés: « outside in ». Selon les cas si l'implémentation n'est pas évidente je passe par un « fake » pour forcer à identifier les différents cas, ça permet de se diriger vers l'implémentation.Le risque quand on va dans l'autre sens (« bottom up ») c'est de créer des bouts de comportement dont au final on n'aura pas besoin, ça s'oppose à la notion de code minimal.

**Matthieu Clin**

> Je suis tellement perdu que j'arrive pas a m'exprimer...Mon problème : Mon équipe (80% que je ne connaissais pas il y a 2 mois) a un niveau proche de 0 sur les tests, et tout ce que tu veux.
> 
> Moi je veux faire progresser tout le monde sur tous les plans et notamment les tests (la qualité n'est clairement pas au rendez-vous d'un point de vue fonctionnel).Je ne peux pas faire de pair programming avec tout le monde tout le temps.
> 
> Donc je cherche un compromis me permettant de les laisser seul tout en me disant qu'on pourra réutiliser / reprendre si besoin.
> Si la frontière entre le outside et le in était claire ça irait. Mais même là c'est compliqué. (Pour la petite blague mon pattern strategy de l'autre jour, le dev a rendu l'interface générique avec un T et il s'apprêtait a faire un mapper dans le usecase selon le strategy, réduisant a néant le principe ! 😂

**Pat Och**

> Je commence toujours par poser un test sur un seul scenario d'un usecase, en général le scenario qui se produit le plus souvent est le happy path (s'il y en a plusieurs prend le plus courant si tu peux).Ensuite plus tu va ajouter de tests (et donc de scenari), plus ton code repondra au besoin final et deviendra générique.  
> 
> ces tests sont des tests du comportement métier attendu. Ils sont sous la forme AAA (arrange act assert), l'équivalent technique du given when then

**Nicolas Fédou**

> Ton test pose des limites : tu appelles des méthodes/points d'entrées/api et le test exécute ce code de prod de l'entrée aux sorties (retour de la méthode, exception lancée, i/o ou dépendance appelée mais mockée).  
> 
> Ta capacité de refacto est limitée de l'entrée du test a sa sortie ...  
> 
> En rails, je suppose qu'on tape les méthodes métiers jusqu'à une base en mémoire.  
> 
> En Java/Spring ta couche métier peut utiliser des services et ensuite aller en bdd, mais ça implique de lancer Spring ou tu fait du junit en injectant a la main et t'aretant avant la magie (jpa/orm).  
> 
> Dans des legacy, l'injection a la main est un enfer.  
> 
> Bref, ton outsider in, c'est appelle une couche métier et choisi entre un test simple sur ce service métier seul et un test avec plus de données, plus de services injectés et un algo testé plus complet.  
> 
> Enfin, sur ces tests :  
> 1/ ce sont des exemples concrets du code testé, leur nom doit représenter l'intention quelle que soit les valeurs concrètes utilisées  
> 2/ tes données de tests vont être réutilisée par plusieurs tests, les objects mothers de Martin Fowler et le test data management sont tes amis  
> 3/ les framework d'assertions et d'approval testing vont te donner une vraie productivité si tu monte en compétence dessus.Sur ce, bon voyage dans le monde des tests auto !

**Vincent Therry**

> Tu as des réf vers le point 2? Object mothers et test data mgmt ?

**Vincent Therry**

> Suis curieux

**Laurent Bossavit** 

> > Je ne peux pas faire de pair programming avec tout le monde tout le temps.
>
> Alors du mob ! 😂

**Laurent Bossavit**

> Ca a l'énorme avantage que tout le monde apprend en même temps.

**Nicolas Fédou**

> Objectmother, un point de départ classique [https://martinfowler.com/bliki/ObjectMother.html](https://martinfowler.com/bliki/ObjectMother.html)  
> En bref, tu vas avoir beaucoup de tests avec des données communes, ça amène des factories par type/concept/agrégat. Comme des personnas. Dans chaque test, tu aura besoin de customiser la data pour couvrir ton code, ça amène des builders sur ces factories.

**Nicolas Fédou**

> Le test data management est un terme de QA que je connais que de nom. Ça consiste à préparer des jeux de données qu'on injecte dans les persistances avec des problèmes de cohérence avec les clés étrangères de synchronisation quand tu as plusieurs persistances, etc...

**Nicolas Fédou**

> +100 sur le mob.  
> C'est idéal pour mettre au point une nouvelle solution, s'aligner sur des pratiques (suivi de prod, tests auto, gestion de droits,...).

**Matthieu Clin**

> Je fais un point tech' d'une heure par semaine déjà où ça nous arrive de faire des kata en mob'. La on a commencé celui : [https://kata-log.rocks/ohce-kata](https://kata-log.rocks/ohce-kata)Je vais me renseigner sur tout ce que vous m'avez donné, ça me donnera des idées d'approche peut-être !

**Laurent Bossavit**

> [@Matthieu Clin](https://wealcome.slack.com/team/U05CNBQ1VV4) Ce que j'entends par mob c'est travailler ensemble (toute l'équipe) sur le code du produit, celui qui va partir en prod.Pas forcément toute la journée toute la semaine (encore que c'est envisageable aussi, il y a des équipes qui font ça) mais peut-être plus qu'une heure par semaine. Comme ça au lieu de rattraper ou reprendre ce qu'on fait les gens dans l'équipe, tu crées de l'alignement en temps réel sur les techniques et les pratiques de conception. Et comme on verbalise le "pourquoi" de ce qu'on fait, en plus d'avoir le "comment" qui s'inscrit dans le code, tu peux comprendre les raisons qui font que telle et telle personne s'oriente dans telle ou telle direction. Ca permet de réduire les incohérences de raisonnement, pas uniquement réparer a posteriori les incohérences de résultat.Un des points importants pour que cette verbalisation aie lieu c'est le "strong style pairing" c'est à dire la règle qu'une idée ne se retrouve dans le code qu'en passant par la tête d'une autre personne (que celle qui a eu l'idée). Le ou la "driver" ne met rien dans le code si quelqu'un d'autre ne le lui a pas demandé. Ca a l'air (et ça peut être) générateur de frustration et c'est aussi une contrainte très puissante pour révéler les carences d'alignement.


**Laurent Bossavit**

> Typiquement ce que tu disais:  
>
> > le dev a rendu l'interface générique avec un T et il s'apprêtait a faire un mapper dans le usecase selon le strategy, réduisant a néant le principe
>
> …c'est un signe de désalignement entre ta compréhension du conseil que tu essayais de donner, et la façon dont le dév l'a compris.En mob ce désalignement est traité en temps réel; mais quand chacun part de son côté, on le traite par petite touches (genre une heure par semaine ou tous les deux-trois jours au rythme des stories) et du coup ça prend beauuucoup plus longtemps de s'aligner.

**Matthieu Clin**

> Oui c'est clair, faut que je trouve un moyen d'organiser ça. Le challenge c'est que je n'ai pas qu'un seul projet.Un projet  
> 
> - Un front angular
> - Un back spring boot
> 
> Un autre  
> 
> - Trois fronts angular
> - Un back spring boot
> 
> Un dernier  
> 
> - Mobile kotlin
> 
> J'essaie de tourner mais plus en pair programming. Faudrait que je fasse du mob' par techno peut être ?  
> A essayer j'imagine