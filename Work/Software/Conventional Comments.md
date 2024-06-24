---
ressource:
  - 🔧 Pratique
relates:
  - "[[Code Review]]"
---
Il s'agit d'une convention de commentaires de [[Code Review]] asynchrone, permettant d'expliciter au mieux notre communication, tout en ménageant celui qui reçoit le commentaire.

Le format conventionnel se présente de la manière suivante :
```
<label> [decoration]: <sujet>

[discussion]
```
- **label** : Étiquette permettant de comprendre de quel type de commentaire, il s'agit
- **sujet** : Message principal du commentaire
- **décoration** (optionnel) : Précision(s) à rajouter à l'étiquette  principale. Elles sont entre parenthèses, et séparées par des virgules.
- **discussion** (optionnel) : Il s'agit de développer le message principal en expliquant le "pourquoi et les prochaines étapes

Lien vers un super article : [Conventional Comments : faire des revues de code avec le smile(y)](https://www.24joursdeweb.fr/2021/conventional-comments-faire-des-revues-de-code-avec-le-smiley/)
### Exemples d'étiquettes

Dans la mesure du possible, déterminez les étiquettes en équipe.

| **Etiquette** | **Trad**                       | **Exemple de Signification**                                                                                                                                                                                                                                                                                                |
| ------------- | ------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| praise:       | éloge                          | Les éloges mettent en avant quelque chose de positif. Essayez de laisser au moins un commentaire de ce type par review : cherchez quelque chose dont faire l'éloge sincèrement.                                                                                                                                             |
| nitpick:      | pinaillage/tatillon/ pétouille | Les pinaillages sont des modifications petites, triviales, mais indispensables. Mettre en avant les pinaillages permet de se concentrer sur les commentaires nécessitant davantage de réflexion.                                                                                                                            |
| suggestion:   | suggestion                     | Une suggestion propose une amélioration de ce qui est commenté.<br><br>Soyez clair et explicite sur ce que vous proposez, et pourquoi c'est une amélioration.                                                                                                                                                               |
| issue:        | problème                       | Cette étiquette met en avant une problématique spécifique sur ce qui est commenté. Dans la mesure du possible, ajoutez une suggestion d’action ou d’amélioration.<br><br>Si vous n'êtes pas sûr(e) que le problème existe, utilisez plutôt une “question”.                                                                  |
| question:     | question                       | Lorsque vous ne comprenez pas le code reviewé, ou si vous suspectez un problème (sans en être certaine ou certain), alors posez une question.<br><br>Demander de clarifier ou d’investiguer peut conduire à une résolution rapide.                                                                                          |
| thought:      | pensée/idée                    | Quand vous relisez du code, vous avez parfois des idées qui vous viennent en tête. Ces idées sont non-bloquantes par nature, mais ont beaucoup de valeur et peuvent conduire à des initiatives précises (sur du refecto par exemple) ou à des opportunités de partager un concept (ex: un DesignPattern à mettre en place). |
| chore:        | routine                        | Les routines sont des tâches simples à réaliser and que le sujet ne soit officiellement “terminé”. Souvent, il s’agit de référence vers le processus (ex : mettre à jour le CHANGELOG).<br><br>Si vous l’avez, pensez à indiquer le lien vers le process pour s’y référer par la suite.                                     |
### Exemples de décoration

Comme pour les étiquettes, cherchez à vous construire votre banque de décoration d'équipe.

| **Décoration** | **Exemple de Signification** |
| ---- | ---- |
| (non-blocking) | Un commentaire avec cette précision signifie qu’il ne bloque pas la Code Review. |
| (blocking) | Un commentaire avec cette précision signifie que la Code Review est bloquée tant que le sujet n’a pas été résolu. |
| (if-minor) | Cette précision donne liberté à l’auteur du code de résoudre le problème seulement si les changements sont mineurs ou triviaux. Si on se rend compte que le sujet est plus important, il pourra faire l’objet d’une autre modification de code. |
| (unit-test) | Les commentaires avec cette précision font référence à du code en rapport avec les tests unitaires. |
| (performance) | Les commentaires avec cette précision font référence à la performance du code. |

### Étiquettes avec Émoji

Coupler les émojis avec les étiquettes permet de visualiser plus facilement l'intention du commentaire.
Les émoji permettent de visualiser rapidement le contexte le commentaire. Pour garantir leur signification il vaut mieux les associer avec une étiquette.

Vous pouvez aussi utiliser l'**échelle d’engagement** (voir plus bas 👇) pour illustrer l’importance que le commentaire a pour vous.

| **Emoji** | **Gitlab** | **Exemple(s) de Signification** |
| ---- | ---- | ---- |
| `🥜 peanuts` | :peanuts: | - Pour renforcer le caractère non-bloquant d’un commentaire |
| `❓ question` | :question: | - Pour renforcer une question |
| `💬 discussion` | :speech_balloon: | - Pour renforcer la nécessité de discuter du sujet. |
| `🚨 alerte` | :rotating_light: | - Pour renforcer le caractère bloquant d’un commentaire |
| `🚫 no-go` | :no_entry_sign: | - Pour renforcer le caractère bloquant d’un commentaire |
| `👏 bravo` | :clap: | - Pour renforcer une éloge |
| `⚠️warning` | :warning: | - Pour renforcer l’attention à porter à un commentaire |
| `☠️ bad idea` | :skull_crossbones: | - Pour illustrer une suggestion (attention à faire attention à ce que le receveur le prenne bien) |
| `✨ magic` | :sparkles: | - Pour illustrer quelque chose qui est magiques dans le code reviewé<br>    <br>- Pour mettre en évidence des nombre magiques dans le code |
| `🔥 burn-it-all` | :fire: | - Pour mettre en évidence du code à supprimer |
# Échelle des niveaux d'engagements

![[Échelle des niveaux d'engagements]]