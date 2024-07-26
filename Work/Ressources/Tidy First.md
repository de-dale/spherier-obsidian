---
ressource:
  - 📖 Livre
author: "[[Kent Beck]]"
relates:
  - "[[Tidy Code]]"
  - "[[Couplage]]"
  - "[[Cohésion]]"
---
*Tidy Code?* est un livre très court (97 pages),
- Facile à lire : le style de [[Kent Beck]] est léger et amusant
- Profond : il y a du contenu de qualité et des choses qui sont mises ensemble qui font très sens, et des traits de philosophie qui font réfléchir
- Pragmatique : il repose les bases, de manière très claire et posée

Ne le lisez pas si vous n'êtes pas prêt.e à faire face à ces déconvenues :  
- [[Tidying]] == refactoring (à une nuance prêt) => Il y a tout une partie du livre, ou on est susceptible de ne rien apprendre
- En suivant les travaux de Kent Beck, j'ai déjà été sensibilisé à tout ce qu'il raconte, donc il n'y a pas eu d'effet Wouah

Le livre s'adresse à des programmers qui ont déjà quelques années, d'expériences, mais je trouve qu'il y a plusieurs niveaux de lecture. Un junior peut y apprendre des choses (les différents Tidyings, quelques pratiques de travail en équipe et une base de théorie du Software Design fondamentale), mais certaines parties demandent d'avoir davantage de recul (et je sais que je n'ai pas tout compris autant que je le voudrais).

Le sommaire du livre est disponible ici : https://www.oreilly.com/library/view/tidy-first/9781098151232/.

### Préface et Introduction

La préface de Larry Constantine, co-auteur de *Structured Design* est assez intéressante, on y retrouve une définition de couplage et cohésion très légère, mais très puissante.

> It is easier to understand the immediate piece of code if it all hangs together, if it make sense as a whole, if it forms what cognitive psychologists call a Gestalt.
> That's [[Cohésion|cohesion]].
> 
> -- Larry Constantine, Tidy First?, Preface, p.xii

🧠 Donner du sens au code qu'on a sous les yeux, c'est ce qu'on appelle "[[Cohésion]]".

> It is is also easier to understand it in terms of its relationships with other piece of code if these relationships are few and relatively weak or highly constrained.
> That's [[Couplage|coupling]].
> 
> -- Larry Constantine, Tidy First?, Preface, p.xii

🧠 La qualification des interactions entre le code qu'on a sous le yeux et les autres parties du code, c'est ce qu'on appelle le "[[Couplage]]"

> Couplage and Cohesion are really all about how your brain deals with complicated systems.
> 
> -- Larry Constantine, Tidy First?, Preface, p.xii

🧠 Couplage et cohésion sont la mesure de la complexité d'un système pour un humain. C'est un indicateur permettant à votre cerveau de composer avec les systèmes compliqués.

> A tidying is like a little baby miniature refactoring.
> 
> -- Introduction, p.xv

🧠 Première définition de "tidying" dans le livre., qui est vu come un tout petit refactoring. Ca répond à des questions que je me posais déjà, même si, à ce moment j'ai du mal à percevoir la différence que Kent Beck fait entre les deux

> [[Kent Beck - Software design is an exercice in human relationship]]
> 
> -- Introduction, p.xv

🧠 Le plus gros mensonge de notre métier de développeur/développeuse, c'est que l'on travaille uniquement avec un ordinateur.
Plus tard dans le livre, Ken Beck explique de *Tidy First?* est le premier livre d'une série dédiée à ce sujet, et que celui-ci traite de la relation entre soi et soi-même face au code.

### Première partie : Tidying

Pour ceux qui pratiquent souvent le refactoring, ce chapitre ne leur apprendra pas grand chose
Kent Beck présente un catalogue de tidyings (des petits refactorings que "personne ne peut haïr").
Ce que j'ai trouvé intéressant sur ce chapitre, c'est la philosophie qui est mise derrière le terme "Tidying" ; il s'agit de faire les toutes petites choses, avec très peu d'impact sur le comportement du code, mais qui apportent beaucoup en terme de compréhension du code pour les lecteurs (vous, et les lecteurs à venir).

Cette partie est très intéressante pour les juniors

> Tidying are a subset of refactorings.
> Tidyings are cute, fuzzy little refactorings that nobody could possible hate on.
> 
> -- Tidyings, p.1

La liste des Tidyings (cf. le sommaire du livre)
1. Guard Clauses
2. Dead Code
3. Normalize Symmetries
4. New Interface, Old Implementation
5. Reading Order
6. Cohesion Order
7. Move Declaration and Initialization Together
8. Explaining Variables
9. Explaining Constants
10. Explicit Parameters
11. Chunk Statements
12. Extract Helper
13. One Pile
14. Explaining Comments
15. Delete Redundant Comments

Je n'ai rien de particulier à dire plusieurs Tidyings, et je vais plutôt détailler les parties qui m'ont marquées.
#### New Interface, Old Implementation

> Implements the interface you wish you could call and call it.
> Implements the new interface by simply calling the old one.
> 
> -- New Interface, Old Implementation, p.9

🧠 Cette pratique fait écho à ma pratique du TDD, où on commence par appeler des éléments de code qui n'existent pas et on utilise les outils de l'IDE pour les créer.
#### Cohesion Order

> If two routines are coupled, put them next to each other.
> If two files are coupled, put them in the same directory.
> \[...]
> If you know how \[to decouple], go for it. Assuming `cost(decoupling) + cost(change) < cost(coupling) + cost(change)`
> [...]
> Tidying can increase cohesion enough to make behaviour change easiers.
> 
> -- Cohesion Order, p.13

🧠 Je trouve ce tidying très pragmatique. Il fait beaucoup de sens pour moi : augmenter la cohésion pour mieux comprendre, et si c'est possible, découpler. Découpler n'étant pas une fin en soi.

#### Explicit Parameters

> It's common to see block of parameters passed as a map.
> 
> -- Explicit Parameters, p.21

🧠 Ce tidying m'a marqué, car à la première lecture, je comprenais "Pratiquer l'inverse du refactoring 'Introduce parameter object'". Ce n'est pas le cas. 
- "Explicit Parameters" proposer de redonner du sens aux paramètres au lieu d'avoir un contexte très peu cohésif, 
- "Introduce parameter object" est un refactoring un peu plus conséquent, qui ajoute de la cohesion entre les paramètres (ce qui n'est pas toujours facile à faire et peu avoir d'autres impacts)

#### Chunk Statements

> Put a blank line between \[two parts of a big chunk of code]
> 
> -- Chunk Statements, p.23

🧠 "Ajouter un saut de lignes entre deux paragraphes". Le tidying le plus simple, selon Kent Beck. Tellement simple, que je le faisais déjà, mais sans l'avoir conscientisé.
#### One Pile

> The biggest cost of code is the cost of reading and understanding it.
> 
> -- One Pile, p.27

> To regain clarity, the code must first be mooshed together so new, easier-to-understand parts can be extracted.
> 
> -- One Pile, p.27

🧠 Inliner le code pour mieux le comprendre, car parfois, en voulant bien faire, on l'éclate de trop. Si c'est trop éclaté, cela demande de mettre beaucoup de chose dans notre mémoire de travail.

Ce qui est intéressant dans cette partie, c'est la réflexion autour du concept de "tidying" : 

> Tidy first has a bias toward lots of little piece \[...] to increase cohesion as a path to reducing coupling, and to reduce the amount of details needed to be held in your head at any one time.

🧠 Quel que soit le tidying, l'objectif reste le même : nous simplifier la compréhension du code.
Souvent, cela va passer par rajouter de la cohésion : réduire la quantité de détails à mettre dans notre tête nous permettant de comprendre le code. Ou plutôt : comprendre le code avec la plus petite charge mentale possible.
Ce tidying nous suggère de faire l'inverse, toujours dans un objectif de comprendre le coode.
#### Delete Redundant Comments

> The purpose of code is to explain to other programmers what you want the computer to do.
> 
> -- Delete Redundant Comments, p.31

🧠 Je ne m'attarde pas sur le tidying , mais, une fois de plus, sur l'objectif du code, et des tidyings : faciliter la compréhension du code (ce qui va avec ma définition de Clean Code "_Le Clean Code est du code pensé pour faciliter son apprentissage par les développeurs et développeuses_")
### Seconde partie : Managing

Juste après la lecture du livre, je me suis rendu compte que cette partie m'avait peu marqué.
Elle parle de l'organisation du travail, seul et en équipe, autour du concept de pratiquer des "Tidyings".
A la relecture, j'avais quand même noté plusieurs choses.

> Tidyings is software design addressing you, your relationship to your code, and ultimately your relationship with yourself.
> [...]
> Tidying is geek self-care.
> 
> -- Managing, p.33

🧠 Cette introduction très philosophique est hyper pertinente dans la mouvance du Software Craftsmanship : ce qui fait la différence, c'est notre attitude face au code, et la relation qu'on entretien avec lui. C'est, par conséquence, le respect que l'on porte à notre propre activité, et donc, à nous-même.

> I wanted to acknowledge that just because you can tidy doesn't mean you should tidy.
> 
> -- Managing, p.33

🧠 Je trouve cette phrase très intéressante : ce n'est pas parce qu'on voit des choses à faire, qu'on peut le faire tout de suite. La tension entre "Tidying", pour soi-même, et les contrainte de production est amenée dès ce chapitre, mais détaillée par la suite.
Ce que je trouve intéressant, c'est de confronter le fait de s'occuper de soi (le truc qui manque pour moi dans le manifeste agile et ses déclinaisons) et le fait de produire quelque chose qui a de la valeur pour son client et son entreprise.

Par la suite,  Kent Beck détaille des pratiques de s'organiser autour du Tidying.
Il part du principe que l'on se trouve dans une entreprise où l'on pratique de la Code Review en Pull-Request (PR).

16. Separate Tidying
17. Chaining
18. Batch Sizes
19. Rhythm
20. Getting Untangled
21. First, After, Later, Never

Je n'ai pas grand chose à dire sur le Separate Tidying, car cela fait sens pour moi.
Je n'ai pas grand chose à dire sur le Chaining ; Kent Beck présente des synergies entres les tidyings présentés dans le chapitre d'avant.
#### Batch Sizes
(j'ai une notre de lecture)

Dans cette section, on se pose la question "combien de tidings je peux grouper ensemble avant de les soumettre en PR"

> Tidying is not looking toward a far-future. 
> Tidying meets an immediate need
> 
> -- Batch Sizes, p.43

🧠 Pratiquer le Tidying répond à un besoin immédiat, et pas à un besoin de changer la structure du code en profondeur (pratiquer un refactoring). Le nombre de tidings n'est donc, pas nécessairement élevé.
Dans l'idéal, on aurait 1 Tidying = 1 Commit = 1 PR. Mais chaque PR un coût pour l'équipe.

Solution : 

> If we want to reduce the cost of tidying, thus increasing tidying and reducing the cost of making behavior changes, then we can reduce the cost of review.
> 
>  -- Batch Sizes, p.45

> In teams with trust and strong culture, tidyings don't require review.
> 
> -- Batch Sizes, p.46

🧠 Ici, je comprends qu'on se dirige vers du Trunk-based development, éventuellement en pratiquant le "Ship Show Ask".

#### Getting Untangled

"Comment je fais si j'ai oublié de séparer mes Tidyings de mes évolutions ?"

> The shortest path to instructing a computer is not an interesting goal.
> -- Getting Untangled, p.49

🧠 Ici, on a plusieurs options pour se débrouiller du problème d'avoir tout mélanger. Ken Beck nous encourage à reverter nos travaux et à recommencer afin de :
- apprendre de nos erreurs et bien séparer nos tidyings de nos évolutions
- s'adresser correctement à nos relecteurs de PR pour leur faciliter leur travail
#### First, After, Later, Never

Cette section est assez chouette car elle donne des pistes de réflexion sur quand pratiquer le tidying.

> Tidying is a great way to become aware of the detailed consequences of your design.
> 
> -- Later, p.52

> Sometimes I just don't have energy to tackle a new feature, but I want to work.
> Picking an item off the Fun List and tidying it brings me joy. 
> 
> -- Later, p.52

🧠 Tidying "longtemps" après avoir développé une fonctionnalité est possible, mais il faut maintenir nos idées et nos observation dans une "Fun List". Utiliser cette liste nous permet d'avoir de la matière à travailler et à nous faire plaisir.
De plus, pratiquer le tidying "plus tard", nous permet d'apprendre de notre code, et d'avoir des retours sur où et comment notre design est pourri.

> Do you tidy after ?
> It depends.
> 
> -- After, p.53

🧠 Quelques pistes de réflexion pour déterminer si on peut se permettre de tidying juste après avoir fini notre fonctionnalité. Pour paraphraser, on a le feu vert si :
- le code qu'on vient de modifier va être de nouveau modifié, très bientôt.
- c'est moins cher de le faire tout de suite
- le coût (en temps) du tidying est du même ordre de grandeur du coût de la feature (1h pour 1h, mais pas 1h pour 1 semaine de tidy)

> Tidy first ?
> 
> -- First, p.53

🧠 La meilleur blague du livre. J'ai ri. Mais je ne spoile pas.

Bon, je spoile un minimum quand même :
- si tidying le code ne rend pas l'évolution plus facile => évitez de tidy first
- si tidying aide à la compréhension du code => tidy first

### Troisième partie : Theory

J'étais très emballé à l'idée de lire cette partie. J'ai quand même du m'accrocher pour bien la lire.
L'idée de Kent Beck pour cette partie, est, non pas de répondre aux questions que l'on se pose, mais de poser des éléments permettant d'y répondre nous-même, dans les différents contextes auxquels nous sommes confrontés.

Les questions en bref :
- c'est quoi le "Software Design" ?
- En quoi le Software Design pilote les coûts de développement et du run ? et vice-versa
- Quels sont les compromis que l'on peut faire ?
- Que peut on utiliser (principles, critères économiques, critères humains) pour savoir quand et comment modifier la structure du logiciel ?

> Software design is an exercice in humain relationships.
> \[...] do you value yourself enough to make your work easier before you do the work ?
> 
> -- Theory, p.56

🧠 Ce livre sur le tidying, est une invitation à prendre soin de soi. Les éléments de théorique qui arrivent viennent apporter des arguments permettant de savoir à quoi on renonce quand on choisi entre "prendre soin de soi" et "livrer de la fonctionnalité"

Par la suite, je en vais pas rentrer dans la théorie en tant que telle, sinon je risque de paraphraser le livre, mais plutôt sur les réflexions que ça m'apporte
#### Beneficially Relating Elements

Cette section définit ce qu'est le "Structure d'un système" afin de la confronter au "Behavior of the system" (défini dans la section d'après, mais je préfère le mettre ici), qui sont deux moyens de qualifier le système.

> Structure of the system : 
> - The elements hierarchy
> - the relationships between elements
> - the benefits created by those relationships
>   
> -- Beneficially Relating Elements, p.59

> Behavior :
> - input/output pairs
> - invariants
>
> -- Structure and Behavior, p.61
#### Structure and Behavior

> Software creates values in two ways :
> - what is does today
> - the possibility of the things we can make it do tomorrow
>   
> -- Structure and Behavior, p.61

> In a word , optionality.
> \[...]
> Options are the economic magic of software
>
> -- Structure and Behavior, p.62

🧠 Issu du vocabulaire de la finance, l'Option est le fait de s'acheter la capacité de s'acheter quelque chose, dans le temps. Dans le cas du Software, c'est la capacité à s'acheter la possibilité d'une évolution/ d'une fonctionnalité/d'un changement
Et ces Options sont quelque chose que l'on devrait être en mesure de valoriser.
Plus le contexte est volatile, plus l'Option a de la valeur.
A contrario, si on perd de la connaissance (avec le départ de personnes), si on perd notre capacité à récolter du feedback, ou si on augmente le coût du changement proposé par l'Option , alors, l'Option perd de la valeur.

> \[Understand] that structure change and behavior change are both way to create value, but they are fundamentally different.
> In a word, reversibility.
> 
> -- Structure and Behavior, p.63

🧠 Il s'agit du dernier paragraphe de la section. La question de la reversibilité fait écho à quelque chose que je connais sous le nom de "Breaking Change".

#### Economics: Time Value and Optionality

L'idée de cette section est de confronter deux visions, issues du monde de la finance.
- gagner de l'argent tout de suite est sûr, mais peut limiter les options futures
- dans une situation chaotique, il vaut mieux s'acheter des options, que de gagner de l'argent immédiatement

> Software design has to reconcile the imperatives of "earn sooner/spend later" and "create options, not things"
> 
> -- Economics: Time Value and Optionality, p.66

🧠 Il existe une tension entre "acheter une fonctionnalité maintenant" et "s'abonner à l'option nous permettant de l'acheter dans le futur". Composer avec cette tension, est le nerf du Software Design.

#### A Dollar Today > A Dollar Tomorrow

Petit laïus sur la monnaie : la monnaie possède une valeur qui dépend de deux facteur
1. Quand est-ce que je peux en disposer ?
2. Quelle certitude ais je de pouvoir en disposer ?

Si on considère que la valeur de la monnaie, ne dépend que du temps, alors, quand on fait le parallèle Monnaie//Software, cette considération encourage à pratiquer le "Tidy After".
Sauf dans le cas où `cost(tidying) + cost(change) < cost(change)`, où il est évident que le seul facteur "coût" encourage à pratiquer le Tidy First.

#### Options

Je trouve cette section très profonde, mais très floue. Je ne suis pas sûr de l'avoir bien comprise, mais ce que j'en retire me parait immensément valable.

Pour le Software, la valeur ne dépend pas uniquement du temps, elle dépend également des options que propose le software.

Une question à se poser : 
> What behavior can I implement next ?
>
> -- Options, p.70

Petite paraphrase : 
Cette question a de la valeur en tant que telle.
Et, plus il y a de comportements disponibles à l'implémentation, plus elle a de valeurs
Et, plus les comportements disponibles ont de la valeur, plus la question a de la valeur

> I don't have to care which item will be most valuable, as long as I keep open the option of implementing it.
>
> -- Options, p.70

🧠 "*En tant que techno, on se moque de savoir quel comportement plus de valeur qu'un autre, tant qu'on est en mesure d'implémenter n'importe lequel des deux*" ; et je trouve ça hyper important, et hyper pertinent. Ca permet de se positionner sur des choix de fonctionnalités, ou d'argumenter face à un PO ou un chef de projet.
Quand les personnes du métier se seront décidées, on doit être en mesure d'implémenter ce qui a le plus de valeur au moment où on nous le demande.
Donc : plus il y a de l'incertitude sur les projets, plus la capacité à donner des options a de la valeur.

> Software design is preparation for change; change of behavior.
> 
> -- Options, p.71

🧠 Les questions que cela soulève sont multiples :
- Est-ce qu'on achète la fonctionnalité aujourd'hui ?
- Demain ?
- Combien ça coûte d'avoir la garantie de pouvoir le faire demain ? de pouvoir le faire deans une semaine ?

#### Reversible Structure Changes

> Code review process don't distinguish between reversible and irreversible changes
>
> -- Reversible Structure Changes, p.76

🧠 Les décision réversibles et irréversibles n'ont pas la même portée. Plus il est facile de changer de décision, moins il y a de risque à prendre cette décision, et moins cela coûte en terme de vérification, stress, contrôles, etc.
Les petits changements dans la structure du code (tidyings) sont des décisions réversibles, qui permettent de rendre d'autres décisions réversibles. Et en ça, le tidying apporte beaucoup de valeur. En cascade.

#### Coupling

> Coupling drives the cost of software.
> Coupling is so fundamental.
> 
> `coupled(E1, E1, Δ) ≡ ΔE1 ⟹ ΔE2`

🧠 Le couplage est une notion fondamentale dans le logiciel. On parle de couplage entre deux éléments (E1, E2), par rapport à un changement (Δ).
Le couplage possède, deux propriétés qui font de lui autre chose qu'une simple relation :
- 1-N : Un élément peut être couplé avec n'importe quel nombre d'autres éléments, pour un changement donné
- Cascade : Quand un changement est passé d'un élément à un autre, il peut déclencher une autre vague de changements, qui peut elle même déclencher une autre vague de changements

Le couplage est appelé "connascence" dans d'autres contextes. J'avais déjà vu passer le mot, mais je n'avais pas compris le rapprochement.
#### Constantine équivalence

Larry Constantine est une des co-auteurs de *Structured Design* qui a inspiré Kent Beck pour son livre et pour la définition du Couplage.

> The full Constantine Equivalence :
> `cost(software) ~= cost(change) ~= cost(big changes) ~= coupling`
> 
> -- Constantine équivalence, p.83

🧠 L'idée derrière cette équivalence, est de dire que le coût du logiciel est concentré dans le coût à investir pour le modifier.
Au vu des ordres de grandeur, le coût du changement est masqué derrière le coût des gros changements.
Comment les changements se propagent dans le logiciel ? Par le biais du Couplage.
Donc: le coût du logiciel est égal au couplage.

> To reduce the cost of software, we must reduce coupling.
>
> -- Constantine équivalence, p.83

#### Cohesion

> Cohesion :
> - Coupled elements should be subelements of the same containing element.
> - Elements that are not coupled should go elsewhere
> 
> -- Cohesion, P.91

> All the benefits that come from cohesion:
> - easier analysis
> - easier change
> - resistance to accidental behavior change
> 
> -- Cohesion, P.91

🧠 La Cohésion est du couplage, mais maîtrisé et qui apporte de la cohérence et de la clarté quand au code qu'on a sous les yeux.
On pratique régulièrement de l'extraction de cohésion (Extract Method, Extract helper).
### Conclusion

> *Tidy First?* question is each time affected by the same forces
> - Cost
> - Revenue
> - Coupling
> - Cohesion
> 
>Most important, though, is you. Will tidying bring peace, satisfaction and joy to your programming ?
>
>-- Conclusion, p.91

🧠 Je trouve cette conclusion, comme le reste du livre, très inspirante. Kent Beck se joue de nous en apportant des éléments rationnels nous permettant de savoir si on veut faire du tidying ou non, mais en confrontant ces arguments avec notre ressenti humain.
Son conseil, est de pratiquer un tidying après un autre, et de s'avoir s'arrêter.

Ce livre se termine en rappelant, qu'il s'agit du premier d'une série sur le Software Design, et avec du teasing sur les prochains livres.

*Tidy First?*, est une question qui s'adresse à soi-même, sur une temporalité en minutes, et qui nous permet de confronter le Couplage et la Cohésion du système pour le rendre plus accessible pour les développeurs et développeuses du future (comme nous-même.)
## Autres avis

> Pour moi il y a une référence implicite à Kondo « La magie du rangement » (en VO _The Life Changing Magic of Tidying Up_)
> Tidy ça a des connotations d'être rangé mais aussi bien rangé, des choses bien à leurs places, propres et nettes.
> On peut aussi penser au 5S du Lean
> On peut aussi penser à soigné.
> Une préoccupation de soin du code et (je crois pour Kent) qui va avec un soin de soi.
> 
> -- Laurent BOSSAVIT