---
relates:
  - "[[Policy"
---

Statégie


# 🤖 Définition par l'IA

In Event Storming, a Policy acts like a bridge between a Domain Event and a Command. It essentially defines a rule that dictates how the system should react to a specific event.

Here's a breakdown:

- **Domain Event:** This is a significant occurrence within the domain you're modeling. It's a past-tense statement describing something that has happened, like "Order Placed" or "Payment Received."
- **Command:** This represents an action or decision taken by a user or external system. It triggers the Domain Event.
- **Policy:** This sits between the Event and the Command, specifying the system's response. It's typically phrased as "When [Event], Then [Command]". For instance, "When Payment Received, Then Confirm Order".

Think of policies as automated business rules. They can be simple or complex, but they essentially define how the system should behave based on specific events.

Here are some additional points about Policies in Event Storming:

- They are often visualized on a sticky note during an Event Storming session, typically colored lilac.
- Policies can represent manual or automated processes.
- They can get intricate, so the phrase "lie detector" is sometimes used to highlight that there might be more to a policy than initially meets the eye.

By incorporating Policies, Event Storming helps capture the decision-making logic within your system and ensures a clear understanding of how events trigger actions.

Dans le contexte de l'Event Storming et du Domain Driven Design (DDD), le terme "Policy" peut se traduire en français de plusieurs manières, selon la nuance souhaitée et le contexte spécifique. Voici quelques options :

1. **Règle:** Cette traduction met l'accent sur l'aspect prescriptif des Policies, définissant les règles à suivre en réponse à un événement.
2. **Directive:** Semblable à "Règle", "Directive" souligne le caractère obligatoire des Policies, indiquant les actions à entreprendre.
3. **Politique:** Cette traduction est plus générique et peut convenir à divers contextes, englobant les directives, les règles et les principes qui régissent le comportement du système.
4. **Stratégie:** "Stratégie" met l'accent sur l'aspect décisionnel des Policies, soulignant le choix délibéré d'une action spécifique en réponse à un événement.
5. **Procédure:** Cette traduction met en avant l'aspect séquencé des Policies, décrivant les étapes à suivre pour traiter un événement.
6. **Algorithme:** "Algorithme" est pertinent pour les Policies plus complexes qui impliquent une logique de décision plus élaborée et des étapes de traitement spécifiques.