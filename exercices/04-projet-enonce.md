# Étape 4 · Projet : une fonctionnalité, deux agents, une décision

Vous faites réaliser **la même fonctionnalité** par deux agents (ou deux modèles), vous relisez les deux pull requests, vous en fusionnez **une seule** et vous justifiez votre choix.

## Choisir une fonctionnalité

Toutes portent sur le catalogue de BiblioTech (tables `livres` et `categories`).

| Fonctionnalité | Ce qu'on attend |
|---|---|
| Recherche multicritère | Filtrer le catalogue par titre, auteur, catégorie, année et disponibilité, combinables |
| Export CSV du catalogue | Télécharger la liste des livres (titre, auteur, année, catégorie, disponibilité) au format CSV |
| Statistiques du catalogue | Une page qui affiche le nombre de livres par catégorie et le nombre de livres disponibles |
| Tri et pagination | Trier le catalogue par titre ou par année, 12 livres par page |
| Badge « Nouveauté » | Signaler les livres ajoutés depuis moins de 30 jours, sur la liste et sur la fiche |

## Les 7 jalons

**A — Préparer**
- Mettez en place la CI : copiez [modele-tests.yml](modele-tests.yml) dans `.github/workflows/tests.yml`, faites un commit, puis vérifiez que le workflow « Tests BiblioTech » est vert dans l'onglet **Actions**.
- **Settings → Branches → Add rule** sur `main` : pull request obligatoire avant fusion, vérifications « Tests (socle + parcours) » requises.

**B — Rédiger l'issue**
- **Issues → New issue → Tâche pour agent**. Au moins 3 critères d'acceptation.
- Vérifiez-la avec [la liste « une bonne issue »](05-liste-bonne-issue.md).

**C — Écrire le test d'acceptation**
- Créez `projetLaravel/tests/Feature/Parcours/MaFonctionnaliteTest.php` avec l'attribut `#[Group('parcours')]`.
- Lancez `php artisan test --group=parcours` : le test doit **échouer**. C'est normal : la fonctionnalité n'existe pas encore.

**D — Déléguer à deux agents**
- Agent 1 : assignez l'issue à **Copilot** (coding agent).
- Agent 2 : mode agent de VS Code avec un **autre modèle**, sur une autre branche (ou Claude / Codex si votre abonnement le permet).
- Suivez les journaux. Notez quel agent et quel modèle vous avez utilisés.

**E — Relire les deux PR**
- Remplissez [la grille de revue](06-grille-revue-pr.md) pour chacune.
- Recadrez au moins une fois par un commentaire (`@copilot …`).

**F — Décider**
- Fusionnez une PR. Fermez l'autre avec un commentaire qui justifie votre choix (au moins 3 arguments tirés de la grille).

**G — Capitaliser**
- Ajoutez 2 règles apprises dans la section « Règles apprises » d'AGENTS.md.

## Ma justification (jalon F)

| Critère | PR agent 1 | PR agent 2 |
|---|---|---|
| Agent et modèle | | |
| Critères couverts | | |
| Qualité des tests | | |
| Fichiers hors périmètre | | |
| Problèmes de sécurité | | |
| Nombre de recadrages | | |

**Mon choix et pourquoi :** …
