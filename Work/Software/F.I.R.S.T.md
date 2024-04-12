# F.I.R.S.T - Pratiques de test unitaires

9 F pour Fast, soit rapide.
9 I pour Isolated/Independent, soit isolé, indépendant.
9 R pour Repeatable, soit répétable, reproductible.
9 S pour Self-verifying, soit auto-validant.
9 T pour Timely/Thorough, soit opportun, précis.


# Extrait de Software Craft
8. 1 LES CARACTÉRISTIQUES DES TESTS :
LES TESTS UNITAIRES F. I . R . S . T .
Quand on parle des tests, notamment pour les tests réalisés en approche TDD,
l’expression suivante revient souvent :
« Tests are FIRST. »
Ceci se traduit littéralement par : « Les tests viennent en premier. ». En effet,
l’idée majeure derrière l’approche TDD est de commencer par les tests. Mais cet
aphorisme porte une autre signification, moins connue ; « FIRST » est également un
acronyme décrivant les propriétés que tout bon test doit comporter :

9 F pour Fast, soit rapide.
9 I pour Isolated/Independent, soit isolé, indépendant.
9 R pour Repeatable, soit répétable, reproductible.
9 S pour Self-verifying, soit auto-validant.
9 T pour Timely/Thorough, soit opportun, précis.

8.1

140 Chapitre 8 Principes et outils pour tester efficacement

8.1.1 Le test doit être rapide

Afin de réduire la durée du feedback et d’inciter à lancer les tests plus fréquem-
ment, l’exécution d’un test ne devrait jamais dépasser les millisecondes pour un

test unitaire. Si la durée d’un test est trop élevée, cela nous dissuadera de le lancer
souvent. Et, par voie de conséquence, la détection des régressions sera réduite et
trop tardive, rendant le code de plus en plus difficile à maintenir au fil du temps.
On pourrait penser que quelques millisecondes de trop, pour un test donné, ne sont
pas réellement un problème. Cependant, si on raisonne à l’échelle du produit, autant
de retard multiplié par le nombre de tests pèsera à la fois sur la fréquence d’exécution
de l’intégralité des tests et sur la volonté d’enrichir la suite avec de nouveaux tests (par
peur d’alourdir une suite déjà lente). Il est donc important de s’assurer que chaque test
est suffisamment véloce, afin de ne pas pénaliser l’ensemble de la suite de tests.
8.1.2 Le test doit être isolé et indépendant
Un test, pris individuellement, doit être suffisamment autonome pour ne pas
dépendre de l’exécution d’autres tests. Qu’il soit lancé seul, ou au sein d’une suite de
tests, son résultat doit être systématiquement le même (à base de code identique).
On doit pouvoir lancer les tests individuellement, en parallèle et dans n’importe quel
ordre d’exécution, et garantir que cela n’a aucun impact sur le résultat. Aucun test ne
doit dépendre de l’exécution d’autres tests, qu’il s’agisse d’initialiser un contexte ou
de préparer des données.
Il suffit d’avoir vécu de fastidieuses et douloureuses investigations en quête de la

cause d’échec de tests interdépendants, ou d’avoir fait face au cauchemar de main-
tenir des tests enchevêtrés sans rien casser, pour être intimement convaincu des

bienfaits des tests indépendants.
8.1.3 Le test doit être répétable

On doit pouvoir répéter l’exécution d’un test à l’infini, sur différents environne-
ments (en local, en environnement de recette, avec un accès au réseau ou non).

Quelle que soit l’exécution, et quel que soit l’environnement, le résultat doit rester

le même (en succès ou en échec). Un test est non répétable, ou non reproduc-
tible, lorsque son résultat change en fonction des environnements ou des conditions

de l’environnement (par exemple, perte de la connexion réseau). Si un test n’est
pas isolé ou indépendant, cela entraîne également qu’il n’est pas répétable. Dans
d’autres cas plus insidieux, certains tests reposent sur une configuration particulière
de l’environnement (telle qu’une variable d’environnement) : c’est une faille majeure
sur la répétabilité des tests, d’autant plus qu’elle est difficile à qualifier.
D’une manière générale, pour qu’un test soit répétable, le code doit contenir tout
ce qui est nécessaire. Il doit s’exécuter comme un système fermé, sans accès à des
ressources extérieures (telles qu’une base de données, un répertoire partagé ou un

8.1 Les caractéristiques des tests : les tests unitaires F.I.R.S.T. 141

microservice). Il ne doit donc pas se baser sur des données aléatoires qui changent
avec le temps comme des identifiants ou la date du jour. Lorsqu’une application
repose sur ce type de dépendances, on peut introduire les bonnes abstractions
pour pouvoir ensuite les substituer (voir la section 8.2 « Doublures de tests (tests
doubles) » ci-dessous).
8.1.4 Le test doit être auto-validant
Un test ne se limite pas à exécuter du code de production, il doit produire également
un résultat objectivable : il est soit en succès, soit en échec (et les causes d’échec
peuvent être diverses). Le résultat doit être outillé et sauter aux yeux, sans requérir une
intervention humaine pour comprendre ou interpréter le statut du test. Si par exemple
on doit vérifier et analyser un fichier de log pour savoir si le test a réussi ou a échoué,
c’est que le test n’est pas auto-validant. Les tests qui ne sont pas auto-validés obligent

une vérification manuelle et fastidieuse qui est non seulement source d’erreurs d’inter-
prétation mais pose également le risque que le test finisse par être laissé de côté.

L’utilisation d’assertions pertinentes contribue à rendre les tests auto-validants.
8.1.5 Le test doit être opportun et précis
Le caractère opportun d’un test se réfère au moment idéal pour l’écrire. Si on suit
la méthode TDD, le test s’écrit naturellement avant l’écriture du code de production.
Lorsqu’on est confronté à un bug, essayer de le reproduire sous la forme d’un test
permet de gagner beaucoup de temps : le test échoue, puis on corrige le code de

production jusqu’à ce que le test réussisse. Inversement, attendre que la fonction-
nalité soit complétement réalisée pour écrire les tests provoque la plupart du temps

amertume et regrets face à un code difficile à tester et à un design déplorable1
.
Le test se doit tout autant d’être précis, en ne couvrant qu’un seul cas d’utilisation.
Même si une fonctionnalité peut mener à une ribambelle de scénarios (avec un cas
nominal, des cas aux limites et des cas d’erreurs par exemple), il est préférable de les
séparer en se limitant à un test par scénario. Le bénéfice principal est de permettre
une compréhension plus précise et rapide lors de l’échec d’un test, tout en facilitant
la maintenance des tests (il est plus pratique de maintenir plusieurs tests couvrant
chacun un cas qu’un seul gros test couvrant tous les cas).
8.1.6 Laissez-vous guider par FIRST
Les caractéristiques FIRST sont essentielles pour définir des tests unitaires
robustes maintenables et rapides. Le fait de les ignorer introduit un risque à moyen
et long terme sur la capacité de l’équipe à maintenir les tests, ou, plus grave, à les
lancer régulièrement.


Fast
Isolated
Repeatable
Self-Exploainatory
Timely

[[Test-Driven Development]]

[[Test unitaire]]
#Skill