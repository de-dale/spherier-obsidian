
### Objectif

- Référencer les pratiques connues
- Savoir si les équipes maîtrisent les pratiques
- Savoir quelles pratiques appliquent les équipes

Les équipes de la Supply s’approprient ensuite les pratiques, se forgent leur opinion, et constituent leur propre catalogue de décisions

# Les pratiques

Les pratiques de cette liste, sont à tagguer avec l’une des étiquettes suivantes, et s'inspirent de ce qui est fait pour des [[Tech Radar - Radar technologique]].

- **ADOPTER** : Pratique stratégique et fondamentale
- **ESSAYER** : les pratiques essentielles qui fonctionnent, mais dont les limites sont à tester
- **ÉVALUER** : les pratiques prometteuses, à étudier de manière approfondie pour envisager une utilisation future
- **SUSPENDRE** pratiques utilisées qui se sont avérées peu satisfaisantes et qui ne sont donc pas recommandées
- **PRÉSENTER** Pratiques identifiées, mais pas encore présentées à l’ensemble de l'équipe
- **CLARIFIER** : Pratique identifiées, mais par qui n’est pas comprise de la même manière par toutes les personnes de l'équipe.

> [!caution] Format des pratiques
> 
> Le format de cette partie reste à consolider
> 
> Idées :
> - Répartir les pratiques par Catégorie
> - Mettre en place un formalisme semblable aux ADR (Architecture Décision Record)
 >   - titre
 >   - statut (Etat de la proposition)
 >       - 📬Proposé
 >       - ✅ Accepté
 >       - ❌ Rejeté
 >       - ✂️ Déprécié
 >       - ♻️ Remplacé
 >   - contexte
 >   - décision
 >   - conséquences

# Exemples de pratiques

**⌨️ Pratiques sur le code**
Guard Clause | ÉVALUER
Code Owners | ADOPTER
Documenter les décisions de conception logicielle par des ADR (Architecture Decision Records) | PRÉSENTER
 
**🚥 Pratiques sur le process de développement**
MEP : Capitaine de prod | ESSAYER
Tidyings | ESSAYER
 
**📖 Pratiques sur les Merge Requests**
C’est celui qui ouvre des thread qui les ferme | ADOPTER
C’est celui qui ouvre la MR qui la merge | ADOPTER
Quand on ajoute un commentaire, on donne une alternative | ÉVALUER
MR du jour, Bonjour | ÉVALUER
Utiliser les Conventional Comments | PRÉSENTER
Ship/Show/Ask | SUSPENDRE
Les Contrats d’Interface peuvent être relus par l’ensemble de la SUPPLY | ÉVALUER
 
**🚀 Pratiques sur les Demandes de Changement (Demande de MEP)**
Renseigner les lien des Boards New Relic des composants impliqués dans le Changement | CLARIFIER
Normaliser les messages de log | PRÉSENTER
 
**Pratiques d'équipe**
Partager sa veille technologique | ÉVALUER
Partager sa veille technologique sur un point de partage DEV | ESSAYER
Faire des blagues | ÉVALUER
## Pratiques sur le code

- **Guard Clause** | Pratique à ÉVALUER  
    Utiliser des Guard Clauses dans le code est une pratique identifiée, mais pour laquelle on n’a pas de préconisation spécifique.
- **Code Owners** | Pratique à PRÉSENTER  
    Dans le cadre de l'évaluation de la maintenabilité du parc applicatif Supply, on s’est rendu compte qu’il y a un bon nombre de composants applicatifs dont la responsabilité n'était pas évidente.  
    Exemple : on a des composants de la responsabilité de TRP, STK, PRO ou PDV dans le même SF.  
    Mettre en place le fichier de CODEOWNERS permettrait de répondre à ce problème.
## Pratiques sur le process de développement

- **MR : C’est celui qui ouvre des thread qui les ferme** | Pratique à ADOPTER
- **MR : C’est celui qui ouvre la MR qui la merge** | Pratique à ADOPTER
- **MEP : Capitaine de prod** | Pratique à ESSAYER
- **MR : Ship/Show/Ask** | Pratique à SUSPENDRE
	  [[Ship Show Ask]]
- **Tidyings** | Pratique à ESSAYER
    La pratique n’est pas encore tout à fait cadrée, mais on peut l’essayer sur cette itération.
	[[Tidying]]