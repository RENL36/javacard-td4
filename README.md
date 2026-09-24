Projet de Java Card.
-> L'objectif est de développer et tester une applet Java Card capable de recevoir des commandes APDU et de retourner le message Hello World.

Structure
src/ → Code source Java Card 
scripts/ → Compilation et tests 
tests/ → Tests APDU 
lib/ → Dépendances 
Dockerfile → Environnement Docker

Prérequis
* Java 17
* Java Card Development Kit 2.2.2
* Docker (optionnel)

Compilation 
./scripts/build.sh
Le script compile l'applet et génère le fichier .cap.

Tests
./scripts/run_tests.sh
Les tests utilisent CREF et APDUTool pour simuler une carte Java Card et envoyer les commandes APDU.

Docker
* Construire l'image :
-> docker build -t javacard-td4 .

* Puis lancer le conteneur :
-> docker run --rm -it javacard-td4
