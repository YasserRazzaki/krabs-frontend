Bienvenue dans le front-end du projet Le Krabs ! 🦀

Partie front-end du projet Le Krabs, réalisée avec Angular dans le cadre de notre projet de recherche de Master 1 Informatique à l'Université de Montpellier.

Cette application web communique avec l'API Symfony afin d'accéder aux fonctionnalités et aux données de l'application.

🚀 Prérequis

Avant de commencer, assurez-vous d'avoir installé les outils suivants :

Node.js : version 18 ou supérieure, ou version 20.
npm : généralement installé avec Node.js.
Angular CLI : accessible localement via les dépendances du projet ou installé globalement.

Pour vérifier les versions installées, exécutez les commandes suivantes :

bash
node -v
npm -v

🛠️ Installation
1. Installer les dépendances

Depuis la racine du dossier front/, exécutez :

bash
npm install


Cette commande installe les dépendances définies dans le fichier package.json.

2. Vérifier l'utilisation d'Angular CLI

Pour éviter les conflits avec des commandes système, il est recommandé d'utiliser le CLI local du projet avec npx.

Pour démarrer l'application, exécutez :

bash
npx ng serve


Vous pouvez également utiliser le script npm défini dans package.json :

bash
npm start


Remarque : si la commande ng lance un autre programme, comme l'éditeur système mg sous Ubuntu, privilégiez npx ng serve ou npm start.

Si vous souhaitez désinstaller le paquet système mg et que vous êtes certain de ne pas en avoir besoin, exécutez :

bash
sudo apt remove mg


Cette désinstallation est facultative et n'est pas nécessaire si npx ng serve fonctionne correctement.

⚡ Démarrage de l'application

Depuis la racine du dossier front/, lancez le serveur de développement Angular :

bash
npx ng serve


Par défaut, l'application est accessible à l'adresse suivante :

http://localhost:4200

Pour démarrer le serveur et ouvrir automatiquement l'application dans votre navigateur, utilisez :

bash
npx ng serve --open


Le serveur de développement surveille les modifications des fichiers et recompile généralement l'application automatiquement.

🔗 Connexion avec le back-end Symfony

Le front-end Angular communique avec l'API Symfony, généralement accessible à l'adresse suivante :

http://localhost:8000

L'URL de l'API peut être configurée dans les fichiers d'environnement Angular, notamment environment.ts, selon l'organisation du projet.

Pour assurer le bon fonctionnement de la communication entre les deux parties, vérifiez que :

Le serveur Symfony est démarré.
L'URL de l'API configurée dans Angular est correcte.
La configuration CORS du back-end autorise l'origine http://localhost:4200.
Les routes et les mécanismes d'authentification JWT correspondent à ceux exposés par l'API.
Résolution des erreurs CORS

Si le navigateur affiche une erreur CORS, procédez aux vérifications suivantes :

Vérifiez la variable CORS_ALLOW_ORIGIN dans le fichier .env.local du back-end.
Vérifiez que l'origine Angular est autorisée par la configuration CORS de Symfony.
Redémarrez le serveur back-end après toute modification de configuration si nécessaire.
Consultez la console du navigateur pour identifier l'origine exacte de l'erreur.
📝 Résolution des problèmes
1. Erreur lors de l'installation des dépendances

Si la commande npm install échoue :

Vérifiez votre version de Node.js.
Vérifiez votre connexion Internet.
Consultez les messages d'erreur affichés dans le terminal.
Si le projet contient un fichier package-lock.json, vous pouvez utiliser npm ci pour effectuer une installation reproductible à partir des dépendances verrouillées.
bash
npm ci


Attention : cette commande remplace le dossier node_modules et nécessite un fichier package-lock.json cohérent avec package.json`.

2. La commande ng ne fonctionne pas

Utilisez le CLI local du projet :

bash
npx ng serve


Vous pouvez également démarrer l'application via le script npm :

bash
npm start

3. Le front-end ne parvient pas à contacter l'API

Si les requêtes vers le back-end échouent, vérifiez les points suivants :

Le serveur Symfony fonctionne sur http://localhost:8000.
L'URL de l'API est correctement renseignée dans la configuration Angular.
La configuration CORS du back-end autorise les requêtes provenant du front-end.
Les erreurs réseau sont consultables dans les outils de développement du navigateur.
📁 Structure indicative du projet

Voici un exemple de structure courante pour une application Angular :

text
front/
├── src/
│   ├── app/
│   ├── assets/
│   ├── environments/
│   ├── index.html
│   └── main.ts
├── angular.json
├── package.json
├── package-lock.json
└── README.md


La structure exacte peut varier selon la version d'Angular et l'organisation du projet.

✅ Résumé des commandes

Voici les principales commandes à retenir pour installer et démarrer le front-end.

bash
# Vérifier les versions de Node.js et npm
node -v
npm -v

# Installer les dépendances
npm install

# Démarrer l'application Angular
npx ng serve

# Démarrer et ouvrir automatiquement le navigateur
npx ng serve --open

# Alternative via le script npm
npm start


URL du front-end : http://localhost:4200

URL du back-end : http://localhost:8000

Front-end Le Krabs — Master 1 Informatique, Université de Montpellier.