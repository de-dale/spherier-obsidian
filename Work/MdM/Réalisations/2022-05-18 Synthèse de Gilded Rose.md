---
relates:
---

Hier, lors du dojo, on s'est fait une synthèse du Gilded rose (La Rose Dorée), l'exercice de refactor qu'on avait travaillé les deux fois précédentes.

# **Couverture de code**

On a rappelé qu'avant de se lancer dans l'ajout d'une fonctionnalité, ou dans le refacto d'une codebase non maitrisée, il fallait s'assurer du comportement initial du code.

Les fois précédentes, on avait tenté :

1. de rétro-tester les règles métiers
2. de rétro tester avec la technique du **[[Golden Master]]** (i.e la source de référence)

Cette fois, on a refait un Golden Master, en utilisant la libraire _**Approvals**_

[https://github.com/approvals/ApprovalTests.Java](https://github.com/approvals/ApprovalTests.Java "https://github.com/approvals/approvaltests.java")

Cette librairie génère propose des Asserts (appelé _Approvals_) à utiliser dans des tets unitaires, et permettant  de générer un fichier "_ClasseDeTest.nom_de_la_methode_de_test.recieved.txt_". Ce fichier peut servir de référence s'il est "approuvé" par un humain (fichier renommé *recieved* => *approved*). Ensuite, tant que le code ne modifie pas le résultat attendu par la source, le test passe.

Utiliser la technique du [[Golden Master]] nous a permis de converger rapidement vers une couverture à 100% de notre code.

# **Limites de la couverture de code**

Ensuite, on s'est rendu compte que, en changeant des choses dans notre code de "prod", le test continuait de passer.

Malgré une couverture de code à 100%, la couverture fonctionnelle **n'était pas complète** !

On a alors regardé ce qu'est le **[[Mutation Testing]]** : une technique permettant de créer des "mutants" de notre code de prod (par de la modification du code de prod) et de confronter ces "mutants" aux tests. Si une mutation entraine une erreur dans un test, c'est chouette : cela signifie que notre test couvre bien une fonctionnalité (ou se prémunit d'un bug).

En revanche si un mutant "survit", c'est à dire que la mutation ne cause aucune erreur dans les tests, cela signifie que nos tests ne sont pas suffisants pour couvrir les fonctionnalités de notre code de prod.

C'est une manière de tester nos tests unitaires.

On a utilisé _**Pittest**_ pour mettre en place le mutation testing dans le projet (et on a bien pensé à le configurer pour JUnit5, ce qui demande une dépendance spécifique)

[https://pitest.org](https://pitest.org "https://pitest.org/")

Puis, on s'est assuré que notre code de test était en mesure de tuer tous les mutants.

Petit rappel  :

> Il n'y a aucun indicateur direct de qualité de code. Le code coverage, le mutation testing & co, ne sont que des indicateurs de non-qualité.  
>   
> e.g. à 10 % de coverage, tu sais que tu testes pas assez mais à 100% de coverage tu ne sais pas si tu testes vraiment.👇🧵  
> [https://twitter.com/JulienTopcu/status/1466405920380968963](https://twitter.com/JulienTopcu/status/1466405920380968963 "https://twitter.com/julientopcu/status/1466405920380968963")

# **Feature First !**

Avec une bonne confiance quand à notre couverture de code, nous avons ajouté la fonctionnalité demandée, comme des gros sales.

On a fait de la **[[Shotgun Surgery]] (qui est un anti-pattern)**, au moins pour montrer qu'on était capable de rapidement livrer la feature, sans avoir besoin de rentrer dans du code qui nous révulse.

# **Appréhender** **du Code Legacy**

L'objectif de l'exercice étant de refactorer, on s'est brièvement posé la question de "comment on aborde ce code".

Deux conseils :

1. Commencer par rétro-tester (fonctionnellement, car le Golden Master couvre techniquement tout el code) la branche de code la plus "haute", c'est à dire avec le moins de conditions pour l'atteindre
2. Commencer par refactorer la branche de code la plus "profonde", c'est-à-dire celle avec le plus de conditions à respecter pour l'atteindre.

On ne s'est pas attardé là-dessus.

# **Utiliser la couverture de code comme outil de développement**


On a fini l'exercice en appliquant la méthode de refactoring "**[[Lift-up Conditional]]**".

L'idée de cette méthode :

- trouver des conditions qui correspondent à des règles métier
- dupliquer le code dans le _if_ ET le _else_ de la règle
- supprimer le code mort dans le _if_ et le _else_ 
    - Le code mort est mis en évidence par la couverture de code (le code non couvert par des tests, qui couvraient initialement 100% du code, est du code mort)
    - On s'aide au maximum de l'IDE, qui nous trouve du code mort automatiquement, et nous supprime le code par dizaines de lignes

Il y a une démo ici : [http://gregorriegler.com/2019/12/08/lift-up-conditional.html](http://gregorriegler.com/2019/12/08/lift-up-conditional.html "http://gregorriegler.com/2019/12/08/lift-up-conditional.html")

Vous pourrez trouver tout le code sur GitLab :

- Le code d'hier : [https://git.maisonsdumonde.net/fhiegel/coding-dojo/-/tree/gilded-rose](https://git.maisonsdumonde.net/fhiegel/coding-dojo/-/tree/gilded-rose "https://git.maisonsdumonde.net/fhiegel/coding-dojo/-/tree/gilded-rose")
- Le code pour tous ceux qui ont travaillé avec Adeline les fois précédentes : [https://git.maisonsdumonde.net/fhiegel/coding-dojo/-/tree/gilded-rose.aavril](https://git.maisonsdumonde.net/fhiegel/coding-dojo/-/tree/gilded-rose.aavril "https://git.maisonsdumonde.net/fhiegel/coding-dojo/-/tree/gilded-rose.aavril")
- Le code pour tous ceux qui ont travaillé avec Romain les fois précédentes ; [https://git.maisonsdumonde.net/rcochennec/gilded-rose](https://git.maisonsdumonde.net/rcochennec/gilded-rose "https://git.maisonsdumonde.net/rcochennec/gilded-rose") (et là : [https://git.maisonsdumonde.net/fhiegel/coding-dojo/-/tree/gilded-rose.romain](https://git.maisonsdumonde.net/fhiegel/coding-dojo/-/tree/gilded-rose.romain "https://git.maisonsdumonde.net/fhiegel/coding-dojo/-/tree/gilded-rose.romain"))

Voilà