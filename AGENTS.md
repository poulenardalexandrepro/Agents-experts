# AGENTS.md — BiblioTech
## Le projet

BiblioTech est une application web de gestion et de consultation d’un catalogue de livres destinée aux bibliothèques ou aux établissements souhaitant centraliser leurs ouvrages. Elle permet notamment de gérer les livres et leurs catégories. Les données fournies dans le projet sont fictives : aucune donnée personnelle réelle ne doit être utilisée ou envoyée à un agent IA.

## Pile technique

- Framework : Laravel 13
- Langage : PHP 8.4 dans Docker (PHP ^8.3 requis par Composer)
- Base de données : MySQL 8.4
- Interface locale : phpMyAdmin sur le port 8080
- Frontend : Vite 8, Tailwind CSS 4 et JavaScript de type module
- Gestion des dépendances PHP : Composer 2
- Gestion des dépendances frontend : npm
- Dossier de l’application : `projetLaravel/`
- Point d’entrée web : `projetLaravel/public/`
- Conteneurs : Docker Compose, avec les services `app`, `mysql` et `phpmyadmin`

## Commandes

À exécuter depuis la racine du dépôt, sauf indication contraire.

- Installer et initialiser l’application : `docker compose exec app composer run setup`
- Installer les dépendances PHP : `cd projetLaravel && composer install`
- Installer les dépendances frontend : `cd projetLaravel && npm install`
- Lancer les tests : `cd projetLaravel && php artisan test`
- Lancer uniquement les tests du parcours : `cd projetLaravel && php artisan test --group=parcours`
- Lancer l’application : `docker compose up -d` puis ouvrir `http://localhost:8000`
- Accéder à phpMyAdmin : ouvrir `http://localhost:8080`
- Construire les assets : `cd projetLaravel && npm run build`
- Formater le code PHP : `cd projetLaravel && ./vendor/bin/pint`

## Règles du projet

- Tout changement fonctionnel doit être couvert par un test automatisé pertinent, idéalement un test PHPUnit Feature ou un test d’acceptation dans `projetLaravel/tests/Feature/Parcours/` pour une fonctionnalité du parcours.
- Le code PHP doit respecter les conventions Laravel et PSR-4 ; nommer les modèles, contrôleurs, migrations, routes et tests avec des noms explicites au singulier ou au pluriel selon les conventions Laravel.
- Les modèles du domaine sont principalement liés aux tables `livres` et `categories`; toute modification de schéma doit passer par une migration dans `projetLaravel/database/migrations/`.
- Utiliser les helpers, validations, Eloquent, Blade et mécanismes de sécurité propres à Laravel plutôt que du SQL ou du code PHP non contextualisé.
- Valider toutes les données venant de l’utilisateur côté serveur et échapper les sorties Blade par défaut avec `{{ ... }}`.
- Utiliser `php artisan` pour les opérations Laravel et ne modifier ni `vendor/`, ni `node_modules/`, ni les fichiers générés automatiquement.
- Ne garder dans une contribution que les fichiers nécessaires à la fonctionnalité demandée et expliquer clairement les changements dans la PR.
- Toute PR produite par un agent doit indiquer l’agent et le modèle utilisés.

## À ne jamais faire

- Ne jamais committer `.env`, des clés, des mots de passe réels ou des données personnelles réelles.
- Ne jamais modifier directement une base de données ou une migration déjà fusionnée pour masquer une erreur; créer une nouvelle migration corrective.
- Ne jamais désactiver, contourner ou supprimer les tests, la validation, l’authentification ou les protections CSRF pour faire passer une modification.
- Ne jamais fusionner une PR d’agent sans relecture humaine, exécution des tests et vérification du périmètre.
- Ne jamais utiliser `--force` pour écraser des migrations ou des modifications locales sans un besoin explicite dans l’issue.
- Ne jamais ajouter de vrais données personnelles dans les fixtures, tests, captures ou fichiers de démonstration.

## Règles apprises

<!-- Étape 4, jalon G : ajouter ici les règles tirées des erreurs observées lors du projet. -->
