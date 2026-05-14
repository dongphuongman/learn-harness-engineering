<p align="center">
  <a href="../../README.md"><img alt="English" src="https://img.shields.io/badge/EN-English-blue?style=flat-square"></a>
  <a href="../zh-CN/README.md"><img alt="简体中文" src="https://img.shields.io/badge/ZH-简体中文-red?style=flat-square"></a>
  <a href="../zh-TW/README.md"><img alt="繁體中文" src="https://img.shields.io/badge/ZH--TW-繁體中文-orange?style=flat-square"></a>
  <a href="../ja-JP/README.md"><img alt="日本語" src="https://img.shields.io/badge/JA-日本語-green?style=flat-square"></a>
  <a href="../ko-KR/README.md"><img alt="한국어" src="https://img.shields.io/badge/KO-한국어-blueviolet?style=flat-square"></a>
  <a href="../es-ES/README.md"><img alt="Español" src="https://img.shields.io/badge/ES-Español-yellow?style=flat-square"></a>
  <a href="../fr-FR/README.md"><img alt="Français" src="https://img.shields.io/badge/FR-Français-007EC6?style=flat-square"></a>
  <a href="https://walkinglabs.github.io/learn-harness-engineering/ru/"><img alt="Русский" src="https://img.shields.io/badge/RU-Русский-informational?style=flat-square"></a>
  <a href="../de-DE/README.md"><img alt="Deutsch" src="https://img.shields.io/badge/DE-Deutsch-2EA043?style=flat-square"></a>
  <a href="../ar-SA/README.md"><img alt="العربية" src="https://img.shields.io/badge/AR-العربية-success?style=flat-square"></a>
  <a href="../vi-VN/README.md"><img alt="Tiếng Việt" src="https://img.shields.io/badge/VI-Tiếng_Việt-cc6699?style=flat-square"></a>
  <a href="https://walkinglabs.github.io/learn-harness-engineering/uz/"><img alt="Oʻzbekcha" src="https://img.shields.io/badge/UZ-Oʻzbekcha-1A8BBA?style=flat-square"></a>
</p>

# Learn Harness Engineering

> **Un cours basé sur des projets consacré à la construction de l'environnement, de la gestion d'état, de la vérification et des mécanismes de contrôle qui permettent aux agents de codage IA de fonctionner de manière fiable.**

Learn Harness Engineering est un cours dédié à l'ingénierie des agents de codage IA. Nous avons étudié et synthétisé en profondeur les théories et pratiques les plus avancées en matière de Harness Engineering dans l'industrie. Nos références principales incluent :

- [OpenAI : Harness engineering : leveraging Codex in an agent-first world](https://openai.com/index/harness-engineering/)
- [Anthropic : Effective harnesses for long-running agents](https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents)
- [Anthropic : Harness design for long-running application development](https://www.anthropic.com/engineering/harness-design-long-running-apps)
- [Awesome Harness Engineering](https://github.com/walkinglabs/awesome-harness-engineering)

> **Démarrage rapide ?** Le skill [`skills/harness-creator/`](../../skills/) peut vous aider à générer un harness de niveau production (AGENTS.md, listes de fonctionnalités, init.sh, flux de vérification) pour votre propre projet en quelques minutes.

---

## Table des Matières

- [Aperçu Visuel](#aperçu-visuel)
- [Ce que signifie réellement Harness Engineering](#ce-que-signifie-réellement-harness-engineering)
- [Démarrage Rapide : Améliorez votre agent dès aujourd'hui](#démarrage-rapide--améliorez-votre-agent-dès-aujourdhui)
- [Projet Final : Une véritable application](#projet-final--une-véritable-application)
- [Parcours d'Apprentissage](#parcours-dapprentissage)
- [Programme d'Études](#programme-détudes)
- [Skills](#skills)
- [Autres Cours](#autres-cours)

---

## Aperçu Visuel

### Page d'Accueil du Cours
> Un plan de cours complet et une introduction aux philosophies fondamentales, offrant un chemin clair pour commencer.

![Aperçu de la page d'accueil du cours](../../docs/public/screenshots/readme/zh-home.png)

### Cours Immersifs
> Des plongées approfondies dans les problèmes concrets et des projets pratiques (comme le Projet 01) pour une expérience d'apprentissage immersive.

![Aperçu des cours](../../docs/public/screenshots/readme/zh-lecture-01.png)

### Bibliothèque de Ressources Prête à l'Emploi
> Des modèles et des configurations de référence conçus pour résoudre les problèmes courants dans le développement d'agents IA multi-tours, tels que la perte de contexte et l'achèvement prématuré des tâches.

![Aperçu de la bibliothèque de ressources](../../docs/public/screenshots/readme/zh-resources.png)

## Livres de Cours en PDF

Le dépôt inclut désormais un pipeline de génération de PDF pour le contenu du cours.

- Exécutez `npm run pdf:build` pour générer les PDF en anglais et en chinois localement.
- Les fichiers de sortie sont écrits dans `artifacts/pdfs/`.
- Exécutez `npm run screenshots:readme` si vous souhaitez mettre à jour les images d'aperçu du README.
- Le workflow GitHub Actions [`release-course-pdfs.yml`](../../.github/workflows/release-course-pdfs.yml) peut construire les PDF et les publier sur les Releases GitHub.

---

## Le modèle est intelligent, le harness le rend fiable

Il y a une dure vérité que la plupart des gens apprennent à leurs dépens : **le modèle le plus puissant au monde échouera toujours sur de vraies tâches d'ingénierie si vous ne construisez pas un environnement approprié autour de lui.**

Vous l'avez probablement constaté vous-même. Vous donnez une tâche à Claude ou GPT dans votre dépôt. Cela commence bien -- il lit des fichiers, écrit du code, semble productif. Puis quelque chose tourne mal. Il saute une étape. Il casse un test. Il dit « terminé » mais rien ne fonctionne vraiment. Vous passez plus de temps à corriger qu si vous l'aviez fait vous-même.

Ce n'est pas un problème de modèle. C'est un problème de harness.

Les preuves sont claires. Anthropic a mené une expérience contrôlée : même modèle (Opus 4.5), même prompt (« construis un éditeur de jeux rétro 2D »). Sans harness, il a dépensé 9 $ en 20 minutes et a produit quelque chose qui ne fonctionnait pas. Avec un harness complet (planificateur + générateur + évaluateur), il a dépensé 200 $ en 6 heures et a construit un jeu auquel on pouvait réellement jouer. Le modèle n'a pas changé. Le harness, oui.

OpenAI a rapporté la même chose avec Codex : dans un dépôt bien équipé d'un harness, le même modèle passe de « peu fiable » à « fiable ». Pas une amélioration marginale -- un changement qualitatif.

**Ce cours vous apprend à construire cet environnement.**

```text
                    THE HARNESS PATTERN
                    ====================

    You --> give task --> Agent reads harness files --> Agent executes
                                                        |
                                              harness governs every step:
                                              |
                                              +--> Instructions: what to do, in what order
                                              +--> Scope:       one feature at a time, no overreach
                                              +--> State:       progress log, feature list, git history
                                              +--> Verification: tests, lint, type-check, smoke runs
                                              +--> Lifecycle:   init at start, clean state at end
                                              |
                                              v
                                         Agent stops only when
                                         verification passes
```

---

## Ce que signifie réellement Harness Engineering

Le Harness Engineering consiste à construire un environnement de travail complet autour du modèle pour qu'il produise des résultats fiables. Il ne s'agit pas d'écrire de meilleurs prompts. Il s'agit de concevoir le système dans lequel le modèle opère.

Un harness comporte cinq sous-systèmes :

```text
    ┌─────────────────────────────────────────────────────────────────┐
    │                        THE HARNESS                              │
    │                                                                 │
    │   ┌──────────────┐  ┌──────────────┐  ┌──────────────────────┐ │
    │   │ Instructions  │  │    State     │  │   Verification       │ │
    │   │              │  │              │  │                      │ │
    │   │ AGENTS.md    │  │ progress.md  │  │ tests + lint         │ │
    │   │ CLAUDE.md    │  │ feature_list │  │ type-check           │ │
    │   │ feature_list │  │ git log      │  │ smoke runs           │ │
    │   │ docs/        │  │ session hand │  │ e2e pipeline         │ │
    │   └──────────────┘  └──────────────┘  └──────────────────────┘ │
    │                                                                 │
    │   ┌──────────────┐  ┌──────────────────────────────────────┐   │
    │   │    Scope     │  │         Session Lifecycle             │   │
    │   │              │  │                                      │   │
    │   │ one feature  │  │ init.sh at start                     │   │
    │   │ at a time   │  │ clean-state checklist at end          │   │
    │   │ definition   │  │ handoff note for next session        │   │
    │   │ of done      │  │ commit only when safe to resume      │   │
    │   └──────────────┘  └──────────────────────────────────────┘   │
    │                                                                 │
    └─────────────────────────────────────────────────────────────────┘

    The MODEL decides what code to write.
    The HARNESS governs when, where, and how it writes it.
    The harness doesn't make the model smarter.
    It makes the model's output reliable.
```

Chaque sous-système a une seule responsabilité :

- **Instructions** -- Indiquent à l'agent ce qu'il doit faire, dans quel ordre, et ce qu'il doit lire avant de commencer. Pas un fichier gigantesque ; une structure à divulgation progressive que l'agent navigue selon ses besoins.
- **State** -- Suivi de ce qui a été fait, de ce qui est en cours et de ce qui reste à faire. Les données sont persistées sur disque pour que la prochaine session reprenne exactement là où la précédente s'est arrêtée.
- **Verification** -- Seul un jeu de tests qui passe constitue une preuve. L'agent ne peut pas déclarer victoire sans une preuve exécutable.
- **Scope** -- Limite l'agent à une seule fonctionnalité à la fois. Pas de surcharge. Pas de trois choses à moitié terminées. Pas de réécriture de la liste de fonctionnalités pour masquer le travail inachevé.
- **Session Lifecycle** -- Initialisation au démarrage. Nettoyage à la fin. Laisser un chemin de redémarrage propre pour la prochaine session.

---

## Pourquoi ce cours existe

La question n'est pas « les modèles peuvent-ils écrire du code ? » Ils le peuvent. La question est : **peuvent-ils accomplir de manière fiable de vraies tâches d'ingénierie dans de vrais dépôts, sur plusieurs sessions, sans supervision humaine constante ?**

Pour l'instant, la réponse est : pas sans un harness.

```text
    WITHOUT HARNESS                          WITH HARNESS
    ==============                          ============

    Session 1: agent writes code            Session 1: agent reads instructions
              agent breaks tests                      agent runs init.sh
              agent says "done"                       agent works on one feature
              you fix it manually                     agent verifies before claiming done
                                                       agent updates progress log
    Session 2: agent starts fresh                    agent commits clean state
              agent has no memory
              of what happened before         Session 2: agent reads progress log
              agent re-does work                       agent picks up exactly where it left off
              or does something else entirely          agent continues the unfinished feature
              you fix it again                         you review, not rescue

    Result: you spend more time                  Result: agent does the work,
            cleaning up than if you                      you verify the result
            did it yourself
```

Les questions auxquelles ce cours s'intéresse réellement :

- Quels modèles de harness améliorent les taux d'achèvement des tâches ?
- Quels modèles réduisent le retravail et les achèvements incorrects ?
- Quels mécanismes maintiennent une progression régulière des tâches de longue durée ?
- Quelles structures gardent le système maintenable après plusieurs exécutions de l'agent ?

---

## Programme d'Études et Documentation

Pour l'ensemble des matériaux du cours, veuillez visiter le **[Site de Documentation](https://walkinglabs.github.io/learn-harness-engineering/)**.

Le programme est divisé en trois parties :

1. **Cours magistraux** : 12 unités conceptuelles expliquant la théorie derrière le Harness Engineering.
2. **Projets** : 6 projets pratiques où vous construisez un espace de travail agentique à partir de zéro.
3. **Bibliothèque de Ressources** : Des modèles prêts à copier (`AGENTS.md`, `feature_list.json`, `init.sh`, etc.) à utiliser dans vos propres dépôts dès aujourd'hui.

---

## Démarrage Rapide : Améliorez votre agent dès aujourd'hui

Vous n'avez pas besoin de lire les 12 cours avant de commencer à en tirer profit. Si vous utilisez déjà un agent de codage sur un vrai projet, voici comment l'améliorer dès maintenant.

L'idée est simple : au lieu de simplement écrire des prompts, donnez à votre agent un ensemble de fichiers structurés qui définissent ce qu'il faut faire, ce qui a été fait et comment vérifier le travail. Ces fichiers résident dans votre dépôt, donc chaque session démarre depuis le même état.

```text
    YOUR PROJECT ROOT
    ├── AGENTS.md              <-- the agent's operating manual
    ├── CLAUDE.md              <-- (alternative, if using Claude Code)
    ├── init.sh                <-- runs install + verify + start
    ├── feature_list.json      <-- what features exist, which are done
    ├── claude-progress.md     <-- what happened each session
    └── src/                   <-- your actual code
```

Récupérez les modèles de démarrage depuis la [Bibliothèque de Ressources](https://walkinglabs.github.io/learn-harness-engineering/en/resources/) et déposez-les dans votre projet. C'est tout. Quatre fichiers, et vos sessions d'agent seront déjà nettement plus stables qu'avec des prompts seuls.

---

## Projet Final : Une véritable application

Les six projets du cours gravitent autour du même produit : **une application de bureau de base de connaissances personnelle basée sur Electron**.

```text
    ┌─────────────────────────────────────────────────────┐
    │               Knowledge Base Desktop App            │
    │                                                     │
    │  ┌──────────────┐  ┌──────────────────────────────┐│
    │  │ Document List │  │       Q&A Panel              ││
    │  │              │  │                              ││
    │  │ doc-001.md   │  │  Q: What is harness eng?    ││
    │  │ doc-002.md   │  │  A: The environment built    ││
    │  │ doc-003.md   │  │     around an agent model... ││
    │  │ ...          │  │     [citation: doc-002.md]   ││
    │  └──────────────┘  └──────────────────────────────┘│
    │                                                     │
    │  ┌─────────────────────────────────────────────────┐│
    │  │ Status Bar: 42 docs | 38 indexed | last sync 3m ││
    │  └─────────────────────────────────────────────────┘│
    └─────────────────────────────────────────────────────┘

    Core features:
    ├── Import local documents
    ├── Manage a document library
    ├── Process and index documents
    ├── Run AI-powered Q&A over imported content
    └── Return grounded answers with citations
```

Ce projet a été choisi car il combine une forte valeur pratique, une complexité produit suffisante pour le monde réel et un bon cadre pour observer les améliorations avant/après harness.

Le starter/solution de chaque projet du cours est une copie complète de cette application Electron à ce stade d'évolution. Le starter de P(N+1) est dérivé de la solution de P(N) -- l'application évolue au fur et à mesure que vos compétences en harness se développent.

---

## Parcours d'Apprentissage

Le cours est conçu pour être suivi dans l'ordre. Chaque phase s'appuie sur la précédente.

```text
    Phase 1: SEE THE PROBLEM              Phase 2: STRUCTURE THE REPO
    ========================              ==========================

    L01  Strong models ≠ reliable         L03  Repository as single
         execution                              source of truth
    L02  What harness actually means
                                       L04  Split instructions across
         |                                   files, not one giant file
         v
    P01  Prompt-only vs.                       |
         rules-first comparison                v
                                               P02  Agent-readable workspace


    Phase 3: CONNECT SESSIONS             Phase 4: FEEDBACK & SCOPE
    ==========================           =========================

    L05  Keep context alive               L07  Draw clear task boundaries
         across sessions
                                       L08  Feature lists as harness
    L06  Initialize before every               primitives
         agent session
                                               |
         |                                     v
         v                                     P04  Runtime feedback to
    P03  Multi-session continuity                   correct agent behavior


    Phase 5: VERIFICATION                 Phase 6: PUT IT ALL TOGETHER
    =====================                 ============================

    L09  Stop agents from                 L11  Make agent's runtime
         declaring victory early               observable

    L10  Full-pipeline run =              L12  Clean handoff at end of
         real verification                      every session

         |                                     |
         v                                     v
    P05  Agent verifies its own work       P06  Build a complete harness
                                               (capstone project)
```

Chaque phase prend environ une semaine si vous suivez le cours à temps partiel. Si vous souhaitez aller plus vite, les phases 1 à 3 peuvent être effectuées en un long week-end.

---

## Programme d'Études

### Cours magistraux -- 12 unités conceptuelles, chacune répondant à une question fondamentale

*Lisez le texte complet de chaque cours sur le [Site de Documentation](https://walkinglabs.github.io/learn-harness-engineering/).*

| Session | Question | Idée Centrale |
|---------|----------|---------------|
| [L01](../../docs/lectures/lecture-01-why-capable-agents-still-fail/index.md) | Pourquoi les modèles performants échouent-ils encore sur des tâches réelles ? | L'écart de capacité entre les benchmarks et l'ingénierie réelle |
| [L02](../../docs/lectures/lecture-02-what-a-harness-actually-is/index.md) | Que signifie réellement « harness » ? | Cinq sous-systèmes : instructions, état, vérification, portée, cycle de vie |
| [L03](../../docs/lectures/lecture-03-why-the-repository-must-become-the-system-of-record/index.md) | Pourquoi le dépôt doit-il être l'unique source de vérité ? | Si l'agent ne peut pas le voir, ça n'existe pas |
| [L04](../../docs/lectures/lecture-04-why-one-giant-instruction-file-fails/index.md) | Pourquoi un seul fichier d'instructions géant échoue-t-il ? | Divulgation progressive : donnez une carte, pas une encyclopédie |
| [L05](../../docs/lectures/lecture-05-why-long-running-tasks-lose-continuity/index.md) | Pourquoi les tâches de longue durée perdent-elles leur continuité ? | Persister le progrès sur disque ; reprendre là où vous vous êtes arrêté |
| [L06](../../docs/lectures/lecture-06-why-initialization-needs-its-own-phase/index.md) | Pourquoi l'initialisation nécessite-t-elle sa propre phase ? | Vérifier que l'environnement est sain avant que l'agent ne commence à travailler |
| [L07](../../docs/lectures/lecture-07-why-agents-overreach-and-under-finish/index.md) | Pourquoi les agents vont-ils trop loin et n'en font-ils pas assez ? | Une seule fonctionnalité à la fois ; définition explicite de « terminé » |
| [L08](../../docs/lectures/lecture-08-why-feature-lists-are-harness-primitives/index.md) | Pourquoi les listes de fonctionnalités sont-elles des primitives du harness ? | Des limites de portée lisibles par machine que l'agent ne peut pas ignorer |
| [L09](../../docs/lectures/lecture-09-why-agents-declare-victory-too-early/index.md) | Pourquoi les agents déclarent-ils victoire trop tôt ? | Lacunes de vérification : confiance ≠ correction |
| [L10](../../docs/lectures/lecture-10-why-end-to-end-testing-changes-results/index.md) | Pourquoi les tests de bout en bout changent-ils les résultats ? | Seule une exécution complète du pipeline compte comme véritable vérification |
| [L11](../../docs/lectures/lecture-11-why-observability-belongs-inside-the-harness/index.md) | Pourquoi l'observabilité appartient-elle au harness ? | Si vous ne pouvez pas voir ce que l'agent a fait, vous ne pouvez pas corriger ce qu'il a cassé |
| [L12](../../docs/lectures/lecture-12-why-every-session-must-leave-a-clean-state/index.md) | Pourquoi chaque session doit-elle laisser un état propre ? | Le succès de la prochaine session dépend du nettoyage de celle-ci |

### Projets -- 6 projets pratiques appliquant les méthodes des cours à la même application Electron

| Projet | Ce que vous faites | Mécanisme du Harness |
|--------|--------------------|----------------------|
| [P01](../../docs/projects/project-01-baseline-vs-minimal-harness/index.md) | Exécuter la même tâche deux fois : avec prompts seuls vs. avec règles d'abord | Harness minimal : AGENTS.md + init.sh + feature_list.json |
| [P02](../../docs/projects/project-02-agent-readable-workspace/index.md) | Restructurer le dépôt pour que l'agent puisse le lire | Espace de travail lisible par l'agent + fichiers d'état persistants |
| [P03](../../docs/projects/project-03-multi-session-continuity/index.md) | Faire en sorte que l'agent reprenne là où il s'est arrêté | Journal de progression + transfert de session + continuité multi-sessions |
| [P04](../../docs/projects/project-04-incremental-indexing/index.md) | Empêcher l'agent d'en faire trop ou pas assez | Retour d'exécution + contrôle de portée + indexation incrémentale |
| [P05](../../docs/projects/project-05-grounded-qa-verification/index.md) | Faire en sorte que l'agent vérifie son propre travail | Auto-vérification + Q&A fondé + achèvement basé sur les preuves |
| [P06](../../docs/projects/project-06-runtime-observability-and-debugging/index.md) | Construire un harness complet à partir de zéro (projet final) | Harness complet : tous les mécanismes + observabilité + étude d'ablation |

```text
    PROJECT EVOLUTION
    =================

    P01  Prompt-only vs. rules-first       You see the problem
     |
     v
    P02  Agent-readable workspace           You restructure the repo
     |
     v
    P03  Multi-session continuity           You connect sessions
     |
     v
    P04  Runtime feedback & scope           You add feedback loops
     |
     v
    P05  Self-verification                  You make the agent check itself
     |
     v
    P06  Complete harness (capstone)        You build the full system

    Each project's solution becomes the next project's starter.
    The app evolves. Your harness skills grow with it.
```

### Bibliothèque de Ressources

- [Bibliothèque de Ressources en anglais](https://walkinglabs.github.io/learn-harness-engineering/en/resources/) -- modèles, listes de contrôle et références de méthodes
- [Bibliothèque de Ressources en chinois](https://walkinglabs.github.io/learn-harness-engineering/zh/resources/) -- 中文模板、清单和方法参考
- [Bibliothèque de Ressources en russe](https://walkinglabs.github.io/learn-harness-engineering/ru/resources/) -- шаблоны, чек-листы и справочники
- [Bibliothèque de Ressources en vietnamien](https://walkinglabs.github.io/learn-harness-engineering/vi/resources/) -- mẫu, danh sách kiểm tra và tài liệu tham khảo

---

## Le Cycle de Vie de la Session de l'Agent

L'une des idées centrales de ce cours : **la session de l'agent doit suivre un cycle de vie structuré, pas être laissée au hasard.** Voici à quoi cela ressemble :

```text
    AGENT SESSION LIFECYCLE
    ======================

    ┌──────────────────────────────────────────────────────────────────┐
    │  START                                                          │
    │                                                                  │
    │  1. Agent reads AGENTS.md / CLAUDE.md                           │
    │  2. Agent runs init.sh (install, verify, health check)          │
    │  3. Agent reads claude-progress.md (what happened last time)    │
    │  4. Agent reads feature_list.json (what's done, what's next)    │
    │  5. Agent checks git log (recent changes)                       │
    │                                                                  │
    │  SELECT                                                          │
    │                                                                  │
    │  6. Agent picks exactly ONE unfinished feature                   │
    │  7. Agent works only on that feature                             │
    │                                                                  │
    │  EXECUTE                                                         │
    │                                                                  │
    │  8. Agent implements the feature                                 │
    │  9. Agent runs verification (tests, lint, type-check)           │
    │  10. If verification fails: fix and re-run                      │
    │  11. If verification passes: record evidence                    │
    │                                                                  │
    │  WRAP UP                                                         │
    │                                                                  │
    │  12. Agent updates claude-progress.md                           │
    │  13. Agent updates feature_list.json                            │
    │  14. Agent records what's still broken or unverified            │
    │  15. Agent commits (only when safe to resume)                   │
    │  16. Agent leaves clean restart path for next session           │
    │                                                                  │
    └──────────────────────────────────────────────────────────────────┘

    The harness governs every transition in this lifecycle.
    The model decides what code to write at each step.
    Without the harness, step 9 becomes "agent says it looks fine."
    With the harness, step 9 is "tests pass, lint is clean, types check."
```

---

## À qui ce cours s'adresse

Ce cours est destiné :

- Aux ingénieurs utilisant déjà des agents de codage et souhaitant une meilleure stabilité et qualité
- Aux chercheurs ou constructeurs souhaitant une compréhension systématique de la conception de harness
- Aux responsables techniques qui doivent comprendre comment la conception de l'environnement affecte les performances de l'agent

Ce cours n'est PAS destiné :

- Aux personnes cherchant une introduction à l'IA sans code
- Aux personnes qui ne s'intéressent qu'aux prompts et ne prévoient pas de construire de véritables implémentations
- Aux apprenants non préparés à laisser des agents travailler dans de vrais dépôts

---

## Prérequis

Il faut au moins l'un de ces outils :

- Claude Code
- Codex
- Un autre agent de codage IDE ou CLI prenant en charge l'édition de fichiers, l'exécution de commandes et les tâches multi-étapes

Le cours suppose que vous êtes capable de :

- Ouvrir un dépôt local
- Autoriser l'agent à modifier des fichiers
- Autoriser l'agent à exécuter des commandes
- Inspecter les résultats et réexécuter les tâches

Si vous ne disposez pas d'un tel outil, vous pouvez toujours lire le contenu du cours, mais vous ne pourrez pas réaliser les projets comme prévu.

---

## Aperçu Local

Ce dépôt utilise VitePress comme visualiseur de documentation.

```sh
npm install
npm run docs:dev        # Serveur de développement avec rechargement à chaud
npm run docs:build      # Build de production
npm run docs:preview    # Aperçu du site construit
```

Ouvrez ensuite l'URL locale affichée par VitePress dans votre navigateur.

---

## Prérequis Techniques

Requis :

- Familiarité avec le terminal, git et les environnements de développement local
- Capacité à lire et écrire du code dans au moins une pile applicative courante
- Expérience de base en débogage logiciel (lecture de logs, tests et comportement à l'exécution)
- Assez de temps à consacrer à un cours axé sur l'implémentation

Utile mais non requis :

- Expérience avec Electron, les applications de bureau ou les outils local-first
- Formation en tests, logging ou architecture logicielle
- Exposition préalable à Codex, Claude Code ou à des agents de codage similaires

---

## Références Principales

Primaires :

- [OpenAI : Harness engineering : leveraging Codex in an agent-first world](https://openai.com/index/harness-engineering/)
- [Anthropic : Effective harnesses for long-running agents](https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents)
- [Anthropic : Harness design for long-running application development](https://www.anthropic.com/engineering/harness-design-long-running-apps)
- [OpenAI : Unrolling the Codex agent loop](https://openai.com/index/unrolling-the-codex-agent-loop/)
- [Anthropic : Demystifying evals for AI agents](https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents)
- [LangChain : Improving Deep Agents with harness engineering](https://www.langchain.com/blog/improving-deep-agents-with-harness-engineering)
- [Thoughtworks / Martin Fowler : Harness engineering for coding agent users](https://martinfowler.com/articles/harness-engineering.html)
- [Cursor : Continually improving our agent harness](https://cursor.com/blog/continually-improving-agent-harness)

Consultez la liste complète de références en couches dans [`docs/en/resources/reference/`](../../docs/en/resources/reference/index.md).

---

## Structure du Dépôt

```text
learn-harness-engineering/
├── docs/                          # Site de documentation VitePress
│   ├── lectures/                  # 12 cours (index.md + exemples dans code/)
│   │   ├── lecture-01-*/
│   │   ├── lecture-02-*/
│   │   └── ... (12 au total)
│   ├── projects/                  # 6 descriptions de projets
│   │   ├── project-01-*/
│   │   └── ... (6 au total)
│   └── resources/                 # Modèles et références multilingues
│       ├── en/                    # Modèles, listes de contrôle et guides en anglais
│       ├── zh/                    # Modèles, listes de contrôle et guides en chinois
│       ├── ru/                    # Modèles, listes de contrôle et guides en russe
│       └── vi/                    # Modèles, listes de contrôle et guides en vietnamien
├── projects/
│   ├── shared/                    # Fondation partagée Electron + TypeScript + React
│   └── project-NN/               # Répertoires starter/ et solution/ par projet
├── skills/                        # Skills réutilisables pour agents IA
│   └── harness-creator/           # Skill de Harness Engineering
├── package.json                   # VitePress + outils de développement
└── CLAUDE.md                      # Instructions Claude Code pour ce dépôt
```

---

## Comment le cours est organisé

- Chaque cours se concentre sur une seule question
- Le cours comprend 6 projets
- Chaque projet nécessite que l'agent effectue un véritable travail
- Chaque projet compare les résultats avec un harness faible vs. un harness robuste
- Ce qui compte, c'est la différence mesurée, pas la quantité de documentation rédigée

---

## Skills

Ce dépôt inclut également des skills réutilisables pour agents IA que vous pouvez installer directement dans votre IDE ou espace de travail agentique.

- [**harness-creator**](../../skills/harness-creator/) : Un skill qui vous aide à générer un harness de niveau production pour votre propre projet en quelques minutes.

---

## Autres Cours

Notre équipe a également créé d'autres cours ! Découvrez-les :

[![Hands-on Modern RL](https://img.shields.io/badge/HANDS--ON_MODERN_RL-0052cc?style=for-the-badge)](https://github.com/walkinglabs/hands-on-modern-rl)

**Hands-on Modern RL** : Un programme pratique et open source qui comble le fossé entre les concepts de base de l'apprentissage par renforcement et l'alignement des LLM, le RLVR et les systèmes agentiques avancés.

---

## Historique des Étoiles

[![Star History Chart](https://api.star-history.com/svg?repos=walkinglabs/learn-harness-engineering&type=date&legend=top-left)](https://www.star-history.com/#walkinglabs/learn-harness-engineering&type=date&legend=top-left)

---

## Remerciements

Ce cours a été inspiré par et puise ses idées dans [learn-claude-code](https://github.com/shareAI-lab/learn-claude-code) -- un guide progressif pour construire un agent à partir de zéro, d'une simple boucle à l'exécution autonome isolée.
