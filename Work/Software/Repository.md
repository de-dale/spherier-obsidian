---
ressource:
  - 📰 Article
  - 🧠 Concept
author:
  - "[[Martin Fowler]]"
link:
  - https://martinfowler.com/eaaCatalog/repository.html
trello: https://trello.com/c/kVP2rac2/845-repository-pattern-of-enterprise-application-architecture-martin-fowler
relates:
  - "[[EventStorming]]"
  - "[[Design Patterns]]"
---
> _Mediates between the domain and data mapping layers using a collection-like interface for accessing domain objects._

Assure la médiation entre les couches de domaine et de mappage de données à l'aide d'une interface de type collection pour accéder aux objets de domaine.

DDD vite fait https://drive.google.com/file/d/1AF37WCcqXVeUmgK_mAzPU5zl5tk92hTr/view?usp=drive_link
p 59

If the infrastructure makes it easy to
do so, the developers of the client may add more traversable
associations, muddling the model. On the other hand, they may
use queries to pull the exact data they need from the database, or
to pull a few specific objects rather than navigating from
Aggregate roots. Domain logic moves into queries and client
code, and the Entities and Value Objects become mere data
containers.

https://www.domainlanguage.com/wp-content/uploads/2016/05/DDD_Reference_2015-03.pdf

https://svatasimara.medium.com/domain-driven-design-part-5-repository-d5ad32b2e06f
https://medium.com/@yohata/mastering-ddd-repository-design-patterns-in-go-2034486c82b3
https://www.abrahamberg.com/blog/repository-pattern-in-ddd-bridging-the-domain-and-data-models/

https://www.geeksforgeeks.org/repository-design-pattern/
https://www.umlboard.com/design-patterns/repository.html
https://medium.com/@pantaanish/understanding-repository-pattern-with-implementation-a-step-by-step-guide-ca1bf36be3b4
https://medium.com/@pererikbergman/repository-design-pattern-e28c0f3e4a30

# IA

##   Le Design Pattern "Repository"

Le design pattern "Repository" est un pattern de conception logicielle qui vise à **abstraire l'accès aux données** d'une application. Il permet de séparer la logique métier de l'application des détails techniques liés à la persistance des données, tels que le type de base de données utilisée ou les requêtes SQL nécessaires pour y accéder.

**Avantages du pattern "Repository" :**

- **Amélioration de la testabilité:** En isolant l'accès aux données, il devient plus facile de tester l'application indépendamment de la base de données utilisée.
- **Meilleure maintenabilité:** Le code est plus facile à comprendre et à modifier car la logique métier est séparée des détails de persistance.
- **Flexibilité accrue:** Il est plus simple de changer de base de données ou de mode de persistance sans affecter le reste de l'application.
- **Réutilisabilité:** Le pattern "Repository" peut être réutilisé dans différentes parties de l'application, ce qui réduit la duplication de code.

**Comment fonctionne le pattern "Repository" ?**

Le pattern "Repository" utilise une interface appelée **"Repository"** qui définit les méthodes pour accéder aux données. Cette interface est implémentée par des classes spécifiques, appelées **"Repositories concrets"**, qui fournissent l'implémentation des méthodes d'accès aux données pour un type de persistance particulier (par exemple, une base de données SQL, un fichier JSON, etc.).

**Exemple d'utilisation du pattern "Repository" :**

Imaginons une application de gestion des clients. La logique métier de l'application pourrait utiliser un repository pour :

- **Récupérer les informations d'un client par son ID.**
- **Ajouter un nouveau client.**
- **Mettre à jour les informations d'un client existant.**
- **Supprimer un client.**

**Le pattern "Repository" est un outil précieux pour les développeurs qui souhaitent créer des applications propres, testables et maintenables.**

**Voici quelques exemples de frameworks et bibliothèques qui implémentent le pattern "Repository" :**

- **Java:** Spring Data JPA, Hibernate
- **C#:** Entity Framework Core
- **Python:** SQLAlchemy
- **JavaScript:** TypeORM

**Ressources supplémentaires :**

- [https://en.wikipedia.org/wiki/Repository](https://en.wikipedia.org/wiki/Repository)
- [https://www.geeksforgeeks.org/repository-design-pattern/](https://www.geeksforgeeks.org/repository-design-pattern/)
- [https://medium.com/@arjunarora171997/repository-pattern-f994d5776373](https://medium.com/@arjunarora171997/repository-pattern-f994d5776373)