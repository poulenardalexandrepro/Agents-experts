# Agents personnalisés

Chaque agent expert est décrit dans un fichier `nom-de-l-agent.agent.md` placé dans ce dossier. Copilot les propose ensuite dans le menu des agents (VS Code, github.com, Copilot CLI).

Structure d'un fichier :

```markdown
---
name: nom-de-l-agent
description: Une phrase qui dit quand utiliser cet agent
tools: ['read', 'search']
model: nom exact recopié depuis le sélecteur de modèles de Copilot
---
Les consignes de l'agent, en français : son rôle, ce qu'il ne doit jamais
faire, le format de sa réponse.
```

À l'étape 3, créez ici `relecteur-securite.agent.md` et `testeur.agent.md`, puis vérifiez-les avec [la liste « un bon agent »](../../exercices/03-liste-bon-agent.md).
