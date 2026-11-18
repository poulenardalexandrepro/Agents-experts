# Corrigé · Les sept agents experts

| Agent | Étape | Il fait | Il ne fait pas | Outils | Modèle |
|---|---|---|---|---|---|
| Analyste besoin | 1 · Spécifier | Reformule un besoin flou en issue, propose des critères testables | N'écrit pas de code, ne fixe pas le périmètre | read, search | Polyvalent |
| Architecte | 2 · Planifier | Analyse le code, propose un plan (fichiers, routes, tests) | Ne modifie aucun fichier, n'arbitre pas | read, search | Raisonnement |
| Planificateur | 3 · Découper | Découpe le plan en tâches indépendantes, repère les tâches parallélisables | N'écrit pas les tests d'acceptation | read, search | Polyvalent |
| Développeur | 5 · Implémenter | Code dans un environnement isolé, lance les tests, ouvre une PR | Ne fusionne jamais, ne sort pas du périmètre | read, search, edit, terminal | Polyvalent |
| Testeur | 6 · Tester | Écrit un test par critère, signale les critères non couverts | Ne modifie pas le code de l'application, n'affaiblit aucun test | read, search, edit (limité à tests/) | Polyvalent |
| Relecteur sécurité | 7 · Revue | Cherche injections, accès, secrets ; classe bloquant ou mineur | Ne corrige rien, ne remplace pas la revue humaine | read, search | Raisonnement |
| Documentaliste | 8 · Capitaliser | Met à jour README et AGENTS.md, transforme une erreur en règle | Ne touche pas au code, ne fusionne pas sans relecture | read, edit | Rapide |

L'étape 4 (déléguer) n'a pas d'agent : c'est le développeur qui choisit et lance.
