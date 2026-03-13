# ***🚀 TECH MY CERT***

### 🧠 Présentation du projet

**TECH MY CERT** est un portail éducatif développé avec **Symfony**, pensé comme une plateforme technique évolutive offrant une expérience 100 % orientée framework et bonnes pratiques.

L’objectif du projet est de mettre en œuvre, consolider et approfondir les compétences nécessaires à la réalisation d’une plateforme moderne, robuste et scalable.

--

***La plateforme propose :***

- 📚 **Cours techniques**
- 📊 **Suivi de progression**
- 📝 **Quiz**
- ⚡ Autres fonctionnalités à développer progressivement

### ***🛠️ Stack technique***

| Technologie        | Version / Notes |
|-------------------|----------------|
| 🐘 PHP            | 8.3            |
| ⚡ Symfony        | 7.4.5          |
| 🗄️ Doctrine ORM   | ✅             |
| 🌐 Twig           | ✅             |
| 🛠️ API Platform   | Prévu          |
| 🔑 JWT / Auth     | Prévue         |
| 🐬 MySQL 8        |                |
| 🐳 Docker          |                |
| 📦 Docker Compose |                |

--

### 📦 Prérequis :

Les outils suivants doivent être installés sur la machine hôte :

- 🐳 **Docker** (version minimale recommandée : 24+)
- 📦 **Docker Compose**


### ***🐳 Architecture Docker***

| Service           | Description                           | Port       |
|------------------|---------------------------------------|-----------|
| `php`             | Application Symfony                   | 8000      |
| `db`              | Base de données MySQL 8               | 3306      |
| `adminer`         | Interface web de gestion de la base   | 8080      |

--

### 🚀 Installation et lancement du projet

1️⃣ Cloner le dépôt

```bash
git clone (https://github.com/calabaria/TechMyCert.git)
cd repot directory (TechMyCert)
```
2️⃣ Créer le fichier d’environnement

Créer un fichier .env.local à la racine du projet :

```bash
cp .env .env.local
```
Adapter les variables si nécessaire (base de données, secrets, etc.).

3️⃣ Lancer les conteneurs Docker

```bash
docker compose up -d
```

4️⃣ Installer les dépendances PHP

```bash
docker compose exec php
composer install
```

5️⃣ Lancer les migrations Doctrine

```bash
docker compose exec php
php bin/console doctrine:migrations:migrate
```

6️⃣ Charger les fixtures

```bash
docker compose exec php
php bin/console doctrine:fixtures:load
```

>⚠️ Attention : cette commande supprime les données existantes avant de les recréer.

--

### 🌐 Accès aux services :

🌐 Application Symfony : http://localhost:8000  

🌐 Adminer (gestion de la base de données) : http://localhost:8080

### 🛠️Paramètres de connexion Adminer :

```bash
Système : MySQL
Serveur : db
Base de données : techmycert
Utilisateur : symfony
Mot de passe : symfony
```

--

### 📂 Workflow de développement

* 🔀 Toute évolution passe par une Pull Request
* ❌ Aucun push direct sur la branche main
* ✅ Respect strict des bonnes pratiques Symfony

Structure pensée pour faciliter l’ajout futur de :

* 🛠️ API Platform
* 🔑 Authentification JWT
* 🧪 Tests automatisés
* ⚡ CI/CD

### 📈 Évolutions prévues

* 🌐 API REST avec API Platform
* 🔑 Authentification et sécurisation via JWT
* 👥 Gestion avancée des rôles utilisateurs
* 📝 Système de quiz et scoring
* 📊 Suivi détaillé de la progression utilisateur
* 🧪 Tests automatisés (unitaires et fonctionnels)
* ⚡ Mise en place d’un pipeline CI/CD

### 👤 Auteur

Projet conçu et développé par Radouane Fettal,
dans un objectif de montée en compétence, de professionnalisation et de maîtrise avancée de l’écosystème Symfony.

### 📄 Licence

Projet privé — usage personnel et pédagogique.
