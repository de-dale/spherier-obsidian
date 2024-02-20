---
titre: 
ressource: 📰 Article
author: "[[Rob Myers]]"
link: https://www.agileinstitute.com/articles/avoiding-tech-debt-w-the-core-four-practices
trello: https://trello.com/c/niB2SfsG/511-avoiding-tech-debt-with-these-core-four-practices-agile-institute
---
# Notes

> Dette technique : Report d'une bonne conception par soucis d'opportunité.  
> => Volontaires ou accidentelle

> Bon design :
- Partage l'intention du comportement du code avec toute l'équipe
- Facilite les changements futurs attendus comme inattendus.

> Réduire la dette =>
- Partager l'intention actuelle
- Rendre le code extensible et maintenable
> => Porte un nom : le Refgactoring
> TDD  
> Pair ou Mob Programming  
> CI

=> Diagramme "Coeur"

 `/  TDD  \   /  CI  \ |         \ /        |  \    Refactoring   /    \              /    Pair/Mob Programming`

```
	
        @@@@@@           @@@@@@
      @@@@@@@@@@       @@@@@@@@@@
    @@@@@@@@@@@@@@   @@@@@@@@@@@@@@
  @@@@@@ TDD @@@@@@ @@@@@@ CI @@@@@@@
 @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@ REFACTORING @@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
 @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
  @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
   @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
    @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
      @@@@@@@@@@@@@@@@@@@@@@@@@@@
        @@@@@ PAIR /  MOB @@@@@
          @@@ PROGRAMMING @@@
            @@@@@@@@@@@@@@@
              @@@@@@@@@@@
                @@@@@@@
                  @@@
                   @
```