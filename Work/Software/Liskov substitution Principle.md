---
ressource:
  - 🧠 Concept
aliases:
  - LSP
relates:
  - "[[SOLID]]"
---
> Let q(x) be a property provable about objects of x of type T.  
> Then q(y) should be provable for objects y of type S where S is a subtype of T.  
  
>Every subclass/derived class should be substitutable for their base/parent class  
  
#### Smells  
You have to check for the type provided (e.g. instanceof)

#### Consequences
Preconditions cannot be strengthened in a subtype  
Postconditions cannot be weakened in a subtype  
Invariants of the supertype must be preserved in a subtype  
Exceptions Should Be Stricter

# 🔗 Ressources
- http://principles-wiki.net/principles:liskov_substitution_principle