#ContrainteKata [[Contraintes de kata]]

🌶️Toutes méthode (autres que les constructeurs) ne doit accepter que classes comme argument et pas de primitive. Les nombres, les chaînes de caractères, etc. ne sont pas autorisés, même en utilisant les “classes primitives” de Java (Integer, Boolean, String, etc.).

🌶️🌶️ Aucune fonction ne doit renvoyer de valeur primitive, pas même les lambdas

> **No Primitives**: All methods (other than constructors) must take classes as arguments. Bare integers, strings, etc are not permitted. Advanced: Try to avoid any primitives as return values (This makes predicate test methods more challenging!)