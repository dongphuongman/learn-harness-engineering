[中文版本 →](../../../zh/projects/project-06-runtime-observability-and-debugging/)

> Related lectures: [Lecture 11. Make the agent's runtime observable](./../../lectures/lecture-11-why-observability-belongs-inside-the-harness/index.md) · [Lecture 12. Clean handoff at the end of every session](./../../lectures/lecture-12-why-every-session-must-leave-a-clean-state/index.md)
> Template files: [templates/](https://github.com/walkinglabs/learn-harness-engineering/blob/main/docs/en/resources/templates/)

# Project 06. Build a Complete Agent Harness (Capstone)

## What You Do

This is the capstone project. Assemble everything learned in the first five projects, run a full benchmark, then do a cleanup pass to verify quality is maintainable.

Use a fixed multi-feature task set covering the complete product slice: document import, indexing, citation-based Q&A, runtime observability, and readable restartable repo state. First run with weak harness baseline, then with your strongest harness, then a cleanup and re-run. Finally, do a harness ablation experiment — remove one component at a time and see which ones actually matter.

## Tools

- Claude Code or Codex
- Git
- Node.js + Electron
- Quality document template
- Evaluator rubric
- All harness components accumulated from the first five projects

## Harness Mechanism

Complete harness: all mechanisms + observability + ablation study

## Use the Checked-In Project

Repository path: `projects/project-06/`

| Directory | What it contains | What to compare |
|------|------|------|
| `starter/` | Mostly complete product code with intentionally weak harness surface: basic `AGENTS.md`, no `feature_list.json`, no `session-handoff.md`, no clean-state checklist. | Manual weak-harness baseline observations. The starter intentionally does not include benchmark scripts. |
| `solution/` | Full harness surface: `AGENTS.md`, `CLAUDE.md`, `feature_list.json`, `init.sh`, `session-handoff.md`, `clean-state-checklist.md`, quality/evaluator docs, benchmark and cleanup scripts. | Run `projects/project-06/solution/scripts/benchmark.sh` and `projects/project-06/solution/scripts/cleanup-scanner.sh`, then compare quality-document evidence. |

Unlike earlier projects, the capstone starter is not mostly missing product
features. The main gap is the operating harness around the app.
