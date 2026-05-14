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

> **Ein projektbasierter Kurs über den Aufbau von Umgebungen, Zustandsverwaltung, Verifizierung und Kontrollmechanismen, die KI-Coding-Agenten zuverlässig machen.**

Learn Harness Engineering ist ein Kurs, der sich der Entwicklung von KI-Coding-Agenten widmet. Wir haben die fortschrittlichsten Theorien und Praktiken des Harness Engineering in der Branche eingehend studiert und zusammengefasst. Unsere Kernreferenzen umfassen:

- [OpenAI: Harness engineering: leveraging Codex in an agent-first world](https://openai.com/index/harness-engineering/)
- [Anthropic: Effective harnesses for long-running agents](https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents)
- [Anthropic: Harness design for long-running application development](https://www.anthropic.com/engineering/harness-design-long-running-apps)
- [Awesome Harness Engineering](https://github.com/walkinglabs/awesome-harness-engineering)

> **Schneller Einstieg?** Der Skill [`skills/harness-creator/`](../../skills/) kann Ihnen helfen, in Minuten ein produktionsreifes Harness (AGENTS.md, Feature-Listen, init.sh, Verifizierungs-Workflows) für Ihr eigenes Projekt zu erstellen.

---

## Inhaltsverzeichnis

- [Visuelle Vorschau](#visuelle-vorschau)
- [Was Harness Engineering wirklich bedeutet](#was-harness-engineering-wirklich-bedeutet)
- [Schnellstart: Verbessern Sie Ihren Agenten noch heute](#schnellstart-verbessern-sie-ihren-agenten-noch-heute)
- [Abschlussprojekt: Eine echte App](#abschlussprojekt-eine-echte-app)
- [Lernpfad](#lernpfad)
- [Lehrplan](#lehrplan)
- [Skills](#skills)
- [Weitere Kurse](#weitere-kurse)

---

## Visuelle Vorschau

### Kurs-Startseite
> Ein umfassender Kursüberblick und eine Einführung in die Kernphilosophien, die einen klaren Einstiegspfad bieten.

![Vorschau der Kurs-Startseite](../../docs/public/screenshots/readme/zh-home.png)

### Immersive Vorlesungen
> Tiefe Einblicke in reale Problemstellungen und praktische Projekte (wie Projekt 01) für ein immersives Lernerlebnis.

![Vorschau der Kurs-Vorlesung](../../docs/public/screenshots/readme/zh-lecture-01.png)

### Vorlagen-Bibliothek
> Vorlagen und Referenzkonfigurationen, die entwickelt wurden, um häufige Fallstricke bei der Entwicklung von Multi-Turn-KI-Agenten zu lösen, wie Kontextverlust und vorzeitiger Aufgabenabschluss.

![Vorschau der Vorlagen-Bibliothek](../../docs/public/screenshots/readme/zh-resources.png)

## PDF-Kursbücher

Das Repository enthält nun eine PDF-Build-Pipeline für die Kursinhalte.

- Führen Sie `npm run pdf:build` aus, um englische und chinesische PDFs lokal zu generieren.
- Die Ausgabedateien werden in `artifacts/pdfs/` geschrieben.
- Führen Sie `npm run screenshots:readme` aus, wenn Sie die README-Vorschaubilder aktualisieren möchten.
- Der GitHub Actions-Workflow [`release-course-pdfs.yml`](../../.github/workflows/release-course-pdfs.yml) kann die PDFs erstellen und auf GitHub Releases veröffentlichen.

---

## Das Modell ist klug, das Harness macht es zuverlässig

Es gibt eine harte Wahrheit, die die meisten Menschen auf die harte Tour lernen: **Das stärkste Modell der Welt wird bei echten Engineering-Aufgaben dennoch scheitern, wenn Sie keine geeignete Umgebung dafür aufbauen.**

Sie haben das wahrscheinlich selbst erlebt. Sie geben Claude oder GPT eine Aufgabe in Ihrem Repo. Es beginnt gut — liest Dateien, schreibt Code, sieht produktiv aus. Dann geht etwas schief. Es überspringt einen Schritt. Es zerstört einen Test. Es sagt „fertig", aber nichts funktioniert tatsächlich. Sie verbringen mehr Zeit mit der Behebung, als wenn Sie es selbst gemacht hätten.

Das ist kein Modellproblem. Es ist ein Harness-Problem.

Die Beweise sind eindeutig. Anthropic führte ein kontrolliertes Experiment durch: gleiches Modell (Opus 4.5), gleicher Prompt („baue einen 2D-Retro-Spieleditor"). Ohne Harness gab es 9 $ in 20 Minuten aus und produzierte etwas, das nicht funktionierte. Mit einem vollständigen Harness (Planer + Generator + Evaluierer) gab es 200 $ in 6 Stunden aus und baute ein Spiel, das man tatsächlich spielen konnte. Das Modell hat sich nicht geändert. Das Harness schon.

OpenAI berichtete dasselbe mit Codex: in einem gut geharnischten Repository wechselt dasselbe Modell von „unzuverlässig" zu „zuverlässig". Keine marginale Verbesserung — ein qualitativer Sprung.

**Dieser Kurs bringt Ihnen bei, wie Sie diese Umgebung aufbauen.**

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

## Was Harness Engineering wirklich bedeutet

Harness Engineering handelt davon, eine vollständige Arbeitsumgebung um das Modell herum aufzubauen, damit es zuverlässige Ergebnisse liefert. Es geht nicht darum, bessere Prompts zu schreiben. Es geht darum, das System zu entwerfen, in dem das Modell arbeitet.

Ein Harness hat fünf Subsysteme:

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

Jedes Subsystem hat eine Aufgabe:

- **Instructions** — Dem Agenten sagen, was zu tun ist, in welcher Reihenfolge und was er lesen soll, bevor er beginnt. Nicht eine riesige Datei; eine progressive Enthüllungsstruktur, die der Agent nach Bedarf navigiert.
- **State** — Verfolgen, was erledigt wurde, was in Bearbeitung ist und was als Nächstes ansteht. Auf der Festplatte gespeichert, damit die nächste Session genau dort ansetzt, wo die letzte aufgehört hat.
- **Verification** — Nur eine bestehende Testsuite gilt als Nachweis. Der Agent kann keinen Erfolg melden ohne ausführbaren Beweis.
- **Scope** — Den Agenten auf ein Feature gleichzeitig beschränken. Keine Übergriffe. Kein halbfertiges Abschließen von drei Dingen. Kein Umschreiben der Feature-Liste, um unfertige Arbeit zu verbergen.
- **Session Lifecycle** — Initialisierung am Anfang. Aufräumen am Ende. Einen sauberen Neustartpfad für die nächste Sitzung hinterlassen.

---

## Warum dieser Kurs existiert

Die Frage ist nicht „Können Modelle Code schreiben?" Sie können. Die Frage ist: **Können sie zuverlässig echte Engineering-Aufgaben in echten Repositories über mehrere Sessions hinweg absolvieren, ohne ständige menschliche Überwachung?**

Im Moment lautet die Antwort: nicht ohne ein Harness.

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

Die Fragen, die dieser Kurs wirklich interessieren:

- Welche Harness-Designs verbessern die Aufgabenabschlussraten?
- Welche Designs reduzieren Nacharbeit und falsche Abschlüsse?
- Welche Mechanismen halten langlaufende Aufgaben stetig voran?
- Welche Strukturen halten das System nach mehreren Agenten-Läufen wartbar?

---

## Kurscurriculum & Dokumentation

Die vollständigen Kursmaterialien finden Sie auf der **[Dokumentations-Website](https://walkinglabs.github.io/learn-harness-engineering/)**.

Das Curriculum ist in drei Teile gegliedert:

1. **Vorlesungen**: 12 konzeptionelle Einheiten, die die Theorie hinter dem Harness Engineering erklären.
2. **Projekte**: 6 praktische Projekte, bei denen Sie einen agentenbasierten Arbeitsbereich von Grund auf neu aufbauen.
3. **Vorlagen-Bibliothek**: Kopierfertige Vorlagen (`AGENTS.md`, `feature_list.json`, `init.sh` usw.), die Sie noch heute in Ihren eigenen Repositories verwenden können.

---

## Schnellstart: Verbessern Sie Ihren Agenten noch heute

Sie müssen nicht alle 12 Vorlesungen lesen, bevor Sie einen Nutzen ziehen. Wenn Sie bereits einen Coding-Agenten in einem echten Projekt einsetzen, können Sie ihn jetzt sofort verbessern.

Die Idee ist einfach: Anstatt nur Prompts zu schreiben, geben Sie Ihrem Agenten einen Satz strukturierter Dateien, die definieren, was zu tun ist, was bereits erledigt ist und wie die Arbeit verifiziert wird. Diese Dateien befinden sich in Ihrem Repo, sodass jede Session vom gleichen Zustand ausgeht.

```text
    YOUR PROJECT ROOT
    ├── AGENTS.md              <-- das Betriebshandbuch des Agenten
    ├── CLAUDE.md              <-- (Alternative, wenn Sie Claude Code verwenden)
    ├── init.sh                <-- führt install + verify + start aus
    ├── feature_list.json      <-- welche Features existieren, welche erledigt sind
    ├── claude-progress.md     <-- was in jeder Session passiert ist
    └── src/                   <-- Ihr tatsächlicher Code
```

Laden Sie sich die Starter-Vorlagen aus der [Vorlagen-Bibliothek](https://walkinglabs.github.io/learn-harness-engineering/en/resources/) herunter und fügen Sie sie in Ihr Projekt ein. Das war's. Vier Dateien, und Ihre Agenten-Sessions werden bereits deutlich stabiler sein als mit Prompts allein.

---

## Abschlussprojekt: Eine echte App

Alle sechs Kursprojekte drehen sich um dasselbe Produkt: **eine Electron-basierte Desktop-App für persönliches Wissensmanagement**.

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

Dieses Projekt wurde gewählt, weil es hohen praktischen Nutzen, ausreichende reale Produktkomplexität und ein gutes Szenario für die Beobachtung von Harness-Verbesserungen (Vorher/Nachher) verbindet.

Jedes Kursprojekt (Starter/Lösung) ist eine vollständige Kopie dieser Electron-App im jeweiligen Entwicklungsstadium. Der Starter von P(N+1) wird aus der Lösung von P(N) abgeleitet — die App entwickelt sich weiter, während Ihre Harness-Fähigkeiten wachsen.

---

## Lernpfad

Der Kurs ist für die chronologische Abarbeitung konzipiert. Jede Phase baut auf der vorherigen auf.

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

Jede Phase dauert etwa eine Woche, wenn Sie nebenbei lernen. Wenn Sie schneller vorgehen möchten, können die Phasen 1–3 an einem langen Wochenende absolviert werden.

---

## Lehrplan

### Vorlesungen — 12 konzeptionelle Einheiten, die jeweils eine Kernfrage beantworten

*Lesen Sie den vollständigen Text jeder Vorlesung auf der [Dokumentations-Website](https://walkinglabs.github.io/learn-harness-engineering/).*

| Session | Frage | Kernidee |
|---------|-------|----------|
| [L01](../../docs/lectures/lecture-01-why-capable-agents-still-fail/index.md) | Warum scheitern starke Modelle dennoch bei echten Aufgaben? | Die Lücke zwischen Benchmarks und echtem Engineering |
| [L02](../../docs/lectures/lecture-02-what-a-harness-actually-is/index.md) | Was bedeutet „Harness" eigentlich? | Fünf Subsysteme: Instructions, State, Verification, Scope, Lifecycle |
| [L03](../../docs/lectures/lecture-03-why-the-repository-must-become-the-system-of-record/index.md) | Warum muss das Repo die einzige Quelle der Wahrheit sein? | Wenn der Agent es nicht sehen kann, existiert es nicht |
| [L04](../../docs/lectures/lecture-04-why-one-giant-instruction-file-fails/index.md) | Warum scheitert eine einzige riesige Instruktionsdatei? | Progressive Enthüllung: eine Karte geben, keine Enzyklopädie |
| [L05](../../docs/lectures/lecture-05-why-long-running-tasks-lose-continuity/index.md) | Warum verlieren langlaufende Aufgaben ihre Kontinuität? | Fortschritt auf der Festplatte speichern; dort fortfahren, wo man aufgehört hat |
| [L06](../../docs/lectures/lecture-06-why-initialization-needs-its-own-phase/index.md) | Warum braucht die Initialisierung eine eigene Phase? | Die Umgebung auf Funktionsfähigkeit prüfen, bevor der Agent mit der Arbeit beginnt |
| [L07](../../docs/lectures/lecture-07-why-agents-overreach-and-under-finish/index.md) | Warum greifen Agenten über und schließen unvollständig ab? | Ein Feature gleichzeitig; explizite Definition von „Fertig" |
| [L08](../../docs/lectures/lecture-08-why-feature-lists-are-harness-primitives/index.md) | Warum sind Feature-Listen Harness-Primitiven? | Maschinenlesbare Scope-Grenzen, die der Agent nicht ignorieren kann |
| [L09](../../docs/lectures/lecture-09-why-agents-declare-victory-too-early/index.md) | Warum melden Agenten zu früh den Erfolg? | Verifizierungslücken: Vertrauen ≠ Korrektheit |
| [L10](../../docs/lectures/lecture-10-why-end-to-end-testing-changes-results/index.md) | Warum ändert End-to-End-Testing die Ergebnisse? | Nur ein vollständiger Pipeline-Lauf gilt als echte Verifizierung |
| [L11](../../docs/lectures/lecture-11-why-observability-belongs-inside-the-harness/index.md) | Warum gehört Observability in das Harness? | Wenn Sie nicht sehen können, was der Agent getan hat, können Sie nicht reparieren, was er zerstört hat |
| [L12](../../docs/lectures/lecture-12-why-every-session-must-leave-a-clean-state/index.md) | Warum muss jede Session einen sauberen Zustand hinterlassen? | Der Erfolg der nächsten Session hängt vom Aufräumen dieser Session ab |

### Projekte — 6 praktische Projekte, die Vorlesungsmethoden auf dieselbe Electron-App anwenden

| Projekt | Was Sie tun | Harness-Mechanismus |
|---------|-------------|---------------------|
| [P01](../../docs/projects/project-01-baseline-vs-minimal-harness/index.md) | Dieselbe Aufgabe zweimal ausführen: nur Prompt vs. regelnbasiert | Minimales Harness: AGENTS.md + init.sh + feature_list.json |
| [P02](../../docs/projects/project-02-agent-readable-workspace/index.md) | Das Repo umstrukturieren, damit der Agent es lesen kann | Agentenlesbarer Arbeitsbereich + persistente Zustandsdateien |
| [P03](../../docs/projects/project-03-multi-session-continuity/index.md) | Den Agenten dort fortfahren lassen, wo er aufgehört hat | Fortschrittsprotokoll + Session-Übergabe + Multi-Session-Kontinuität |
| [P04](../../docs/projects/project-04-incremental-indexing/index.md) | Den Agenten davon abhalten, zu viel oder zu wenig zu tun | Laufzeit-Feedback + Scope-Kontrolle + inkrementelle Indizierung |
| [P05](../../docs/projects/project-05-grounded-qa-verification/index.md) | Den Agenten seine eigene Arbeit verifizieren lassen | Selbstverifizierung + fundierte Q&A + evidenzbasierter Abschluss |
| [P06](../../docs/projects/project-06-runtime-observability-and-debugging/index.md) | Ein vollständiges Harness von Grund auf neu aufbauen (Abschlussprojekt) | Vollständiges Harness: alle Mechanismen + Observability + Ablationsstudie |

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

### Vorlagen-Bibliothek

- [Englische Vorlagen-Bibliothek](https://walkinglabs.github.io/learn-harness-engineering/en/resources/) — Vorlagen, Checklisten und Methodenreferenzen
- [Chinesische Vorlagen-Bibliothek](https://walkinglabs.github.io/learn-harness-engineering/zh/resources/) — 中文模板、清单和方法参考
- [Russische Vorlagen-Bibliothek](https://walkinglabs.github.io/learn-harness-engineering/ru/resources/) — шаблоны, чек-листы и справочники
- [Vietnamesische Vorlagen-Bibliothek](https://walkinglabs.github.io/learn-harness-engineering/vi/resources/) — mẫu, danh sách kiểm tra và tài liệu tham khảo

---

## Der Lebenszyklus einer Agenten-Session

Eine der Kernideen dieses Kurses: **Die Session eines Agenten sollte einem strukturierten Lebenszyklus folgen, keinem Freifür-alle.** So sieht das aus:

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

## Für wen ist dieser Kurs?

Dieser Kurs richtet sich an:

- Entwickler, die bereits Coding-Agenten verwenden und mehr Stabilität und Qualität möchten
- Forscher oder Entwickler, die ein systematisches Verständnis des Harness-Designs erwerben möchten
- Tech-Leads, die verstehen möchten, wie Umgebungsdesign die Agentenleistung beeinflusst

Dieser Kurs richtet sich nicht an:

- Personen, die eine Einführung in KI ohne Programmierung suchen
- Personen, die sich nur für Prompts interessieren und keine echten Implementierungen planen
- Lernende, die nicht bereit sind, Agenten in echten Repositories arbeiten zu lassen

---

## Voraussetzungen

Dies ist ein Kurs, in dem Sie tatsächlich Coding-Agenten ausführen.

Sie benötigen mindestens eines dieser Werkzeuge:

- Claude Code
- Codex
- Einen anderen IDE- oder CLI-Coding-Agenten, der Dateibearbeitung, Befehlsausführung und mehrstufige Aufgaben unterstützt

Der Kurs setzt voraus, dass Sie:

- Ein lokales Repository öffnen können
- Dem Agenten erlauben können, Dateien zu bearbeiten
- Dem Agenten erlauben können, Befehle auszuführen
- Ausgaben überprüfen und Aufgaben neu starten können

Wenn Sie über kein solches Werkzeug verfügen, können Sie die Kursinhalte dennoch lesen, aber Sie werden die Projekte nicht wie vorgesehen abschließen können.

---

## Lokale Vorschau

Dieses Repository verwendet VitePress als Dokumentationsbetrachter.

```sh
npm install
npm run docs:dev        # Dev-Server mit Hot Reload
npm run docs:build      # Produktions-Build
npm run docs:preview    # Vorschau der erstellten Seite
```

Öffnen Sie dann die lokale URL, die VitePress ausgibt, in Ihrem Browser.

---

## Vorkenntnisse

Erforderlich:

- Vertrautheit mit dem Terminal, Git und lokalen Entwicklungsumgebungen
- Fähigkeit, Code in mindestens einem gängigen Anwendungsstack zu lesen und zu schreiben
- Grundlegende Software-Debugging-Erfahrung (Lesen von Logs, Tests und Laufzeitverhalten)
- Ausreichend Zeit für implementationsfokussierte Kursarbeit

Hilfreich, aber nicht erforderlich:

- Erfahrung mit Electron, Desktop-Apps oder Local-First-Tools
- Hintergrund in Testing, Logging oder Softwarearchitektur
- Frühere Erfahrung mit Codex, Claude Code oder ähnlichen Coding-Agenten

---

## Kernreferenzen

Primär:

- [OpenAI: Harness engineering: leveraging Codex in an agent-first world](https://openai.com/index/harness-engineering/)
- [Anthropic: Effective harnesses for long-running agents](https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents)
- [Anthropic: Harness design for long-running application development](https://www.anthropic.com/engineering/harness-design-long-running-apps)
- [OpenAI: Unrolling the Codex agent loop](https://openai.com/index/unrolling-the-codex-agent-loop/)
- [Anthropic: Demystifying evals for AI agents](https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents)
- [LangChain: Improving Deep Agents with harness engineering](https://www.langchain.com/blog/improving-deep-agents-with-harness-engineering)
- [Thoughtworks / Martin Fowler: Harness engineering for coding agent users](https://martinfowler.com/articles/harness-engineering.html)
- [Cursor: Continually improving our agent harness](https://cursor.com/blog/continually-improving-agent-harness)

Die vollständige geschichtete Referenzliste finden Sie in [`docs/en/resources/reference/`](../../docs/en/resources/reference/index.md).

---

## Repository-Struktur

```text
learn-harness-engineering/
├── docs/                          # VitePress-Dokumentationsseite
│   ├── lectures/                  # 12 Vorlesungen (index.md + code/ Beispiele)
│   │   ├── lecture-01-*/
│   │   ├── lecture-02-*/
│   │   └── ... (insgesamt 12)
│   ├── projects/                  # 6 Projektbeschreibungen
│   │   ├── project-01-*/
│   │   └── ... (insgesamt 6)
│   └── resources/                 # Mehrsprachige Vorlagen & Referenzen
│       ├── en/                    # Englische Vorlagen, Checklisten, Leitfäden
│       ├── zh/                    # Chinesische Vorlagen, Checklisten, Leitfäden
│       ├── ru/                    # Russische Vorlagen, Checklisten, Leitfäden
│       └── vi/                    # Vietnamesische Vorlagen, Checklisten, Leitfäden
├── projects/
│   ├── shared/                    # Gemeinsame Electron + TypeScript + React-Basis
│   └── project-NN/               # Projektbezogene starter/ und solution/ Verzeichnisse
├── skills/                        # Wiederverwendbare KI-Agenten-Skills
│   └── harness-creator/           # Harness Engineering Skill
├── package.json                   # VitePress + Dev-Werkzeuge
└── CLAUDE.md                      # Claude Code-Anweisungen für dieses Repo
```

---

## Wie der Kurs organisiert ist

- Jede Vorlesung konzentriert sich auf eine Frage
- Der Kurs umfasst 6 Projekte
- Jedes Projekt erfordert, dass der Agent echte Arbeit leistet
- Jedes Projekt vergleicht schwache vs. starke Harness-Ergebnisse
- Was zählt, ist der gemessene Unterschied, nicht wie viele Dokumente geschrieben wurden

---

## Skills

Dieses Repository enthält auch wiederverwendbare KI-Agenten-Skills, die Sie direkt in Ihre IDE oder Ihren Agenten-Arbeitsbereich installieren können.

- [**harness-creator**](../../skills/harness-creator/): Ein Skill, der Ihnen hilft, in Minuten ein produktionsreifes Harness für Ihr eigenes Projekt zu erstellen.

---

## Weitere Kurse

Unser Team hat auch weitere Kurse erstellt! Schauen Sie sich diese an:

[![Hands-on Modern RL](https://img.shields.io/badge/HANDS--ON_MODERN_RL-0052cc?style=for-the-badge)](https://github.com/walkinglabs/hands-on-modern-rl)

**Hands-on Modern RL**: Ein Open-Source-Praxiscurriculum, das die Lücke von grundlegenden RL-Konzepten zu LLM-Alignment, RLVR und fortschrittlichen agentischen Systemen überbrückt.

---

## Star-History

[![Star History Chart](https://api.star-history.com/svg?repos=walkinglabs/learn-harness-engineering&type=date&legend=top-left)](https://www.star-history.com/#walkinglabs/learn-harness-engineering&type=date&legend=top-left)

---

## Danksagungen

Dieser Kurs wurde inspiriert von und bezieht Ideen aus [learn-claude-code](https://github.com/shareAI-lab/learn-claude-code) — einem fortschreitenden Leitfaden zum Aufbau eines Agenten von Grund auf, von einem einzelnen Loop bis zur isolierten autonomen Ausführung.
