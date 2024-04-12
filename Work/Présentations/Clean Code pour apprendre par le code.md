---
ressource:
  - 🎥 Talk
tags:
  - Brouillon
  - 🚧wip
  - 🫧CleanCode
relates:
  - "[[Conférence Clean Code ou Manuel de lecture du code]]"
  - "[[Knowledge Driven Development]]"
  - "[[Clean Code]]"
---
# Modèle mental 

-> On a tous des modèles mentaux  
-> Connaître ses modèles mentaux permet d'apprendre à se défait de ses préjugés (cf. 5ième Discipline de Peter Senge)  
-> Ils influencent l'image que nous nous faisons du monde  
-> Il s'agit des croyances, postulats, hypothèses ou représentation qu'a une personne sur elle même, les autre et le monde  
-> Un concept, un système ou une manière de voir le monde qui nous aide à comprendre comment les choses fonctionnent  
-> Tous les modèles sont faux, mais certains sont utiles (George Box,)  
-> Modeling = coding  
  
# Code Legacy

-> Factuel : il existe  
-> C'est le mode d'emplois réel du logiciel  
-> C'est l'opportunité d'apprendre de nos prédécesseurs  
  
# Code legecy
-> Comment l'appréhender  : via des [[Code Review]] :  
--> Se poser et lire du code pendant un temps, avec son équipe ou seul  
--> Validation de PR/MR  
--> Via du Pair/Mob Programming où on a en plus les explications verbales  
  
Code legacy  
-> Comment l'appréhender -> Connaître les codes smells et les schémas de lecture de notre contexte  
  
Clean Code  
-> Permet dans son contexte, de présenter des Normes et standards  
-> permet de guider les équipiers à adopter le modèle mental qui convient au contexte  
--> Cela facilite l'apprentissage et l'on-boarding  
--> #CollectiveOwnership  
  
Clean code   
= code maintenable ?  
-> ça veut dire quoi "maintenable" ?  
==> Maintenable = quelqu'un d'autre peut se l'approprier et corriger les defect/bugs/incompréhention  
= le mieux que l'on puisse faire de notre point de vue aujourd'hui  
  
Clean Code  
-> Comment ? => Nommage  
--> Se poser la question du nom des choses  
-> Ubiquitous language (DDD)  
-> eXtreme Programming : Communication / system metaphor + Coding standards  
- séparer développer  / nommer  
- Méthode : 3 Steps Models (Feitelson)  
  
Clean Code  
-> Comment ? => Patterns  
-> Les [[Design Patterns]] donnent une grille de lecture des problèmes qu'ils résolvent  
-> Comment ? => Modéliser le métier  
--> Nommer les concepts  
--> Réfléchir à la Cohésion/Couplage des notions métier rencontrées  
  
Clean Code  
-> Comment ? => Principes/Tips/Guides  
-> [[Shu Ha Ri]] (Connaitre, Maîtriser, dépasser)  
-> ne pas être dogmatique car c'est du gatekeeping  
-> on convain mieux sans buzzwords  
-> SOLID, Demeter, KiSS, YAGNI, DRY  
  
Clean Code vs Code Legacy  
Code qui correspond à notre modèle mental => Code qui nous fait plaisir  
vs.  
Code qui ne correspond pas à notre modèle mentatl => Code qui nous fait souffrir  
  
Refactor (posture d'écrivain) vs. Code review (posture de lecteur et 'apprenant)  
<Schéma que j'arrivera pas à reproduire>  
Adapter le code pour qu'il corresponde à notre modèle mental  
vs.  
Apprendre depuis le code et faire évoluer son propre modèle mental en conséquence  
  
Refactoriser   
= Passerelle entre le Clean Code et le Code legacy  
-> passerelle passe par notre cerveau  
"[[Writing is Thinking]]"  
  
Code Reveiw  
= Passerelle entre le Code Legacy et Clean Brain/Code  
-> passe par notre cerveau  
  
Zone de confort vs Inconnu  
<Schéma>  
Confrt/Sécurité vs Peur/Douleur  
Boucle entre les deux  
-> Sortir de la zone de confort vers l'inconnu pour apprendre  
-> Rentrer dans la zone de confort pour se rassurer/ réaffirmer ce que l'on sait.  
? travailler sur une notion de Zone d'inconfort ?