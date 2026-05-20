[中文版本 →](../../../zh/projects/project-03-multi-session-continuity/)

> Zugehörige Lektionen: [Lektion 05. Kontext über Sessions hinweg lebendig halten](./../../lectures/lecture-05-why-long-running-tasks-lose-continuity/index.md) · [Lektion 06. Vor jeder Agenten-Session initialisieren](./../../lectures/lecture-06-why-initialization-needs-its-own-phase/index.md)
> Vorlagendateien: [templates/](https://github.com/walkinglabs/learn-harness-engineering/blob/main/docs/de/resources/templates/)

# Projekt 03. Den Agenten über Session-Neustarts hinweg weiterarbeiten lassen

## Was du tust

Füge dem Agenten Scope-Kontrolle und Verifikationsgates hinzu. Implementiere Dokument-Chunking, Metadatenextraktion, Indexierungsfortschritt und einen Q&A-Flow mit Zitaten. Nutze `feature_list.json`, um Feature-Status zu verfolgen: ein Feature nach dem anderen, kein `pass` ohne Verifikationsnachweis.

Du führst es zweimal aus: zuerst ohne Einschränkungen, dann mit strikter Durchsetzung.

## Nutze das eingecheckte Projekt

Repository-Pfad: `projects/project-03/`

| Verzeichnis | Inhalt | Vergleichspunkt |
|------|------|------|
| `starter/` | Project-02-Code, bei dem Indexierung und zitierfähiges Q&A noch unvollständig sind. Es gibt ein erstes `feature_list.json`, aber keine finalen Neustart- und Übergabeartefakte. | Ob der Agent über mehrere Funktionen driftet oder nach einem Neustart Zustand verliert. |
| `solution/` | Chunking, Metadaten, Indexierungsstatus und Q&A mit Zitaten sind fertig, plus `init.sh`, `session-handoff.md`, `claude-progress.md` und `clean-state-checklist.md`. | Ob jede Funktion konkrete Evidenz hat, bevor sie als bestanden markiert wird. |

## Werkzeuge

- Claude Code oder Codex
- Git
- Node.js + Electron

## Harness-Mechanismus

Fortschrittslog + Session-Handoff + Multi-Session-Kontinuität
