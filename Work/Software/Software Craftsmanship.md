

[[Clean Code]]
[[Test Driven Development]]
[[Behavior-Driven Development]]
[[Domain Driven Design]]

## Questions classiques 

- Dans quel cas on propose une architecture Hexa / Oinion ?
	- µService
	- Echelle + scale des optim's
- Comment on teste un système à plusieurs composants ?
	- Isolation vs Intégré 
		- Docker compose
	- Tout tester vs Smoke tests
	- tester en prod
		- Vérifier CA après chaque release
		- => Observabilité
	- Tester lib vs contrat
		- lib : si on veut tester notre service


#Craft