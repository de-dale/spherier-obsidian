🎯 **Objectif** : #🔭Découverte 
	Connaissez vous les principes [[SOLID]] ? Il s'agit de 5 principes de développement logiciel, réputé garantir la qualité des logiciels que nous développons.
	Au travers de 5 exercices, découvrons ces 5 principes.
🕓 **Durée** : #1h🕓 x5
👥 **Participants** : #👥2-n

Le but de ce Kata, est de faire découvrir une partie de [[SOLID]] : 
- [[Single Responsibility Principle]] ([[Single Responsibility Principle|SRP]]), 
- [[Open-Closed Principle]] ([[Open-Closed Principle|OCP]])
- [[Liskov substitution Principle]] ([[Liskov substitution Principle|LSP]]).  

Dans cet exercice, on va mettre de coté :  
- La soustraction ; trop proche de l’addition et qui engendre des questions sur les cas au limite trop tôt sur leur codebase  
- La composition des opérations, qui va trop loin par rapport au but de l’exercice  
  
# Introduction du Kata  
  
Présenter [[SOLID]], si ce n’a pas été fait avant.   
Pour avoir le temps d’insister sur [[Open-Closed Principle|OCP]] et [[Liskov substitution Principle|LSP]], c’est plus facile d’avoir fait [[Single Responsibility Principle|SRP]] avant, et de ne pas trop s’attarder dessus.   
Au vu des promotions précédentes, le [[Single Responsibility Principle|SRP]] s’assimile rapidement.  
  
Présenter la Reverse Polish Notation :  
http://codingdojo.org/kata/RPN/  
  
Poser quelques contraintes :  
- On ne prend en entrée que des entiers positifs  
- On ne retourne que des nombres positifs  
  
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

# Déroulé 

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
- Introduction du [[Work/Software/Dependency inversion Principle|DIP]] ([[Work/Software/Dependency inversion Principle]])
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
