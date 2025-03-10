# Rapport Final 
## Étape de développement et choix technique 
### [BACKEND](https://github.com/Yves-Shaheem/NoGas_BE):
* TypeScript
* Express 
* bcrypt
* jsonwebtoken
* firebase-admin
* firebase
1. Structure du server express js.
2. Connexion à la base de données
3. CRUD + TEST
4. Emailling system + TEST
5. Ajustement 
### [FRONTEND](https://github.com/Yves-Shaheem/NoGas_FE):
* TypeScript 
* Next.js
* Tailwind CSS
1. Structure de server Next js. 
2. Squelette des pages + style 
3. Connexion au BACKEND 
4. Test 
5. Ajustement 
### DATABASE:
* FireStore Firebase
* noSQL document database
1. Création d'un projet Firebase 
2. Choisir la base de données FireBase 
3. Création d'une clé SDK admin 
### [IDO](https://github.com/Yves-Shaheem/NoGas_IDO):
* raspberry-pi 
* open-ssh
* mosquitto 
* python3 

## Analyse des défis rencontrés et solutions mises en place
**Firestore free quota limit atteint trop fréquemment**
Causé par une trop grand nombre de read & writes, donc,  éviter les boucles et réduire le temps de rafraichissement des données dans le frontend

**L'endpoint d'ajout d'un contact est une vulnérabilité sur la sécurité, n'importe qui peut ajouter des contacts à  un utilisateur**
Sécuriser la route avec vérification du JWT. Pour ajouter un contact à un utilisateur, le compte doit être fait, puis ensuite on ajoute ses contacts avec son JWT.

**L'endpoint pour envoyer des emails n'est pas protégé**
N'importe quel utilisateur connecté pouvait manipuler l'envoi de emails, la solution était de vérifier que le JWT appartient à un administrateur

## Résultats des tests
| ![image](![upload_1696b11d17c98ad695d1a29a17e98342](https://github.com/user-attachments/assets/031bb4c0-9adc-4d26-a735-52087693ea24)) |
|:--:| 
| *frontend* |

| ![image](![upload_bfe6f6bf4ff4a5caf469320008047f98](https://github.com/user-attachments/assets/1f43c2c4-9176-4687-ad48-306066a67dc2)) |
|:--:| 
| *backend* | 

## Évaluations finales
L'application web Nogas contient la majorité des fonctionnalitées principales que nous avons envisonné. Si le temps nous permettez, voici quelques améliorations que nous auront aimé ajouter à l'application

- Ajout d'un panneau administrateur pour ajouter plus de fonctionnalités au rôle admin
- Envoi de message d'urgence au contacts d'urgence via leurs téléphone avec SMS
- 2FA pour augmenté la sécurité
- Vérifier l'email de l'utilisateur pour la création d'un compte
- Plus d'information sur la qualité de l'air (azote, humidité, etc..)
- Un graphique représentant l'historique des informations collectées par les capteurs
- Page contact
