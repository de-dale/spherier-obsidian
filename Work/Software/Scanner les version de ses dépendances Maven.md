#maven

**💡Quelques commande #maven pour scan versions dépendances depuis les propriétés**

```
versions:display-dependency-updates
```
analyse les dépendances d'un projet et produit un rapport sur les dépendances pour lesquelles des versions plus récentes sont disponibles.

```
versions:display-plugin-updates
```
analyse les plugins d'un projet et produit un rapport sur les plugins qui ont des versions plus récentes disponibles, en tenant compte des prérequis de version de Maven.

```
versions:display-property-updates
```
analyse un projet et produit un rapport sur les propriétés qui sont utilisées pour contrôler les versions des artefacts et sur les propriétés pour lesquelles des versions plus récentes sont disponibles ([documentation](https://www.mojohaus.org/versions/versions-maven-plugin/display-property-updates-mojo.html "https://www.mojohaus.org/versions/versions-maven-plugin/display-property-updates-mojo.html")).