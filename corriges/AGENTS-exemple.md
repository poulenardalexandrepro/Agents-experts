# AGENTS.md — BiblioTech (exemple de corrigé)

## Le projet
BiblioTech est l'application de catalogue de la médiathèque : les usagers consultent et recherchent les livres, l'équipe de la médiathèque fait évoluer le catalogue.

## Pile technique
Laravel, PHP 8.4, MySQL 8.4. L'application est dans le dossier `projetLaravel/`.

## Commandes
- Installer les dépendances : `cd projetLaravel && composer install`
- Lancer les tests : `php artisan test --group=socle,parcours`
- Lancer l'application : `php artisan serve`

## Règles du projet
- Toute nouvelle route a au moins un test Feature, dans `tests/Feature/Parcours/`, avec `#[Group('parcours')]`.
- Les requêtes passent par Eloquent ou des requêtes préparées : jamais de SQL concaténé avec une saisie utilisateur.
- Une migration déjà poussée n'est jamais modifiée : on en crée une nouvelle.
- Les noms de classes, de routes et de vues suivent les conventions déjà présentes (en français).

## À ne jamais faire
- Modifier un test existant pour le faire passer.
- Ajouter une dépendance Composer ou npm sans le signaler dans la PR.
- Écrire un secret (mot de passe, clé) dans le code : il va dans `.env`.

## Règles apprises
<!-- Exemple : « Toute page qui liste des livres reste paginée. » -->
