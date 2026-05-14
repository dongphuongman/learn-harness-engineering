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

> **Un curso basado en proyectos sobre cómo construir el entorno, la gestión de estado, la verificación y los mecanismos de control que hacen que los agentes de codificación de IA funcionen de forma fiable.**

Learn Harness Engineering es un curso dedicado a la ingeniería de agentes de codificación de IA. Hemos estudiado y sintetizado en profundidad las teorías y prácticas más avanzadas de Harness Engineering en la industria. Nuestras referencias principales incluyen:

- [OpenAI: Harness engineering: leveraging Codex in an agent-first world](https://openai.com/index/harness-engineering/)
- [Anthropic: Effective harnesses for long-running agents](https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents)
- [Anthropic: Harness design for long-running application development](https://www.anthropic.com/engineering/harness-design-long-running-apps)
- [Awesome Harness Engineering](https://github.com/walkinglabs/awesome-harness-engineering)

> **Inicio rápido?** La skill [`skills/harness-creator/`](../../skills/) puede ayudarte a generar un harness de nivel productivo (AGENTS.md, listas de funcionalidades, init.sh, flujos de verificación) para tu propio proyecto en cuestión de minutos.

---

## Tabla de Contenidos

- [Vista Previa Visual](#vista-previa-visual)
- [Lo que realmente significa Harness Engineering](#lo-que-realmente-significa-harness-engineering)
- [Inicio Rápido: Mejora tu agente hoy mismo](#inicio-rápido-mejora-tu-agente-hoy-mismo)
- [Proyecto Final: Una aplicación real](#proyecto-final-una-aplicación-real)
- [Ruta de Aprendizaje](#ruta-de-aprendizaje)
- [Programa de Estudios](#programa-de-estudios)
- [Skills](#skills)
- [Otros Cursos](#otros-cursos)

---

## Vista Previa Visual

### Pagina de Inicio del Curso
> Un esquema completo del curso e introducción a las filosofías centrales, que proporciona una ruta clara para comenzar.

![Vista previa de la página de inicio](../../docs/public/screenshots/readme/zh-home.png)

### Clases Inmersivas
> Análisis profundo de problemas reales y proyectos prácticos (como el Proyecto 01) para una experiencia de aprendizaje inmersiva.

![Vista previa de las clases](../../docs/public/screenshots/readme/zh-lecture-01.png)

### Biblioteca de Recursos Listos para Usar
> Plantillas y configuraciones de referencia diseñadas para resolver problemas comunes en el desarrollo de agentes de IA de múltiples turnos, como la pérdida de contexto y la finalización prematura de tareas.

![Vista previa de la biblioteca de recursos](../../docs/public/screenshots/readme/zh-resources.png)

## Libros de Curso en PDF

El repositorio ahora incluye un pipeline de construcción en PDF para el contenido del curso.

- Ejecuta `npm run pdf:build` para generar los PDFs en inglés y chino localmente.
- Los archivos de salida se escriben en `artifacts/pdfs/`.
- Ejecuta `npm run screenshots:readme` si deseas actualizar las imágenes de vista previa del README.
- El workflow de GitHub Actions [`release-course-pdfs.yml`](../../.github/workflows/release-course-pdfs.yml) puede construir los PDFs y publicarlos en GitHub Releases.

---

## El modelo es inteligente, el harness lo hace fiable

Hay una verdad difícil que la mayoría de las personas aprenden por las malas: **el modelo más potente del mundo seguirá fallando en tareas de ingeniería reales si no construyes un entorno adecuado a su alrededor.**

Probablemente ya lo hayas visto. Le das una tarea a Claude o GPT en tu repositorio. Comienza bien: lee archivos, escribe código, parece productivo. Luego algo sale mal. Omite un paso. Rompe un test. Dice "listo" pero nada funciona realmente. Pasas más tiempo arreglando las cosas que si lo hubieras hecho tú mismo.

Esto no es un problema del modelo. Es un problema del harness.

La evidencia es clara. Anthropic realizó un experimento controlado: mismo modelo (Opus 4.5), mismo prompt ("construye un editor de juegos retro 2D"). Sin un harness, gastó $9 en 20 minutos y produjo algo que no funcionaba. Con un harness completo (planificador + generador + evaluador), gastó $200 en 6 horas y construyó un juego que realmente se podía jugar. El modelo no cambió. El harness sí.

OpenAI reportó lo mismo con Codex: en un repositorio bien equipado con un harness, el mismo modelo pasa de "poco fiable" a "fiable". No una mejora marginal, sino un cambio cualitativo.

**Este curso te enseña cómo construir ese entorno.**

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

## Lo que realmente significa Harness Engineering

Harness Engineering se trata de construir un entorno de trabajo completo alrededor del modelo para que produzca resultados fiables. No se trata de escribir mejores prompts. Se trata de diseñar el sistema dentro del cual opera el modelo.

Un harness tiene cinco subsistemas:

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

Cada subsistema tiene una única responsabilidad:

- **Instructions** — Le dicen al agente qué hacer, en qué orden y qué leer antes de comenzar. No un archivo gigante; una estructura de divulgación progresiva que el agente navega según lo necesite.
- **State** — Rastrea qué se ha hecho, qué está en progreso y qué sigue. Se persiste en disco para que la siguiente sesión continúe exactamente donde la anterior se quedó.
- **Verification** — Solo un conjunto de tests que pasan cuenta como evidencia. El agente no puede declarar victoria sin pruebas ejecutables.
- **Scope** — Limita al agente a una funcionalidad a la vez. Sin excederse. Sin dejar tres cosas a medias. Sin reescribir la lista de funcionalidades para ocultar trabajo inacabado.
- **Session Lifecycle** — Inicializar al inicio. Limpiar al final. Dejar una ruta de reinicio limpia para la siguiente sesión.

---

## Por qué existe este curso

La pregunta no es "pueden los modelos escribir código?" Pueden. La pregunta es: **pueden completar de forma fiable tareas de ingeniería reales dentro de repositorios reales, a lo largo de múltiples sesiones, sin supervisión humana constante?**

En este momento, la respuesta es: no sin un harness.

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

Las preguntas que realmente importan en este curso:

- Qué diseños de harness mejoran las tasas de completitud de tareas?
- Qué diseños reducen el retrabajo y las completaciones incorrectas?
- Qué mecanismos mantienen las tareas de larga duración progresando de manera constante?
- Qué estructuras mantienen el sistema mantenible después de múltiples ejecuciones del agente?

---

## Plan de Estudios y Documentación del Curso

Para ver todos los materiales del curso, visita el **[Sitio de Documentación](https://walkinglabs.github.io/learn-harness-engineering/)**.

El plan de estudios se divide en tres partes:

1. **Clases**: 12 unidades conceptuales que explican la teoría detrás de Harness Engineering.
2. **Proyectos**: 6 proyectos prácticos donde construyes un espacio de trabajo para agentes desde cero.
3. **Biblioteca de Recursos**: Plantillas listas para copiar (`AGENTS.md`, `feature_list.json`, `init.sh`, etc.) para usar en tus propios repositorios hoy mismo.

---

## Inicio Rápido: Mejora tu agente hoy mismo

No necesitas leer las 12 clases antes de empezar a obtener valor. Si ya estás usando un agente de codificación en un proyecto real, aquí tienes cómo mejorarlo ahora mismo.

La idea es simple: en lugar de solo escribir prompts, dale a tu agente un conjunto de archivos estructurados que definan qué hacer, qué se ha hecho y cómo verificar el trabajo. Estos archivos viven dentro de tu repositorio, así que cada sesión comienza desde el mismo estado.

```text
    YOUR PROJECT ROOT
    ├── AGENTS.md              <-- the agent's operating manual
    ├── CLAUDE.md              <-- (alternative, if using Claude Code)
    ├── init.sh                <-- runs install + verify + start
    ├── feature_list.json      <-- what features exist, which are done
    ├── claude-progress.md     <-- what happened each session
    └── src/                   <-- your actual code
```

Obtén las plantillas iniciales de la [Biblioteca de Recursos](https://walkinglabs.github.io/learn-harness-engineering/en/resources/) y colócalas en tu proyecto. Eso es todo. Cuatro archivos, y tus sesiones de agente ya serán significativamente más estables que ejecutándolas solo con prompts.

---

## Proyecto Final: Una aplicación real

Los seis proyectos del curso giran en torno al mismo producto: **una aplicación de escritorio de base de conocimiento personal basada en Electron**.

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

Este proyecto fue elegido porque combina un fuerte valor práctico, suficiente complejidad de producto del mundo real y un buen entorno para observar mejoras antes y después del harness.

El starter/solution de cada proyecto del curso es una copia completa de esta aplicación Electron en esa etapa evolutiva. El starter de P(N+1) se deriva de la solution de P(N) — la aplicación evoluciona a medida que crecen tus habilidades de harness.

---

## Ruta de Aprendizaje

El curso está diseñado para realizarse en orden. Cada fase se construye sobre la anterior.

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

Cada fase toma aproximadamente una semana si lo haces a tiempo parcial. Si quieres ir más rápido, las fases 1-3 se pueden completar en un fin de semana largo.

---

## Programa de Estudios

### Clases — 12 unidades conceptuales, cada una respondiendo una pregunta central

*Lee el texto completo de cada clase en el [Sitio de Documentación](https://walkinglabs.github.io/learn-harness-engineering/).*

| Sesión | Pregunta | Idea Central |
|---------|----------|--------------|
| [L01](../../docs/lectures/lecture-01-why-capable-agents-still-fail/index.md) | Por qué los modelos potentes siguen fallando en tareas reales? | La brecha de capacidad entre benchmarks e ingeniería real |
| [L02](../../docs/lectures/lecture-02-what-a-harness-actually-is/index.md) | Qué significa realmente "harness"? | Cinco subsistemas: instrucciones, estado, verificación, alcance, ciclo de vida |
| [L03](../../docs/lectures/lecture-03-why-the-repository-must-become-the-system-of-record/index.md) | Por qué el repositorio debe ser la única fuente de verdad? | Si el agente no puede verlo, no existe |
| [L04](../../docs/lectures/lecture-04-why-one-giant-instruction-file-fails/index.md) | Por qué falla un único archivo de instrucciones gigante? | Divulgación progresiva: da un mapa, no una enciclopedia |
| [L05](../../docs/lectures/lecture-05-why-long-running-tasks-lose-continuity/index.md) | Por qué las tareas de larga duración pierden continuidad? | Persistir el progreso en disco; continuar donde lo dejaste |
| [L06](../../docs/lectures/lecture-06-why-initialization-needs-its-own-phase/index.md) | Por qué la inicialización necesita su propia fase? | Verificar que el entorno está saludable antes de que el agente comience a trabajar |
| [L07](../../docs/lectures/lecture-07-why-agents-overreach-and-under-finish/index.md) | Por qué los agentes se exceden y no terminan? | Una funcionalidad a la vez; definición explícita de "hecho" |
| [L08](../../docs/lectures/lecture-08-why-feature-lists-are-harness-primitives/index.md) | Por qué las listas de funcionalidades son primitivas del harness? | Límites de alcance legibles por máquina que el agente no puede ignorar |
| [L09](../../docs/lectures/lecture-09-why-agents-declare-victory-too-early/index.md) | Por qué los agentes declaran victoria demasiado pronto? | Brechas de verificación: confianza ≠ corrección |
| [L10](../../docs/lectures/lecture-10-why-end-to-end-testing-changes-results/index.md) | Por qué las pruebas de extremo a extremo cambian los resultados? | Solo una ejecución completa del pipeline cuenta como verificación real |
| [L11](../../docs/lectures/lecture-11-why-observability-belongs-inside-the-harness/index.md) | Por qué la observabilidad pertenece dentro del harness? | Si no puedes ver lo que el agente hizo, no puedes arreglar lo que rompió |
| [L12](../../docs/lectures/lecture-12-why-every-session-must-leave-a-clean-state/index.md) | Por qué cada sesión debe dejar un estado limpio? | El éxito de la siguiente sesión depende de la limpieza de esta sesión |

### Proyectos — 6 proyectos prácticos aplicando los métodos de las clases a la misma aplicación Electron

| Proyecto | Lo que haces | Mecanismo del Harness |
|----------|--------------|----------------------|
| [P01](../../docs/projects/project-01-baseline-vs-minimal-harness/index.md) | Ejecutar la misma tarea dos veces: solo con prompts vs. con reglas primero | Harness mínimo: AGENTS.md + init.sh + feature_list.json |
| [P02](../../docs/projects/project-02-agent-readable-workspace/index.md) | Reestructurar el repositorio para que el agente pueda leerlo | Espacio de trabajo legible por el agente + archivos de estado persistentes |
| [P03](../../docs/projects/project-03-multi-session-continuity/index.md) | Hacer que el agente continúe desde donde se quedó | Registro de progreso + transferencia de sesión + continuidad multi-sesión |
| [P04](../../docs/projects/project-04-incremental-indexing/index.md) | Evitar que el agente haga demasiado o muy poco | Retroalimentación en tiempo de ejecución + control de alcance + indexación incremental |
| [P05](../../docs/projects/project-05-grounded-qa-verification/index.md) | Hacer que el agente verifique su propio trabajo | Auto-verificación + Q&A fundamentado + completación basada en evidencia |
| [P06](../../docs/projects/project-06-runtime-observability-and-debugging/index.md) | Construir un harness completo desde cero (proyecto final) | Harness completo: todos los mecanismos + observabilidad + estudio de ablación |

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

### Biblioteca de Recursos

- [Biblioteca de Recursos en Inglés](https://walkinglabs.github.io/learn-harness-engineering/en/resources/) — plantillas, checklists y referencias de métodos
- [Biblioteca de Recursos en Chino](https://walkinglabs.github.io/learn-harness-engineering/zh/resources/) — 中文模板、清单和方法参考
- [Biblioteca de Recursos en Ruso](https://walkinglabs.github.io/learn-harness-engineering/ru/resources/) — шаблоны, чек-листы и справочники
- [Biblioteca de Recursos en Vietnamita](https://walkinglabs.github.io/learn-harness-engineering/vi/resources/) — mẫu, danh sách kiểm tra và tài liệu tham khảo

---

## El Ciclo de Vida de la Sesión del Agente

Una de las ideas centrales de este curso: **la sesión del agente debe seguir un ciclo de vida estructurado, no un libre intercambio.** Así es como se ve:

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

## Para quién es este curso

Este curso es para:

- Ingenieros que ya usan agentes de codificación y desean mayor estabilidad y calidad
- Investigadores o constructores que quieren una comprensión sistemática del diseño de harnesses
- Líderes técnicos que necesitan entender cómo el diseño del entorno afecta el rendimiento del agente

Este curso NO es para:

- Personas que buscan una introducción a la IA sin código
- Personas que solo se interesan por los prompts y no planean construir implementaciones reales
- Estudiantes que no están preparados para dejar que los agentes trabajen dentro de repositorios reales

---

## Requisitos

Este es un curso donde realmente ejecutas agentes de codificación.

Necesitas al menos una de estas herramientas:

- Claude Code
- Codex
- Otro agente de codificación de IDE o CLI que soporte edición de archivos, ejecución de comandos y tareas de múltiples pasos

El curso asume que puedes:

- Abrir un repositorio local
- Permitir que el agente edite archivos
- Permitir que el agente ejecute comandos
- Inspeccionar la salida y volver a ejecutar tareas

Si no tienes una de estas herramientas, aún puedes leer el contenido del curso, pero no podrás completar los proyectos según lo previsto.

---

## Vista Previa Local

Este repositorio usa VitePress como visor de documentación.

```sh
npm install
npm run docs:dev        # Servidor de desarrollo con recarga en caliente
npm run docs:build      # Build de producción
npm run docs:preview    # Vista previa del sitio construido
```

Luego abre la URL local que VitePress muestra en tu navegador.

---

## Prerrequisitos

Requerido:

- Familiaridad con la terminal, git y entornos de desarrollo local
- Capacidad de leer y escribir código en al menos un stack de aplicaciones común
- Experiencia básica en depuración de software (lectura de logs, tests y comportamiento en tiempo de ejecución)
- Suficiente tiempo para dedicar a un curso enfocado en la implementación

Útil pero no requerido:

- Experiencia con Electron, aplicaciones de escritorio o herramientas local-first
- Experiencia en testing, logging o arquitectura de software
- Exposición previa a Codex, Claude Code o agentes de codificación similares

---

## Referencias Principales

Primarias:

- [OpenAI: Harness engineering: leveraging Codex in an agent-first world](https://openai.com/index/harness-engineering/)
- [Anthropic: Effective harnesses for long-running agents](https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents)
- [Anthropic: Harness design for long-running application development](https://www.anthropic.com/engineering/harness-design-long-running-apps)
- [OpenAI: Unrolling the Codex agent loop](https://openai.com/index/unrolling-the-codex-agent-loop/)
- [Anthropic: Demystifying evals for AI agents](https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents)
- [LangChain: Improving Deep Agents with harness engineering](https://www.langchain.com/blog/improving-deep-agents-with-harness-engineering)
- [Thoughtworks / Martin Fowler: Harness engineering for coding agent users](https://martinfowler.com/articles/harness-engineering.html)
- [Cursor: Continually improving our agent harness](https://cursor.com/blog/continually-improving-agent-harness)

Consulta la lista completa de referencias en capas en [`docs/en/resources/reference/`](../../docs/en/resources/reference/index.md).

---

## Estructura del Repositorio

```text
learn-harness-engineering/
├── docs/                          # Sitio de documentación VitePress
│   ├── lectures/                  # 12 clases (index.md + ejemplos en code/)
│   │   ├── lecture-01-*/
│   │   ├── lecture-02-*/
│   │   └── ... (12 en total)
│   ├── projects/                  # 6 descripciones de proyectos
│   │   ├── project-01-*/
│   │   └── ... (6 en total)
│   └── resources/                 # Plantillas y referencias multilingües
│       ├── en/                    # Plantillas, checklists y guías en inglés
│       ├── zh/                    # Plantillas, checklists y guías en chino
│       ├── ru/                    # Plantillas, checklists y guías en ruso
│       └── vi/                    # Plantillas, checklists y guías en vietnamita
├── projects/
│   ├── shared/                    # Fundación compartida de Electron + TypeScript + React
│   └── project-NN/               # Directorios starter/ y solution/ por proyecto
├── skills/                        # Skills reutilizables para agentes de IA
│   └── harness-creator/           # Skill de Harness Engineering
├── package.json                   # VitePress + herramientas de desarrollo
└── CLAUDE.md                      # Instrucciones de Claude Code para este repositorio
```

---

## Cómo está organizado el curso

- Cada clase se enfoca en una pregunta
- El curso incluye 6 proyectos
- Cada proyecto requiere que el agente haga trabajo real
- Cada proyecto compara resultados con harness débil vs. fuerte
- Lo que importa es la diferencia medida, no cuánta documentación se escribió

---

## Skills

Este repositorio también incluye skills reutilizables para agentes de IA que puedes instalar directamente en tu IDE o espacio de trabajo del agente.

- [**harness-creator**](../../skills/harness-creator/): Un skill que te ayuda a generar un harness de nivel productivo para tu propio proyecto en cuestión de minutos.

---

## Otros Cursos

Nuestro equipo también ha creado otros cursos! Échales un vistazo:

[![Hands-on Modern RL](https://img.shields.io/badge/HANDS--ON_MODERN_RL-0052cc?style=for-the-badge)](https://github.com/walkinglabs/hands-on-modern-rl)

**Hands-on Modern RL**: Un plan de estudios práctico y de código abierto que cierra la brecha entre los conceptos básicos de RL y la alineación de LLMs, RLVR y sistemas Agentic avanzados.

---

## Historial de Estrellas

[![Star History Chart](https://api.star-history.com/svg?repos=walkinglabs/learn-harness-engineering&type=date&legend=top-left)](https://www.star-history.com/#walkinglabs/learn-harness-engineering&type=date&legend=top-left)

---

## Agradecimientos

Este curso fue inspirado por y toma ideas de [learn-claude-code](https://github.com/shareAI-lab/learn-claude-code) — una guía progresiva para construir un agente desde cero, desde un simple bucle hasta la ejecución autónoma aislada.
