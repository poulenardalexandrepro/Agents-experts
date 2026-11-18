# Étape 1 · Tri des 24 cartes

Pour chaque tâche, indiquez **qui** la réalise dans le nouveau cycle :

- **H** = le développeur (humain)
- **A** = un agent IA
- **CI** = l'automatisation (GitHub Actions)

Remplissez la colonne « Ma réponse », faites un commit, **puis seulement** ouvrez [le corrigé](../corriges/01-tri-cartes.md) et comptez vos erreurs.

| # | Tâche | Ma réponse |
|---|---|---|
| 1 | Analyser le code avec CodeQL | CI |
| 2 | Rédiger les critères d'acceptation | H |
| 3 | Proposer un plan technique | A |
| 4 | Fusionner la PR | H |
| 5 | Lancer les tests sur chaque PR | CI |
| 6 | Coder la tâche sur une branche | A |
| 7 | Choisir l'agent et le modèle | H |
| 8 | Signaler une faille |❌ H -> A|
| 9 | Détecter un secret dans le code | ❌A -> CI |
| 10 | Écrire le test d'acceptation | H |
| 11 | Reformuler le besoin en issue | A |
| 12 | Bloquer la fusion sans approbation | CI |
| 13 | Expliquer le code à l'oral | H |
| 14 | Découper le plan en tâches | ❌CI -> A |
| 15 | Vérifier les dépendances | ❌A -> CI |
| 16 | Approuver ou refuser la PR | H |
| 17 | Écrire les tests manquants | A |
| 18 | Exécuter le workflow tests.yml | CI |
| 19 | Valider le plan technique | H |
| 20 | Ouvrir la PR en brouillon | ❌CI -> A |
| 21 | Afficher le statut des vérifications | CI |
| 22 | Protéger la branche main | H |
| 23 | Proposer une règle pour AGENTS.md | A |
| 24 | Refuser une PR dont un test échoue | CI |

**Mon nombre d'erreurs : …** (je valide avec 3 erreurs au plus)
