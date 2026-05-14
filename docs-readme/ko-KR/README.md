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

> **AI 코딩 에이전트가 안정적으로 작동하도록 만드는 환경, 상태 관리, 검증 및 제어 메커니즘을 구축하는 프로젝트 기반 강좌입니다.**

Learn Harness Engineering은 AI 코딩 에이전트의 엔지니어링에 집중하는 강좌입니다. 업계에서 가장 선진적인 Harness Engineering 이론과 실무를 심층적으로 연구하고 종합했습니다. 핵심 참고 자료는 다음과 같습니다:

- [OpenAI: Harness engineering: leveraging Codex in an agent-first world](https://openai.com/index/harness-engineering/)
- [Anthropic: Effective harnesses for long-running agents](https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents)
- [Anthropic: Harness design for long-running application development](https://www.anthropic.com/engineering/harness-design-long-running-apps)
- [Awesome Harness Engineering](https://github.com/walkinglabs/awesome-harness-engineering)

> **빠른 시작?** [`skills/harness-creator/`](../../skills/) 스킬을 사용하면 몇 분 만에 여러분의 프로젝트에 프로덕션급 하니스(AGENTS.md, 기능 목록, init.sh, 검증 워크플로우)를 스캐폴딩할 수 있습니다.

---

## 목차

- [✨ 시각적 미리보기](#-시각적-미리보기)
- [Harness Engineering의 진정한 의미](#harness-engineering의-진정한-의미)
- [빠른 시작: 오늘 바로 에이전트 개선하기](#빠른-시작-오늘-바로-에이전트-개선하기)
- [캡스톤 프로젝트: 실제 앱](#캡스톤-프로젝트-실제-앱)
- [학습 경로](#학습-경로)
- [강의 개요](#강의-개요)
- [스킬](#스킬)
- [다른 강좌](#다른-강좌)

---

## ✨ 시각적 미리보기

### 🏠 강좌 홈페이지
> 포괄적인 강좌 개요와 핵심 철학에 대한 소개로, 시작하기 위한 명확한 경로를 제공합니다.

![강좌 홈페이지 미리보기](../../docs/public/screenshots/readme/zh-home.png)

### 📖 몰입형 강의
> 실제 문제점에 대한 심층 분석과 실습 프로젝트(예: Project 01)를 통한 몰입형 학습 경험.

![강좌 강의 미리보기](../../docs/public/screenshots/readme/zh-lecture-01.png)

### 🗂️ 바로 사용 가능한 리소스 라이브러리
> 다중 턴 AI 에이전트 개발에서 발생하는 컨텍스트 손실, 조기 작업 완료 등 일반적인 문제를 해결하기 위해 설계된 템플릿과 참조 구성.

![리소스 라이브러리 미리보기](../../docs/public/screenshots/readme/zh-resources.png)

## PDF 강좌 자료

이 저장소에는 강좌 콘텐츠를 위한 PDF 빌드 파이프라인이 포함되어 있습니다.

- `npm run pdf:build`를 실행하여 영어 및 중국어 PDF를 로컬에서 생성합니다.
- 출력 파일은 `artifacts/pdfs/`에 저장됩니다.
- README 미리보기 이미지를 새로고침하려면 `npm run screenshots:readme`를 실행하세요.
- GitHub Actions 워크플로우 [`release-course-pdfs.yml`](../../.github/workflows/release-course-pdfs.yml)를 통해 PDF를 빌드하고 GitHub Releases에 게시할 수 있습니다.

---

## 모델은 똑똑하고, 하니스가 안정성을 만듭니다

대부분의 사람들이 어려운 방식으로 깨닫는 뼈아픈 사실이 있습니다: **세계에서 가장 강력한 모델이라도 주변에 적절한 환경을 구축하지 않으면 실제 엔지니어링 작업에서 여전히 실패합니다.**

직접 겪어보셨을 것입니다. 여러분의 저장소에서 Claude나 GPT에 작업을 맡깁니다. 처음에는 잘 진행됩니다 — 파일을 읽고, 코드를 작성하고, 생산적으로 보입니다. 그러다 무언가 잘못됩니다. 단계를 건너뜁니다. 테스트를 망가뜨립니다. "완료"라고 말하지만 실제로는 아무것도 작동하지 않습니다. 직접 했더라면 더 빨랐을 작업을 수정하는 데 더 많은 시간을 쓰게 됩니다.

이것은 모델의 문제가 아닙니다. 하니스의 문제입니다.

증거는 명확합니다. Anthropic은 통제된 실험을 진행했습니다: 동일한 모델(Opus 4.5), 동일한 프롬프트("2D 레트로 게임 에디터 구축"). 하니스 없이는 20분 만에 $9를 소비하고 작동하지 않는 결과물을 만들었습니다. 전체 하니스(플래너 + 제너레이터 + 평가자)를 갖추면 6시간 동안 $200를 소비하고 실제로 플레이할 수 있는 게임을 구축했습니다. 모델은 변하지 않았습니다. 하니스가 달랐습니다.

OpenAI도 Codex에서 동일한 결과를 보고했습니다: 잘 구축된 하니스가 있는 저장소에서는 동일한 모델이 "불안정"에서 "안정적"으로 변합니다. 미미한 개선이 아닌 질적인 전환입니다.

**이 강좌는 그 환경을 구축하는 방법을 가르칩니다.**

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

## Harness Engineering의 진정한 의미

Harness engineering은 모델 주변에 안정적인 결과를 생성하는 완전한 작업 환경을 구축하는 것입니다. 더 나은 프롬프트를 작성하는 것이 아닙니다. 모델이 작동하는 시스템 자체를 설계하는 것입니다.

하니스에는 다섯 가지 하위 시스템이 있습니다:

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

각 하위 시스템은 하나의 역할을 담당합니다:

- **지시 사항(Instructions)** — 에이전트에게 무엇을, 어떤 순서로, 시작하기 전에 무엇을 읽어야 하는지 알려줍니다. 거대한 단일 파일이 아닌, 에이전트가 필요에 따라 탐색하는 점진적 공개 구조입니다.
- **상태(State)** — 완료된 작업, 진행 중인 작업, 다음 작업을 추적합니다. 디스크에 영속화되어 다음 세션이 정확히 이전 세션이 중단된 지점에서 이어집니다.
- **검증(Verification)** — 통과하는 테스트 스위트만 증거로 인정됩니다. 에이전트는 실행 가능한 증명 없이 완료를 선언할 수 없습니다.
- **범위(Scope)** — 에이전트를 한 번에 하나의 기능으로 제한합니다. 과도한 작업 금지. 세 가지를 반쯤 완성하는 것 금지. 미완료 작업을 숨기기 위해 기능 목록을 재작성하는 것 금지.
- **세션 수명 주기(Session Lifecycle)** — 시작할 때 초기화. 끝날 때 정리. 다음 세션을 위한 깔끔한 재시작 경로를 남깁니다.

---

## 이 강좌가 존재하는 이유

질문은 "모델이 코드를 작성할 수 있는가?"가 아닙니다. 작성할 수 있습니다. 진짜 질문은: **실제 저장소 내에서 여러 세션에 걸쳐 지속적인 인간 감독 없이 실제 엔지니어링 작업을 안정적으로 완료할 수 있는가?**입니다.

현재 답은: 하니스 없이는 불가능합니다.

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

이 강좌가 실제로 다루는 질문들:

- 어떤 하니스 설계가 작업 완료율을 향상시키는가?
- 어떤 설계가 재작업 및 잘못된 완료를 줄이는가?
- 어떤 메커니즘이 장기 실행 작업을 꾸준히 진행되게 유지하는가?
- 어떤 구조가 여러 에이전트 실행 후에도 시스템을 유지보수 가능하게 만드는가?

---

## 강의 과정 및 문서

전체 강의 자료는 **[문서 웹사이트](https://walkinglabs.github.io/learn-harness-engineering/)**를 방문하세요.

과정은 세 부분으로 나뉩니다:

1. **강의(Lectures)**: Harness engineering 이론을 설명하는 12개의 개념적 단원.
2. **프로젝트(Projects)**: 처음부터 에이전트 작업 공간을 구축하는 6개의 실습 프로젝트.
3. **리소스 라이브러리**: 여러분의 저장소에 오늘 바로 사용할 수 있는 복사 가능 템플릿(`AGENTS.md`, `feature_list.json`, `init.sh` 등).

---

## 빠른 시작: 오늘 바로 에이전트 개선하기

12개의 강의를 모두 읽고 나서 가치를 얻기 시작할 필요가 없습니다. 이미 실제 프로젝트에서 코딩 에이전트를 사용하고 있다면, 지금 당장 개선하는 방법은 다음과 같습니다.

핵심 아이디어는 간단합니다: 프롬프트만 작성하는 대신, 무엇을 해야 하는지, 무엇이 완료되었는지, 작업을 어떻게 검증할지 정의하는 구조화된 파일 세트를 에이전트에 제공하세요. 이 파일들은 저장소 내에 있으므로 모든 세션이 동일한 상태에서 시작합니다.

```text
    YOUR PROJECT ROOT
    ├── AGENTS.md              <-- 에이전트의 운영 매뉴얼
    ├── CLAUDE.md              <-- (대체, Claude Code 사용 시)
    ├── init.sh                <-- 설치 + 검증 + 시작 실행
    ├── feature_list.json      <-- 어떤 기능이 있는지, 무엇이 완료되었는지
    ├── claude-progress.md     <-- 각 세션에서 무슨 일이 있었는지
    └── src/                   <-- 실제 코드
```

[리소스 라이브러리](https://walkinglabs.github.io/learn-harness-engineering/en/resources/)에서 스타터 템플릿을 가져와 프로젝트에 넣으세요. 그게 전부입니다. 네 개의 파일만으로 프롬프트만 사용할 때보다 에이전트 세션이 훨씬 더 안정적일 것입니다.

---

## 캡스톤 프로젝트: 실제 앱

6개의 강좌 프로젝트는 모두 동일한 제품을 중심으로 전개됩니다: **Electron 기반 개인 지식 베이스 데스크톱 앱**.

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

이 프로젝트는 강력한 실용적 가치, 충분한 실제 제품 복잡성, 그리고 하니스 개선 전후를 관찰하기 좋은 환경을 결합하고 있어 선택되었습니다.

각 강좌 프로젝트의 스타터/솔루션은 해당 진화 단계의 Electron 앱 전체 사본입니다. P(N+1)의 스타터는 P(N)의 솔루션에서 파생됩니다 — 앱은 여러분의 하니스 기술이 성장함에 따라 함께 진화합니다.

---

## 학습 경로

이 강좌는 순서대로 진행하도록 설계되었습니다. 각 단계는 이전 단계를 기반으로 구축됩니다.

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

파트타임으로 진행하면 각 단계는 약 1주일이 소요됩니다. 더 빠르게 진행하고 싶다면 1~3단계는 긴 주말에 완료할 수 있습니다.

---

## 강의 개요

### 강의 — 각각 하나의 핵심 질문에 답하는 12개의 개념적 단원

*각 강의의 전체 내용은 [문서 웹사이트](https://walkinglabs.github.io/learn-harness-engineering/)에서 읽을 수 있습니다.*

| 세션 | 질문 | 핵심 아이디어 |
|---------|----------|-----------|
| [L01](../../docs/lectures/lecture-01-why-capable-agents-still-fail/index.md) | 왜 강력한 모델도 실제 작업에서 여전히 실패하는가? | 벤치마크와 실제 엔지니어링 사이의 역량 격차 |
| [L02](../../docs/lectures/lecture-02-what-a-harness-actually-is/index.md) | "하니스"는 실제로 무엇을 의미하는가? | 다섯 가지 하위 시스템: 지시 사항, 상태, 검증, 범위, 수명 주기 |
| [L03](../../docs/lectures/lecture-03-why-the-repository-must-become-the-system-of-record/index.md) | 왜 저장소가 단일 진실 공급원이어야 하는가? | 에이전트가 볼 수 없다면 존재하지 않는 것과 같다 |
| [L04](../../docs/lectures/lecture-04-why-one-giant-instruction-file-fails/index.md) | 왜 거대한 단일 지시 파일은 실패하는가? | 점진적 공개: 백과사전이 아닌 지도를 제공하라 |
| [L05](../../docs/lectures/lecture-05-why-long-running-tasks-lose-continuity/index.md) | 왜 장기 실행 작업은 연속성을 잃는가? | 진행 상황을 디스크에 영속화; 중단된 지점에서 이어하기 |
| [L06](../../docs/lectures/lecture-06-why-initialization-needs-its-own-phase/index.md) | 왜 초기화에 전용 단계가 필요한가? | 에이전트가 작업을 시작하기 전에 환경이 정상인지 확인 |
| [L07](../../docs/lectures/lecture-07-why-agents-overreach-and-under-finish/index.md) | 왜 에이전트는 과도하게 작업하고 불완전하게 마무리하는가? | 한 번에 하나의 기능; 명시적인 완료 정의 |
| [L08](../../docs/lectures/lecture-08-why-feature-lists-are-harness-primitives/index.md) | 왜 기능 목록이 하니스 프리미티브인가? | 에이전트가 무시할 수 없는 기계 판독 가능 범위 경계 |
| [L09](../../docs/lectures/lecture-09-why-agents-declare-victory-too-early/index.md) | 왜 에이전트는 너무 일찍 완료를 선언하는가? | 검증 격차: 자신감 ≠ 정확성 |
| [L10](../../docs/lectures/lecture-10-why-end-to-end-testing-changes-results/index.md) | 왜 엔드투엔드 테스트가 결과를 바꾸는가? | 전체 파이프라인 실행만이 진정한 검증으로 인정된다 |
| [L11](../../docs/lectures/lecture-11-why-observability-belongs-inside-the-harness/index.md) | 왜 관측 가능성이 하니스 내에 있어야 하는가? | 에이전트가 무엇을 했는지 볼 수 없으면, 무엇을 망가뜨렸는지 고칠 수 없다 |
| [L12](../../docs/lectures/lecture-12-why-every-session-must-leave-a-clean-state/index.md) | 왜 모든 세션은 깔끔한 상태를 남겨야 하는가? | 다음 세션의 성공은 이번 세션의 정리에 달려 있다 |

### 프로젝트 — 동일한 Electron 앱에 강의 방법론을 적용하는 6개의 실습 프로젝트

| 프로젝트 | 수행 내용 | 하니스 메커니즘 |
|---------|------------|-------------------|
| [P01](../../docs/projects/project-01-baseline-vs-minimal-harness/index.md) | 동일한 작업을 두 번 실행: 프롬프트만 vs. 규칙 우선 | 최소 하니스: AGENTS.md + init.sh + feature_list.json |
| [P02](../../docs/projects/project-02-agent-readable-workspace/index.md) | 에이전트가 읽을 수 있도록 저장소 재구성 | 에이전트 판독 가능 작업 공간 + 영속적 상태 파일 |
| [P03](../../docs/projects/project-03-multi-session-continuity/index.md) | 에이전트가 중단된 지점에서 이어가도록 만들기 | 진행 로그 + 세션 인계 + 다중 세션 연속성 |
| [P04](../../docs/projects/project-04-incremental-indexing/index.md) | 에이전트가 너무 많거나 너무 적게 작업하지 않도록 방지 | 런타임 피드백 + 범위 제어 + 점진적 인덱싱 |
| [P05](../../docs/projects/project-05-grounded-qa-verification/index.md) | 에이전트가 자신의 작업을 검증하도록 만들기 | 자체 검증 + 근거 기반 Q&A + 증거 기반 완료 |
| [P06](../../docs/projects/project-06-runtime-observability-and-debugging/index.md) | 처음부터 완전한 하니스 구축 (캡스톤) | 전체 하니스: 모든 메커니즘 + 관측 가능성 + 어블레이션 스터디 |

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

### 리소스 라이브러리

- [영어 리소스 라이브러리](https://walkinglabs.github.io/learn-harness-engineering/en/resources/) — 템플릿, 체크리스트, 방법론 참조
- [중국어 리소스 라이브러리](https://walkinglabs.github.io/learn-harness-engineering/zh/resources/) — 中文模板、清单和方法参考
- [러시아어 리소스 라이브러리](https://walkinglabs.github.io/learn-harness-engineering/ru/resources/) — шаблоны, чек-листы и справочники
- [베트남어 리소스 라이브러리](https://walkinglabs.github.io/learn-harness-engineering/vi/resources/) — mẫu, danh sách kiểm tra và tài liệu tham khảo
- [우즈베크어 리소스 라이브러리](https://walkinglabs.github.io/learn-harness-engineering/uz/resources/) — andozalar, tekshiruv ro'yxatlari va ma'lumotnomalar

---

## 에이전트 세션 수명 주기

이 강좌의 핵심 아이디어 중 하나: **에이전트의 세션은 자유 방임이 아닌 구조화된 수명 주기를 따라야 합니다.** 그 모습은 다음과 같습니다:

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

## 이 강좌의 대상

이 강좌는 다음 분들을 위한 것입니다:

- 이미 코딩 에이전트를 사용 중이며 더 나은 안정성과 품질을 원하는 엔지니어
- 하니스 설계에 대한 체계적인 이해를 원하는 연구자 또는 빌더
- 환경 설계가 에이전트 성능에 미치는 영향을 이해해야 하는 기술 리더

이 강좌는 다음 분들에게 적합하지 않습니다:

- 코드 없는 AI 입문을 찾는 분
- 프롬프트에만 관심이 있고 실제 구현을 계획하지 않는 분
- 에이전트가 실제 저장소 내에서 작업하도록 할 준비가 되지 않은 학습자

---

## 요구 사항

이 강좌는 실제로 코딩 에이전트를 실행하는 강좌입니다.

다음 도구 중 최소 하나가 필요합니다:

- Claude Code
- Codex
- 파일 편집, 명령 실행, 다단계 작업을 지원하는 다른 IDE 또는 CLI 코딩 에이전트

이 강좌는 다음이 가능하다고 가정합니다:

- 로컬 저장소 열기
- 에이전트가 파일을 편집하도록 허용
- 에이전트가 명령을 실행하도록 허용
- 출력을 검사하고 작업을 재실행

해당 도구가 없는 경우에도 강좌 내용을 읽을 수 있지만, 의도된 대로 프로젝트를 완료할 수는 없습니다.

---

## 로컬 미리보기

이 저장소는 문서 뷰어로 VitePress를 사용합니다.

```sh
npm install
npm run docs:dev        # 핫 리로드가 포함된 개발 서버
npm run docs:build      # 프로덕션 빌드
npm run docs:preview    # 빌드된 사이트 미리보기
```

그런 다음 브라우저에서 VitePress가 출력하는 로컬 URL을 여세요.

---

## 사전 요구 사항

필수:

- 터미널, git, 로컬 개발 환경에 대한 친숙도
- 최소 하나의 일반적인 애플리케이션 스택에서 코드 읽기 및 쓰기 능력
- 기본적인 소프트웨어 디버깅 경험 (로그, 테스트, 런타임 동작 읽기)
- 구현 중심의 강좌 작업에 투자할 충분한 시간

도움이 되지만 필수는 아님:

- Electron, 데스크톱 앱 또는 로컬 우선 도구에 대한 경험
- 테스팅, 로깅 또는 소프트웨어 아키텍처에 대한 배경지식
- Codex, Claude Code 또는 유사한 코딩 에이전트에 대한 사전 경험

---

## 핵심 참고 자료

주요 자료:

- [OpenAI: Harness engineering: leveraging Codex in an agent-first world](https://openai.com/index/harness-engineering/)
- [Anthropic: Effective harnesses for long-running agents](https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents)
- [Anthropic: Harness design for long-running application development](https://www.anthropic.com/engineering/harness-design-long-running-apps)
- [OpenAI: Unrolling the Codex agent loop](https://openai.com/index/unrolling-the-codex-agent-loop/)
- [Anthropic: Demystifying evals for AI agents](https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents)
- [LangChain: Improving Deep Agents with harness engineering](https://www.langchain.com/blog/improving-deep-agents-with-harness-engineering)
- [Thoughtworks / Martin Fowler: Harness engineering for coding agent users](https://martinfowler.com/articles/harness-engineering.html)
- [Cursor: Continually improving our agent harness](https://cursor.com/blog/continually-improving-agent-harness)

계층화된 전체 참고 문헌 목록은 [`docs/en/resources/reference/`](../../docs/en/resources/reference/index.md)에서 확인하세요.

---

## 저장소 구조

```text
learn-harness-engineering/
├── docs/                          # VitePress 문서 사이트
│   ├── lectures/                  # 12개 강의 (index.md + code/ 예제)
│   │   ├── lecture-01-*/
│   │   ├── lecture-02-*/
│   │   └── ... (총 12개)
│   ├── projects/                  # 6개 프로젝트 설명
│   │   ├── project-01-*/
│   │   └── ... (총 6개)
│   └── resources/                 # 다국어 템플릿 및 참조 자료
│       ├── en/                    # 영어 템플릿, 체크리스트, 가이드
│       ├── zh/                    # 중국어 템플릿, 체크리스트, 가이드
│       ├── ru/                    # 러시아어 템플릿, 체크리스트, 가이드
│       └── vi/                    # 베트남어 템플릿, 체크리스트, 가이드
├── projects/
│   ├── shared/                    # 공유 Electron + TypeScript + React 기반
│   └── project-NN/               # 프로젝트별 starter/ 및 solution/ 디렉토리
├── skills/                        # 재사용 가능한 AI 에이전트 스킬
│   └── harness-creator/           # Harness engineering 스킬
├── package.json                   # VitePress + 개발 도구
└── CLAUDE.md                      # 이 저장소의 Claude Code 지침
```

---

## 강좌 구성 방식

- 각 강의는 하나의 질문에 집중합니다
- 강좌에는 6개의 프로젝트가 포함됩니다
- 모든 프로젝트는 에이전트가 실제 작업을 수행하도록 요구합니다
- 모든 프로젝트는 약한 하니스와 강한 하니스의 결과를 비교합니다
- 중요한 것은 작성된 문서의 양이 아니라 측정된 차이입니다

---

## 스킬

이 저장소에는 IDE나 에이전트 작업 공간에 직접 설치할 수 있는 재사용 가능한 AI 에이전트 스킬도 포함되어 있습니다.

- [**harness-creator**](../../skills/harness-creator/): 몇 분 만에 여러분의 프로젝트에 프로덕션급 하니스를 스캐폴딩하는 스킬.

---

## 다른 강좌

저희 팀은 다른 강좌도 만들었습니다! 확인해 보세요:

[![Hands-on Modern RL](https://img.shields.io/badge/HANDS--ON_MODERN_RL-0052cc?style=for-the-badge)](https://github.com/walkinglabs/hands-on-modern-rl)

**Hands-on Modern RL**: 기본 RL 개념부터 LLM 정렬, RLVR, 고급 에이전트 시스템까지 이어지는 오픈소스 실습 커리큘럼.

---

## 스타 히스토리

[![Star History Chart](https://api.star-history.com/svg?repos=walkinglabs/learn-harness-engineering&type=date&legend=top-left)](https://www.star-history.com/#walkinglabs/learn-harness-engineering&type=date&legend=top-left)

---

## 감사의 글

이 강좌는 [learn-claude-code](https://github.com/shareAI-lab/learn-claude-code)에서 영감을 받고 아이디어를 얻었습니다 — 단일 루프에서 격리된 자율 실행까지, 에이전트를 처음부터 구축하는 점진적 가이드입니다.
