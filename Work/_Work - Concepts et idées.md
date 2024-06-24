---
ressource: []
---

# Idées

```dataview
list
FROM "Work"
WHERE contains(ressource, "Idée") OR contains(ressource, "Pensée")
SORT file.name
```
# Concepts
```dataview
list
FROM "Work"
WHERE contains(ressource, "Concept")
SORT file.name
```
