---
ressource:
  - 🛠️ Outil
relates: []
---
### Tester le build en local  
  
Si vous rencontre un problème sur la CI, que vous ne rencontrez pas en local, il est possible d'investiguer avec la   
procédure suivante. En ligne de commande :  
  
```shell  
docker build .
```  
  
On s'attend que le build échoue à un moment, car c'est ce qu'il se passe sur la CI, mais cela crée tout de même iune image.  
  
```shell  
# Récupérer les images, dont la dernière buildée  
docker images  
# Démarrer une conteneur sur l'image, en lançant un shell  
docker run --rm -it --entrypoint sh <IMAGE_ID>  
```  
  
Vous entrez en invite de commande sur l'image docker.  
On peut exécuter le build identique à la CI, mais ce n'est pas nécessaire les rapports de tests sont déjà présente  
  
```shell  
# Lancer le build iso CI  
mvn -s /maven/settings.xml -B org.jacoco:jacoco-maven-plugin:prepare-agent verify org.jacoco:jacoco-maven-plugin:report sonar:sonar -Dsonar.skip=$MDM_SONAR_SKIP ${SONAR_OPTS}  
```  
  
#### Récupérer les diff des pdfs ou des images générées   
  
Une fois que vous avez démarré un container avec l'image qui échoue aiu build de la CI (cf. ci-dessus), vous   
exécutez les commandes suivantes dans une autre invite de commande.  
  
```shell  
# Récupération de l'id du Container démarré  
docker ps  
# Copie des fichiers depuis le container, vers un répertoire local  
docker cp <ID_CONTAINER>:src/test/resources/editions/parcels/ ./local-folder  
```