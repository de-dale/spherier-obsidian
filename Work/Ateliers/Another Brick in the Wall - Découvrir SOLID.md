🎯 **Objectif** : #🔭Découverte 
	Connaissez vous les principes [[SOLID]] ? Il s'agit de 5 principes de développement logiciel, réputé garantir la qualité des logiciels que nous développons.
	Au travers de 5 exercices, découvrons ces 5 principes.
🕓 **Durée** : #1h🕓 x5
👥 **Participants** : #👥2-n

Le but de ce Kata, est de faire découvrir une partie de [[SOLID]] : 
- [[Single Responsibility Principle]] ([[Single Responsibility Principle|SRP]]), 
- [[Open-Closed Principle]] ([[Open-Closed Principle|OCP]])
- [[Liskov substitution Principle]] ([[Liskov substitution Principle|LSP]]).  

# Introduction du Kata  
  
Présenter le Kata - [[Reverse Polish Notation]] :  
http://codingdojo.org/kata/RPN/  
  
Poser quelques contraintes :  
- On ne prend en entrée que des entiers positifs  
- On ne retourne que des nombres positifs  

Dans cet exercice, on va mettre de coté :  
- La soustraction ; trop proche de l’addition et qui engendre des questions sur les cas limites trop tôt sur la codebase  
- La composition des opérations, qui va trop loin par rapport au but de l’exercice : On s'arrête à un seul opérateur

Ne pas mentionner INTEGER_MAX_VALUE. Si les stagiaires se posent des questions, la réponse peut être différente en fonction de où on en est 
- Si on est encore à l'Addition / Multiplication
  => Eviter de lever des Exception, et proposer une solution "cyclique" (MAX + 1 = 0)
- Si on a traité le cas de la Division, posez vous la question en groupe et trouver une solution qui satisfasse le plus grand nombre (lever une Exception typée, introduire un objet de type "Either")

# Proposition de déroulé :  
- Présentation de la journée  
- Quicky SRP (si pas encore fait)  
- Session 1 : Objectif : implémenter l’Addition                     [20-25 mins]  

- Session 2 : Objectif : implémenter la Multiplication                 [20-25 mins]  
    - Exemples :  
      - 2 2 * => 4  
      - 3 4 * => 12  
- Session 3 : Objectif : implémenter la Division                     [20-25 mins]  
    - Exemples :  
      - 2 2 / => 1  
      - 3 4 / => 0.75  
- Code review en Mob                                 [5 mins/paire]  
- Quicky OCP  
- Session 4 : Refactoring                            [20-25 mins]  
    - Objectif : Mettre en place l’OCP  
- 🎉 Pause déjeuner 🎉  
- Session de question :   
- Par rapport à la division : est-ce qu'on peut utiliser la classe division partout où on utilise addition ?  
- Quicky LSP  
- Session 6 : Refactoring                            [20-25 mins]  
    - Objectif : Mettre en place l’OCP  
- Code review en Mod                                 [5 mins/paire]  
  
---  

# Déroulé (court)

> Ce déroulé "court" peut se tenir en 2h, mais c'est dense.

En Dojo (voir les règles du Dojo) sur le Kata ""Roman Numerals"", on abordera les 5 Principes S.O.L.I.D.  
Introduction et présentation du Kata.  

## Itération #1

> 🎯 Implémenter l'addition
> 🕓 20-25 mins

> Contrainte : Respecter le [[Single Responsibility Principle]] ([[Single Responsibility Principle|SRP]])

- Introduction au Kata
- Introduction du [[Single Responsibility Principle]] ([[Single Responsibility Principle|SRP]])
- Refactor et échanges

### Exemples

```java
"2 2 +" // input
4 // output

"3 4 +" // input)
7 // output
```

[[Single Responsibility Principle]] ([[Single Responsibility Principle|SRP]]), 

## Itération #2

> 🎯 Implémenter la multiplication
> 🕓 20-25 mins

- Présentation des UsesCases
- Introduction du [[Open-Closed Principle]] ([[Open-Closed Principle|OCP]])
- Refactor et échanges

### Exemples

```java
"2 2 *" // input
4 // output

"3 4 *" // input)
12 // output
```

[[Open-Closed Principle]] ([[Open-Closed Principle|OCP]])

## Itération #3

> 🎯 Implémenter la division
> 🕓 20-25 mins

- Présentation des UsesCases
- Introduction du [[Liskov substitution Principle]] ([[Liskov substitution Principle|LSP]])
- Refactor et échanges

### Exemples

```java
"2 2 /" // input
4 // output

"3 4 /" // input)
0.75 // output
```

Question
Question Par rapport à la division : est-ce qu'on peut utiliser la classe division partout où on utilise addition ?  

[[Liskov substitution Principle]] ([[Liskov substitution Principle|LSP]])

## Itération #4

> 🎯 Implémenter un calculateur 'normal'
> 🕓 20-25 mins

- Présentation des UsesCases  
- Introduction du [[Dependency Inversion Principle|DIP]] ([[Dependency Inversion Principle]])
- Refactor et échanges

### Exemples

```java
// Addition
"2 2 +" // input
4 // output

"3 4 +" // input)
7 // output

// Multiplication
"2 2 *" // input
4 // output

"3 4 *" // input)
12 // output

// Division
"2 2 /" // input
4 // output

"3 4 /" // input)
0.75 // output
```

# Déroulé (long)

En Dojo (voir les règles du Dojo) sur le Kata ""Roman Numerals"", on abordera les 5 Principes S.O.L.I.D.  
Introduction et présentation du Kata.  

## Itération #1 - Feature ➕

> 🎯 Implémenter l'addition
> 🕓 20-25 mins

- Introduction au Kata RPN, avec les contraintes de la session
- Refactor et échanges

### Exemples

```java
"2 2 +" // input
4 // output

"3 4 +" // input)
7 // output
```

**Questions pour le débreiff**

- Est-ce que vous êtes satisfait·e·s du nommage ou du découpage de votre code ? Que pourrait on améliorer ?
- Est-ce qu'il y a un principe SOLID que l’on pourrait déjà appliquer à cette étape de l’exercice ?
    => [[Single Responsibility Principle|SRP]]
## Itération #1.b - ♻️ SRP

> 🎯 Refactorer l'addition vers SRP
> 🕓 20-25 mins

> Contrainte : Respecter le [[Single Responsibility Principle]] ([[Single Responsibility Principle|SRP]])

- Introduction du [[Single Responsibility Principle]] ([[Single Responsibility Principle|SRP]])
- Refactor et échanges

**Questions pour le débreiff**

- Est-ce que vous êtes satisfait·e·s du nommage ou du découpage de votre code ? Que pourrait on améliorer ?
- Est-ce qu’il un a un Design Pattern que l’on pourrait utiliser pour résoudre les problèmes rencontrés ?
  (Command ?)

***Optionnel*** : présenter le Design Pattern - [[Command]]

## Itération #2 - Feature ✖️

> 🎯 Implémenter la multiplication
> 🕓 20-25 mins

- Présentation des Exemples
- Refactor et échanges
### Exemples

```java
"2 2 *" // input
4 // output

"3 4 *" // input)
12 // output
```

**Questions pour le débrief**

- Question : entre l’addition et la multiplication, est-ce qu’il y a des choses que l’on peut mutualiser regrouper ?
- Est-ce qu'il y a un principe SOLID que l’on pourrait déjà appliquer à cette étape de l’exercice ?
    => [[Open-Closed Principle|OCP]]
	=> Option : éviter OCP à ce moment, introduire la Division à la place, et introduire OCP après la division
## Itération #2.b - ♻️ OCP

> 🎯 Refactorer la multiplication vers OCP
> 🕓 20-25 mins

- Présentation des Exemples
- Refactor et échanges

**Questions pour le débrief**

- Question : entre l’addition et la multiplication, est-ce qu’il y a des choses que l’on peut mutualiser regrouper ?
- Est-ce qu’il un a un Design Pattern que l’on pourrait utiliser pour résoudre les problèmes rencontrés ?
  (Strategy ?)

***Optionnel*** : présenter le Design Pattern - [[Strategy]]

## Itération #3 - Feature ➗

> 🎯 Implémenter la division
> 🕓 20-25 mins

- Présentation des UsesCases
- Refactor et échanges

### Exemples

```java
"2 2 /" // input
4 // output

"3 4 /" // input)
0.75 // output
```

**Questions pour le débreiff**

- Est-ce qu'on peut utiliser la classe division partout où on utilise addition ?
- Est-ce qu'il y a un principe SOLID que l’on pourrait déjà appliquer à cette étape de l’exercice ?
	=> [[Liskov substitution Principle|LSP]]

## Itération #3.b - ♻️ LSP

> 🎯 Refactorer vers une solution qui respecte le LSP
> 🕓 20-25 mins

- Introduction du [[Liskov substitution Principle]] ([[Liskov substitution Principle|LSP]])
- Refactor et échanges

**Questions pour le débreiff**

- Est-ce que vous êtes satisfait·e·s du nommage ou du découpage de votre code ? Que pourrait on améliorer ?
- Est-ce qu’il un a un Design Pattern que l’on pourrait utiliser pour résoudre les problèmes rencontrés ?
	=> Null Object ?
	=> Monade ?
	=> Either ?

## Itération #4 - Feature 🧮

> 🎯 Implémenter un calculateur 'normal'
> 🕓 20-25 mins

- Présentation des UsesCases  
- Refactor et échanges
### Exemples

```java
// Addition
"2 2 +" // input
4 // output

"3 4 +" // input)
7 // output

// Multiplication
"2 2 *" // input
4 // output

"3 4 *" // input)
12 // output

// Division
"2 2 /" // input
4 // output

"3 4 /" // input)
0.75 // output
```

**Questions pour le débreiff**

- Est-ce que c’est simple ou facile de reprendre toutes les fonctionnalités d’un coup ? Que faudrait il pour rendre cette manipulation plus fluide ?
- Est-ce qu'il y a un principe SOLID que l’on pourrait déjà appliquer à cette étape de l’exercice ?
- Est-ce qu’il un a un Design Pattern que l’on pourrait utiliser pour résoudre les problèmes rencontrés ?

## Itération #4.b - ♻️ DIP

> 🎯 Refactore vers DIP
> 🕓 20-25 mins

- Introduction du [[Dependency Inversion Principle]] [[Dependency Inversion Principle|DIP]]
- Refactor et échanges

**Questions pour le débreiff**

- Est-ce que c’est simple ou facile de reprendre toutes les fonctionnalités d’un coup ? Que faudrait il pour rendre cette manipulation plus fluide ?
- Est-ce qu’il un a un Design Pattern que l’on pourrait utiliser pour résoudre les problèmes rencontrés ?

## Rétro finale

- Est-ce que tout le monde a pu montrer tout ou partie de son code ?
- Est-ce que vous vous êtes amusé.e ?
- Qu’est ce que vous avez appris ?
- Optionnel : présenter [[Interface segregation Principle|ISP]], le I de SOLID qu'on n'a pas pratiqué