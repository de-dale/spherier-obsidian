

Formateur·ice·s: Adrien JOLY
Pédagogie: 30% théorique, 70% pratique
État: En cours
📚 Thématiques: Technique (https://www.notion.so/Technique-7344967dad7646fab84a3b4f03d10eb3?pvs=21)
Dernière modification: September 4, 2023 3:42 PM

# Description

Depuis sa création en 2009, Node.js est devenue une technologie incontournable pour prototyper puis faire passer à l’échelle des logiciels de type variés: APIs web en tout genre: SAAS, dashboards, sites e-commerce, réseaux sociaux, pipelines de données…

Node.js a contribué à faire de JavaScript (et son petit frère: TypeScript) un langage incontournable pour développer des applications modernes, que ce soit sur le web ou autres environnements d’exécution.

En revanche, le langage JavaScript n’a pas été conçu pour écrire des logiciels robustes. Et l’apport de typage statique par TypeScript, même s’il apporte de nombreux bénéfices, n’apporte aucune garantie quant à la qualité du code produit, et ajoute même son lot de complexité et de surprises.

Ajoutons à cela l’apparente accessibilité d’usage de ces langages, l’absence de consensus sur les bonnes pratiques de développement associées et la prolifération de frameworks installable en saisissant une simple commande npm… Tous les ingrédients sont réunis pour que nos équipes de développement finissent par perdre la maîtrise du code Node.js qu’ils avaient pourtant eu tellement de facilité à écrire !

En pratique, cette perte de maîtrise peut avoir de lourdes conséquences sur l’entreprise: ralentissement du rythme d’évolutions produit, bugs et régressions fonctionnelles qui font fuir les utilisateurs vers la concurrence, fuite des talents…

Cette formation s’adresse aux personnes (lead ou pas) contribuant au développement de code Node.js, pour qui la qualité et la robustesse durables ne sont pas une option.

Elle s’appuie sur une expérience de plus de 10 ans d’usage de Node.js en entreprise et l’adaptation de bonnes pratiques employées avec succès par les communautés d’autres langages de POO (programmation orientée objet) et de programmation fonctionnelle. Le tout, avec une sensibilité « craft » (apprentissage en continu, emploi non dogmatique de pratiques permettant d’aligner le logiciel avec les besoins métier associés, écriture de code de qualité et pérenne) et « DevOps » (responsabiliser l’équipe de développement sur la qualité et l’amélioration continue, en maîtrisant la livraison régulière, voire continue, de code en production).

Cette formation bénéficiera particulièrement aux développeurs de votre équipe si:

- Plus d’1 mise en production sur 10 se solde par un incident, l’apparition de bugs et/ou de régressions ?
- Votre application met plusieurs dizaines de secondes (voire minutes) à démarrer, et/ou sa performance en production laisse à désirer ?
- Votre équipe passe régulièrement plus d’une journée pour reproduire puis résoudre des bugs observés en production ?
- Vous ne voyez pas le bout de la “refonte” dans laquelle vous vous êtes lancé·e·s, ou celle-ci semble causer plus de problèmes qu’elle n’en résout ?
- Les dévs rechignent à contribuer à certaines parties du code, par manque de compréhension et/ou peur de “tout casser” ?

Ne vous inquiétez pas, ces problèmes sont courants après quelques années de développement sur du code Node.js, notamment dans les projets qui évoluent en permanence. (ex: startups)

*<Qu’est-ce qui sera abordé lors de la formation ? ⇒ cf Programme>*

# Objectifs

Cette formation va vous faire découvrir et pratiquer les outils et méthodes qui vous aideront à:

- rendre votre code Node.js plus clair, facile à comprendre, et donc: maintenable et réparable;
- adapter l’architecture de votre application Node.js de manière à ce qu’elle soit plus performante en production, à l’échelle des besoins de chaque instant;
- retrouver un niveau de sérénité, vélocité et confiance similaire à celui que vous aviez au début de votre projet.

# Programme

- **Introduction** (~2h)
    - 🙋‍♂️ Tour de table, pour faire connaissance. (~15mn)
    - 🙋‍♂️ Cartographie des difficultés et problèmes liés à nos applications Node.js. (~45mn)
        - Problèmes typiques:
            - Bugs nombreux / zones “dangereuses” dans le code / difficulté à écrire des tests auto ← Couplage fort dans le code
            - Problèmes de performance / scalabilité ← Couplage fort dans l’architecture
            - Les défauts/bugs sont découverts par les utilisateurs, et/ou difficiles à reproduire ← Mauvaise gestion des erreurs (dont instrumentation/monitoring) et/ou typage fort
    - 🧑‍🏫 Présentation du programme de la formation. (~5mn)
    - 💻 Découverte de la codebase historique sur laquelle nous allons pratiquer (~20mn)
    - 🙋‍♂️ Quels problèmes voyez-vous ? Par quoi commenceriez-vous ? Comment s’y prendre ? (~20m)
- **Les différents types d’erreurs** qui peuvent se produire, et comment les gérer ? (~2h)
    - 🧑‍🏫 Présentation (avec exemples) des différents types d’erreurs:
        - Erreurs hors de notre contrôle, ex: erreurs réseau
        - Erreurs de validité venant de l’extérieur du système (retours d’APIs et/ou de l’utilisateur)
        - Erreurs liées à l’environnement: env vars, mémoire, espace disque…
        - Erreurs de cas non prévus: violations de pré-requis / hypothèses
        - Erreurs de programmation, ex: `XXX is undefined`
    - 🙋‍♂️ Pratique: qualifications du type de plusieurs erreurs, dans notre codebase d’exemple
    - 🙋‍♂️ Que veut-on faire de ces erreurs, au juste ?
        - Exemples: `console.log`, Sentry, outils de monitoring cloud, affichage à l’utilisateur ?
    - 🧑‍🏫 À quel endroit faut-il intercepter (ou pas) les erreurs ?
    - 🧑‍🏫 Comment rendre nos rapports d’erreurs plus exploitables, en vue de les reproduire et corriger les bugs ? (spoiler: en ajoutant des métadonnées structurées)
- **Faire du typage fort (TypeScript) un allié** pour réduire les surprises en production (~2h)
    - 🧑‍🏫 Pourquoi ? Comment ?
        - Objectif: détecter les erreurs de programmation pendant le développement
        - Stratégie: mettre en place une validation stricte des types de données avec TypeScript
        - Tactique: s’appuyer sur ESLint pour prévenir les assertions de type (`as`) incorrectes
    - 💻 Corriger les erreurs de type et de linter d’un module typé
    - 🌟 Pro-tip: usage de JSDoc pour commencer à typer une codebase JavaScript
- **Détecter les bugs et regressions plus vite** grâce à des tests auto bien écrits (~2h)
    - 🧑‍🏫 Concept “d’objet testé” + survol des types de tests: e2e vs unitaire vs integration.
    - 🧑‍🏫 Principes FIRST et autres recommandations pour des tests bien écrits et maintenables.
    - 💻 Compléter et exécuter différents types de test sur du code Node.js existant
    - 🌟 Bonus: les tests comme moyen de conception émergente (TDD)
    - 🌟 Bonus: les tests comme moyen de prouver le respect des exigences fonctionnelles (BDD)
- **Des fonctions plus faciles à tester**, grâce au découplage / inversion de dépendance (~2h)
    - 🧑‍🏫 Problèmes classiques liés aux tests: ça ramme et/ou on ne comprend pas pourquoi ça échoue
    - 🧑‍🏫 Présentation de l’inversion de dépendance comme solution à ces problèmes
    - 💻 Améliorer un test en inversant les dépendances de la fonction ciblée
    - 🌟 Survol des autres principes SOLID
- **Refactoring: pourquoi faire ?** + survol des techniques applicables (~2h)
    - 🧑‍🏫 Différence entre “refonte”, “refactoring”, “changement fonctionnel” et “correction de bug”
    - 🧑‍🏫 Définition du “refactoring”
        - Analogie avec la manipulation d’équations mathématiques
        - Exemple de code: avant/après refactoring.
        - Exemple de diagramme de séquence: avant/après refactoring.
    - 🧑‍🏫 Survol des techniques: “safe refacto” à l’aide de son IDE, “mikado”, “scratch”, “strangler”
    - 💻 Appliquer technique “scratch refactoring” sur un module fourni
    - 🙋‍♂️ Quelles améliorations observe-t-on après avoir refactorisé ce code ? Des fausses bonnes idées à partager ?
    - 🌟 Survol de quelques règles de “Clean Code”
- **Refactoring sûr**: recettes de base (extract / move / inline / etc…) (~2h)
    - 🧑‍🏫 Dans quel cas utiliser ces recettes ? Jusqu’où faut-il aller ?
    - 🧑‍🏫 Démonstration de chaque recette
    - Exemple de code: avant/après refactoring.
    - 💻 Appliquer ces recettes sur cet exemple, pour arriver à cette fin
    - 🙋‍♂️ Impressions: est-ce que l’IDE fait (toujours) bien son boulot ? Voyez-vous d’autres recettes dsûres ?
- **Refactoring risqué**: écrire des tests pour éviter les régressions (~4h)
    - 🧑‍🏫 Que veut-on dire par “risqué” ? Dans quels cas sommes-nous concernés ?
    - 🧑‍🏫 Comment procéder ?
        - Explication du principe, en donnant un exemple de situation risquée.
        - Écriture et exécution d’approval tests: avant et après le refactoring.
        - Comment éviter les échecs accidentels ? (ex: retrait des temporisations)
    - 💻 Écrire des tests approval sur un endpoint API fourni, en vue de son refac
    - 🌟 Que faire des tests approval, après le refactoring ?
    - 🌟 Technique du “point de couture” (”seam”) de Michael Feathers
- **Décommissionnement progressif** par “étrangement” (strangler fig pattern) (~4h)
    - 🧑‍🏫 Dans quel cas faut-il employer cette technique ?
    - 🧑‍🏫 Exemple de situation: un cache interne qui cause des problèmes de maintenabilité et de performance. ⇒ Risques de le retirer ou améliorer à l’aide des techniques précédentes, voire “au feeling”.
    - 🧑‍🏫 Explication de la stratégie de décommissionnement progressif par “étrangement”.
    - 💻 [en groupe, sur un dépôt partagé] décommissioner un cache d’utilisateurs
    - 🌟 Pro tip / démo: usage d’AST pour aider à la planification et au bon déroullement du décommissionnement.

Notes:

- Chaque partie de ce programme peut constituer une formation approfondie en une journée.
- Symboles:
    - 🧑‍🏫 = explication / démonstration par le formateur
    - 🙋‍♂️ = échange avec tou·te·s les participant·e·s
    - 💻 = exercice pratique individuel ou par petit groupe
    - 🌟 = retour d’expérience / pro-tip / introduction d’un

# À qui est destinée cette formation ?

Cette formation s’adresse aux dévs et tech leads qui:

- ne se sentent plus suffisamment en maîtrise de leur application (web ou autre) en Node.js;
- et/ou reprennent le développement d’une codebase historique (legacy) en Node.js.

# Prérequis

## Compétences requises

- Comprendre les bases de la programmation orientée objet (POO): classes, méthodes, héritage, polymorphisme.
- Comprendre le fonctionnement de base du Web: requêtes HTTP, différence entre les verbes GET et POST, codes de statut employés dans les réponses, passage et récupération de paramètres de requête, passage de contenu via le corps de requête, récupération de contenu depuis le corps de la réponse.
- Maîtriser les bases de la programmation JavaScript moderne et Node.js: types standard, appel et définition de fonctions, appel et définition de fonctions asynchrones basées sur le passage de `callback`, usage et définition de `Promise`, gestion et analyse d’erreurs (classe `Error`, `throw`, `try`-`catch`), importation de modules internes et externes (via `npm`).

## Matériel requis

- Un ordinateur portable en bon état de fonctionnement, capable de se connecter à Internet par WiFi.
- Un IDE compatible avec les langages JavaScript, TypeScript, et intégrant les erreurs rapportées par les outils `tsc` (analyseur TypeScript) et `eslint`. ⇒ Nous allons utiliser VSCode. (gratuit)
- Un environnement prêt à executer des commandes shell de type `bash` ou `zsh`. (c’est le cas sous Linux et MacOS, mais nécessite l’installation de WSL sous Windows)
- De quoi prendre des notes, que ce soit sur machine ou papier.

Note: nous n’aurons pas le temps de préparer votre environnement ni d’installer ces logiciels, donc veillez à le faire avant la formation.

# Inspiration / references / notes

- Formation de Christophe Porteneuve: [Formation TypeScript • Delicious Insights](https://delicious-insights.com/fr/formations/typescript/)