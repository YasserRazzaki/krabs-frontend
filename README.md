# Bienvenue dans la partie Front-end du projet Krabs !
Partie Front-end du projet "Le Krabs" de notre Projet de Recherche M1 Informatique à l'Université de Montpellier réalisée avec Angular.

Application web front-end du projet Karabs, développée avec Angular. Elle communique avec l'API Symfony pour accéder aux fonctionnalités et aux données de l'application.

🚀 Prérequis

Avant de commencer, assurez-vous d'avoir installé les outils suivants :

Node.js : version 18 ou supérieure, ou version 20.
npm, généralement installé avec Node.js.
Angular CLI, accessible localement via les dépendances du projet ou installé globalement.

Pour vérifier les versions installées :

bash
node -v
npm -v

🛠️ Installation
1. Installer les dépendances

Depuis la racine du dossier front/, exécutez :

bash
npm install


Cette commande installe les dépendances définies dans package.json.

2. Vérifier l'utilisation d'Angular CLI

Pour éviter les conflits avec des commandes système, il est recommandé d'utiliser le CLI local du projet avec npx.

Démarrez l'application avec :

bash
npx ng serve


Vous pouvez également utiliser le script npm défini dans package.json :

bash
npm start

Si la commande ng lance un autre programme, comme l'éditeur système mg sous Ubuntu, privilégiez npx ng serve ou npm start.

Si vous souhaitez désinstaller le paquet système mg et que vous êtes certain de ne pas en avoir besoin :

bash
sudo apt remove mg


Cette désinstallation est facultative : elle n'est pas nécessaire si npx ng serve fonctionne correctement.

⚡ Démarrage de l'application

Depuis le dossier front/, lancez :

bash
npx ng serve


Par défaut, l'application Angular est accessible à l'adresse suivante :

http://localhost:4200

Pour démarrer le serveur et ouvrir automatiquement le navigateur :

bash
npx ng serve --open


Le serveur de développement surveille les modifications des fichiers et recompile généralement l'application automatiquement.

🔗 Connexion avec le back-end Symfony

Le front-end communique avec l'API Symfony, généralement accessible à l'adresse :

http://localhost:8000

L'URL de l'API peut être configurée dans les fichiers d'environnement Angular, notamment environment.ts, selon l'organisation du projet.

Vérifiez que :

Le serveur Symfony est démarré.
L'URL de l'API configurée dans Angular est correcte.
La configuration CORS du back-end autorise l'origine http://localhost:4200.
Les routes et les mécanismes d'authentification JWT correspondent à ceux exposés par l'API.
Résolution des erreurs CORS

Si le navigateur affiche une erreur CORS :

Vérifiez la variable CORS_ALLOW_ORIGIN dans le fichier .env.local du back-end.
Vérifiez que l'origine Angular est autorisée par la configuration CORS de Symfony.
Redémarrez le serveur back-end après toute modification de configuration si nécessaire.
Consultez la console du navigateur pour identifier l'origine exacte de l'erreur.
📝 Résolution des problèmes
Erreur lors de l'installation des dépendances

Si npm install échoue :

Vérifiez votre version de Node.js.
Vérifiez votre connexion Internet.
Consultez les messages d'erreur affichés dans le terminal.
Si le projet utilise un fichier package-lock.json, privilégiez npm ci lorsque vous souhaitez une installation reproductible à partir du verrouillage des dépendances.
La commande ng ne fonctionne pas

Utilisez le CLI local :

bash
npx ng serve


Ou exécutez le script npm :

bash
npm start

Le front-end ne parvient pas à contacter l'API

Vérifiez que le back-end fonctionne sur http://localhost:8000 et que l'URL de l'API est correctement renseignée dans la configuration Angular.

Si nécessaire, vérifiez également les erreurs réseau dans les outils de développement du navigateur.

La structure exacte peut varier selon la version d'Angular et l'organisation du projet.

✅ Résumé des commandes
bash
# Installer les dépendances
npm install

# Démarrer l'application Angular
npx ng serve

# Alternative via le script npm
npm start


L'application sera accessible sur http://localhost:4200, à condition que le port soit disponible.