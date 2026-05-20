[中文版本 →](../../../zh/projects/project-01-baseline-vs-minimal-harness/)

> Leçons liées : [Leçon 01. Les modèles forts ne garantissent pas une exécution fiable](./../../lectures/lecture-01-why-capable-agents-still-fail/index.md) · [Leçon 02. Ce que signifie vraiment harness](./../../lectures/lecture-02-what-a-harness-actually-is/index.md)
> Fichiers modèles : [templates/](https://github.com/walkinglabs/learn-harness-engineering/blob/main/docs/fr/resources/templates/)

# Projet 01. Prompt seul vs règles d'abord : quelle différence cela fait-il ?

## Ce que vous faites

Construisez le squelette minimal d'une application Electron de base de connaissances : une fenêtre avec une liste de documents à gauche, un panneau Q&A à droite et un dossier de données local. La tâche elle-même n'est pas complexe. Ce qui est complexe, c'est la manière de faire en sorte que l'agent la termine.

Vous l'exécutez deux fois. Première fois : seulement un prompt, sans préparation. Deuxième fois : `AGENTS.md`, `init.sh` et `feature_list.json` déjà placés dans le dépôt. Ensuite, comparez.

Ce scénario de cours prend un court intervalle de redécouverte/préparation comme exemple, pas un résultat mesuré fixe.

## Outils

- Claude Code ou Codex (choisissez-en un et gardez-le pour les deux exécutions)
- Git (gérer les branches et comparer)
- Node.js + Electron (stack du projet)
- Un minuteur (noter la durée de chaque exécution)

## Mécanisme de harness

Harness minimal : `AGENTS.md` + `init.sh` + `feature_list.json`

## Utiliser le projet fourni dans le dépôt

Chemin dans le dépôt : `projects/project-01/`

| Dossier | Ce qu’il contient | Comment l’utiliser |
|------|------|------|
| `starter/` | Exécution « harness faible ». Contient uniquement `task-prompt.md` comme description de la tâche, sans `AGENTS.md` ni `feature_list.json`. | Donne le prompt à ton agent et mesure ce qu’il termine sans structure supplémentaire. |
| `solution/` | Le même slice produit avec des artefacts de harness explicites : `AGENTS.md`, `CLAUDE.md`, `init.sh`, `feature_list.json` et `claude-progress.md`. | Compare comment les règles et la vérification rendent la même tâche concrète et vérifiable. |

Les quatre fonctionnalités concrètes sont : ouverture de la fenêtre, liste de documents, panneau de questions, et création du répertoire de données local. Consulte `solution/feature_list.json` pour l’évidence attendue pour chaque fonctionnalité.
