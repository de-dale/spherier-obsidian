#ContrainteKata [[Contraintes de kata]]

Une des styles du [[Pair-Programming]]]

> _"For an idea to go from your head into the computer_ 
> _it MUST go through someone else's hands"_
> 
> -- [[Llewellyn Falco]]

The person at the keyboard ([[Driver]]) types the code. 
The person who is not at the keyboard ([[Navigator]]) makes all code design decisions.
The [[Navigator]] instructs the [[Driver]] to implement their intent with the highest level of abstraction that the [[Driver]] can fluently work with.
[[Driver]] and [[Navigator]] switch on a fixed boundary (eg: 2-5 minute timer, or completing code to make test pass)

### La navigation _strong style_

Ce type de navigation peut s’appliquer lorsqu’un des deux participants a une idée et cherche à la mettre en place. Dans une implémentation traditionnelle du pair programming, cette personne prendrait le clavier et réaliserait son idée. Dans le [[Strong-Style Pairing|Strong Style]] cette personne va donner le clavier à son partenaire et lui exposer son idée pour que le partenaire l’implémente.

> For an idea to go from your head to the computer it must go through someone else’s hands
> 
> -- Llewellyn Falco

> Pour transmettre une idée de votre esprit à l’ordinateur, il faut la faire transiter par les mains de quelqu’un d’autre

Le binômage en navigation _strong style_ permet de découpler la réflexion de l’écriture du code. Celui qui a l’idée principale, n’a pas le clavier et est donc davantage impliqué dans la réalisation de la tâche, puisqu’il s’agit de son idée que l’on implémente. Celui qui a le clavier, est nécessairement impliqué, car c’est lui qui transmet l’idée à la machine, en recevant les directives du copilote.

Cette manière de faire renforce l’implication des deux participants, notamment grâce à une meilleure synchronisation.

#### Mise en place du _Strong Style_

> Ce que l'on conçoit bien s'énonce clairement et les mots pour le dire arrivent aisément.
> 
> -- Nicolas Boileau

Le copilote a une idée et peut la décrire selon trois niveaux à utiliser dans l’ordre suivant :

- **Intention** : _« Crée une variable que l'on appellera 'décompte' »_
- **Emplacement** : _« À la ligne 27 et demi (une nouvelle ligne entre la #27 & #28) »_
- **Détails** : _« Tape v,a,r espace 'décompte' égal 1 »_

Dans cette approche, la première étape pour le copilote, est d’exprimer son _intention_. Si cela suffit pour que le pilote implémente l’idée, il n’est pas nécessaire d’aller plus loin. Le Pilote est vu dans ce cas comme une interface homme-machine de luxe, beaucoup plus intelligente que les périphériques classiques, avec laquelle le Copilote interagit. Sinon, le Copilote exprime l’_emplacement_ et si cela n’est pas suffisant, il exprime les _détails_. Il est important que le Copilote trouve le bon niveau auquel s’adresser au Pilote. Si les attentes sont asymétriques, il peut en résulter de la frustration dans le binôme.

Par exemple :

- Si le copilote ne donne que les _détails_, alors que l'_intention_ suffit au pilote, cela va agacer le pilote.
- Si le copilote ne donne que l'_intention_, alors que le pilote a besoin de l'_emplacement_ ou les _détails_, le pilote se retrouve perdu.

Dans tous ces cas le binôme n'avance pas.

# Ressources

- Llewellyn’s strong-style pairing
  http://llewellynfalco.blogspot.com/2014/06/llewellyns-strong-style-pairing.html 