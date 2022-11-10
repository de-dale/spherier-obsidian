# Conventional Comments

Il s'agit d'une convention de commentaires de [[Code Review]], permettant d'expliciter au mieux notre communication, tout en ménageant celui qui reçoit le commentaire.

Le format conventionnel se présente de la manière suivante :
```
<label> [decoration]: <sujet>

[discussion]
```
- **label** : Étiquette permettant de comprendre de quel type de commentaire, il s'agit
- **sujet** : Message principal du commentaire
- **décoration** (optionnel) : Précision(s) à rajouter à l'étiquette  principale. Elles sont entre parenthèses, et séparées par des virgules.
- **discussion** (optionnel) : Il s'agit de développer le message principal en expliquant le "pourquoi et les prochaines étapes

### Exemples d'étiquettes

> [!warning] TODO
> - [ ] Reprendre le tableau

| Etiquette   | Trad                |                                                                                                                                                                                                                                                                           |
| ----------- | ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| praise:     | éloge               | Les éloges mettent en avant quelque chose de positif. Essayez de laisser au moins un commentaire de ce type par review : cherchez quelque chose dont faire l'éloge sincèrement.                                                                                           |
| nitpick:    | pinaillage/tatillon | Les pinaillages sont des modifications petites, triviales, mais indispensables. Mettre en avant les pinaillages permet de se concentrer sur les commentaires nécessitant davantage de reflexion?                                                                                                                                                                                          | 
| suggestion: | suggestion          | Une suggestion propose une amélioration de ce qui est commenté. Soyez clair et explicite dans votre suggestion, et pourquoi c'est une amélioration.                                                                                                                 |
| issue:      | problème            | Issues highlight specific problems with the subject under review. These problems can be user-facing or behind the scenes. It is strongly recommended to pair this comment with a suggestion. If you are not sure if a problem exists or not, consider leaving a question. |
| question:   | question            | Questions are appropriate if you have a potential concern but are not quite sure if it’s relevant or not. Asking the author for clarification or investigation can lead to a quick resolution.                                                                            |
| thought:    | pensée/idée         | Thoughts represent an idea that popped up from reviewing. These comments are non-blocking by nature, but they are extremely valuable and can lead to more focused initiatives and mentoring opportunities.                                                                |
| chore:      | routine             | Chores are simple tasks that must be done before the subject can be “officially” accepted. Usually, these comments reference some common process. Try to leave a link to the process description so that the reader knows how to resolve the chore.                       |

### Exemples de décoration
| Argument       | Meaning                                                                                                                                                                                             |
| -------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| (non-blocking) | A comment with this decoration should not prevent the subject under review from being accepted. This is helpful for organizations that consider comments blocking by default.                       |
| (blocking)     | A comment with this decoration should prevent the subject under review from being accepted, until it is resolved. This is helpful for organizations that consider comments non-blocking by default. |
| (if-minor)     | This decoration gives some freedom to the author that they should resolve the comment only if the changes ends up being minor or trivial.                                                           |
| (unit-test)    | Comment with this decoration suggests something related to unit tests.                                                                                                                              |
| (performance)  | Comment with this decoration suggests something related to performance.                                                                                                                             |


### Étiquettes avec Émoji

Coupler les émojis avec les étiquettes permet de visualiser plus facilement l'intention du commentaire.

- 🥜 peanuts, 
- ❓question, 
- 💬 discussion, 
- 🚨 alerte, 
- 🚫 no-go, 
- 👏 bravo, 
- ⚠️warning, 
- ☠️ bad idea, 
- ✨ magic, 
- 🔥 burn-it-all