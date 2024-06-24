---
relates:
  - "[[Git]]"
  - "[[Computer Setup]]"
---
### Configuration globale

### Quand on n'a pas le port 22 de disponible (https)
passer par le port 443 (ssh) après avoir ajouté une clé SSH

Générer une clé
```shell
ssh-keygen -t ed25519 -C "your_email@example.com"
```

Déclarer "ssh.github.com" comme hôte connu
```shell
curl -L https://api.github.com/meta \
| grep ssh-rsa \
| awk '{print "ssh.github.com", $2}' >> ~/.ssh/known_hosts

```