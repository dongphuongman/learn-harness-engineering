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

> **AIコーディングエージェントを確実に動作させるための環境、状態管理、検証、制御メカニズムを構築するプロジェクトベースのコース。**

Learn Harness Engineering は、AIコーディングエージェントのエンジニアリングに特化したコースです。業界最先端の Harness Engineering の理論と実践を深く研究し、統合しました。主な参考文献は以下の通りです：

- [OpenAI: Harness engineering: leveraging Codex in an agent-first world](https://openai.com/index/harness-engineering/)
- [Anthropic: Effective harnesses for long-running agents](https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents)
- [Anthropic: Harness design for long-running application development](https://www.anthropic.com/engineering/harness-design-long-running-apps)
- [Awesome Harness Engineering](https://github.com/walkinglabs/awesome-harness-engineering)

> **すぐに始めたい方へ：** [`skills/harness-creator/`](../../skills/) スキルを使えば、自分のプロジェクト向けに本格的なハーネス（AGENTS.md、機能リスト、init.sh、検証ワークフロー）を数分でスキャフォールドできます。

---

## 目次

- [✨ ビジュアルプレビュー](#-ビジュアルプレビュー)
- [Harness Engineering が本当に意味すること](#harness-engineering-が本当に意味すること)
- [クイックスタート：今日からエージェントを改善する](#クイックスタート今日からエージェントを改善する)
- [カプロジェクト：実際のアプリケーション](#カプロジェクト実際のアプリケーション)
- [学習パス](#学習パス)
- [シラバス](#シラバス)
- [スキル](#スキル)
- [その他のコース](#その他のコース)

---

## ✨ ビジュアルプレビュー

### 🏠 コースホームページ
> 包括的なコース概要とコア思想の紹介により、明確なスタートパスを提供します。

![コースホームページプレビュー](../../docs/public/screenshots/readme/zh-home.png)

### 📖 没入型レクチャー
> 実際の課題とハンズオンプロジェクト（プロジェクト01など）の深い解説により、没入型の学習体験を提供します。

![コースレクチャープレビュー](../../docs/public/screenshots/readme/zh-lecture-01.png)

### 🗂️ すぐに使えるリソースライブラリ
> マルチターンAIエージェント開発における一般的な落とし穴（コンテキストの損失やタスクの早期完了など）を解決するために設計されたテンプレートと参照設定。

![リソースライブラリプレビュー](../../docs/public/screenshots/readme/zh-resources.png)

## PDF コースブック

このリポジトリには、コースコンテンツの PDF ビルドパイプラインが含まれています。

- `npm run pdf:build` を実行して、英語と中国語の PDF をローカルで生成します。
- 出力ファイルは `artifacts/pdfs/` に書き込まれます。
- README プレビュー画像を更新したい場合は、`npm run screenshots:readme` を実行してください。
- GitHub Actions ワークフロー [`release-course-pdfs.yml`](../../.github/workflows/release-course-pdfs.yml) は PDF をビルドし、GitHub Releases に公開できます。

---

## モデルは賢い、ハーネスがそれを確実にする

ほとんどの人が痛い目を見て学ぶ厳しい真実があります：**世界最強のモデルであっても、周囲に適切な環境を構築しなければ、実際のエンジニアリングタスクでは失敗します。**

あなたも経験したことがあるかもしれません。Claude や GPT にリポジトリでタスクを与えます。最初はうまくいきます — ファイルを読み、コードを書き、生産的に見えます。しかし、どこかで問題が発生します。ステップを飛ばします。テストを壊します。「完了」と言いますが、実際には何も動いていません。自分でやった以上に修正に時間を費やすことになります。

これはモデルの問題ではありません。ハーネスの問題です。

証拠は明確です。Anthropic は対照実験を行いました：同じモデル（Opus 4.5）、同じプロンプト（「2Dレトロゲームエディタを構築して」）。ハーネスなしでは、20分で9ドル使って動かないものを生成しました。フルハーネス（プランナー + ジェネレーター + エバリュエーター）では、6時間で200ドル使って実際に遊べるゲームを構築しました。モデルは変わっていません。ハーネスが変わったのです。

OpenAI も Codex で同じことを報告しています：適切にハーネスされたリポジトリでは、同じモデルが「信頼性なし」から「信頼性あり」になります。わずかな改善ではなく、質的な変化です。

**このコースは、その環境の構築方法を教えます。**

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

## Harness Engineering が本当に意味すること

Harness Engineering は、モデルの周囲に完全な作業環境を構築し、信頼性の高い結果を生成させることです。より良いプロンプトを書くことではありません。モデルが内部で動作するシステムを設計することです。

ハーネスには5つのサブシステムがあります：

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

各サブシステムには一つの役割があります：

- **Instructions** — エージェントに何を、どの順序で、開始前に何を読むべきかを伝えます。一つの巨大なファイルではなく、エージェントが必要に応じてナビゲートする段階的開示構造です。
- **State** — 何が完了し、何が進行中で、何が次かを追跡します。ディスクに永続化され、次のセッションは前回の続きから正確に再開できます。
- **Verification** — 合格したテストスイートのみが証拠として認められます。エージェントは実行可能な証拠なしに完了を宣言できません。
- **Scope** — エージェントを一度に一つの機能に制約します。過剰な範囲拡大なし。3つのことを中途半端に終わらせることなし。未完了の作業を隠すために機能リストを書き換えることなし。
- **Session Lifecycle** — 開始時に初期化。終了時にクリーンアップ。次のセッションのためのクリーンな再起動パスを残します。

---

## なぜこのコースが存在するのか

問題は「モデルはコードを書けるか？」ではありません。書けます。問題は：**実際のリポジトリ内で、複数のセッションにわたり、常に人間の監視なしに、実際のエンジニアリングタスクを確実に完了できるか？** ということです。

現時点での答えは：ハーネスなしでは無理です。

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

このコースが本当に重視している問い：

- どのハーネス設計がタスク完了率を向上させるか？
- どの設計が手戻りや誤った完了を減らすか？
- どのメカニズムが長時間実行タスクを着実に進行させるか？
- どの構造が複数回のエージェント実行後もシステムを保守可能に保つか？

---

## コースカリキュラムとドキュメント

完全なコース資料については、**[ドキュメントウェブサイト](https://walkinglabs.github.io/learn-harness-engineering/)** をご覧ください。

カリキュラムは3つの部分に分かれています：

1. **レクチャー**：Harness Engineering の背景理論を説明する12の概念ユニット。
2. **プロジェクト**：ゼロからエージェントワークスペースを構築する6つのハンズオンプロジェクト。
3. **リソースライブラリ**：自分のリポジトリで今日すぐ使えるコピー用テンプレート（`AGENTS.md`、`feature_list.json`、`init.sh` など）。

---

## クイックスタート：今日からエージェントを改善する

価値を得るために12のレクチャーをすべて読む必要はありません。すでに実際のプロジェクトでコーディングエージェントを使用している場合、今すぐ改善する方法は以下の通りです。

アイデアはシンプルです：プロンプトを書く代わりに、何をすべきか、何が完了しているか、作業をどう検証するかを定義する構造化ファイルのセットをエージェントに与えます。これらのファイルはリポジトリ内に存在するため、すべてのセッションが同じ状態から始まります。

```text
    YOUR PROJECT ROOT
    ├── AGENTS.md              <-- エージェントの操作マニュアル
    ├── CLAUDE.md              <-- （代替、Claude Code を使用する場合）
    ├── init.sh                <-- install + verify + start を実行
    ├── feature_list.json      <-- 存在する機能、完了している機能
    ├── claude-progress.md     <-- 各セッションで何が起きたか
    └── src/                   <-- 実際のコード
```

[リソースライブラリ](https://walkinglabs.github.io/learn-harness-engineering/en/resources/)からスターターテンプレートを取得し、プロジェクトに配置してください。たったこれだけです。4つのファイルで、プロンプトだけで実行するよりもエージェントセッションが大幅に安定します。

---

## カプロジェクト：実際のアプリケーション

6つのコースプロジェクトはすべて同じ製品を中心に展開しています：**Electron ベースの個人ナレッジベースデスクトップアプリ**です。

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

このプロジェクトが選ばれたのは、実用的な価値、十分な現実世界の製品複雑さ、ハーネス改善の前後を観察するのに適した設定を組み合わせているからです。

各コースプロジェクトのスターター/ソリューションは、その進化段階におけるこの Electron アプリの完全なコピーです。P(N+1) のスターターは P(N) のソリューションから派生します — アプリはあなたのハーネスキルの成長とともに進化します。

---

## 学習パス

このコースは順番に進めるように設計されています。各フェーズは前のフェーズの上に構築されます。

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

パートタイムで進める場合、各フェーズは約1週間です。より速く進めたい場合、フェーズ1〜3は長い週末で完了できます。

---

## シラバス

### レクチャー — 12の概念ユニット、それぞれが一つのコアな問いに答える

*各レクチャーの全文は[ドキュメントウェブサイト](https://walkinglabs.github.io/learn-harness-engineering/)で読めます。*

| セッション | 問い | コアアイデア |
|---------|----------|-----------|
| [L01](../../docs/lectures/lecture-01-why-capable-agents-still-fail/index.md) | なぜ強力なモデルでも実際のタスクで失敗するのか？ | ベンチマークと実際のエンジニアリングの能力格差 |
| [L02](../../docs/lectures/lecture-02-what-a-harness-actually-is/index.md) | 「ハーネス」とは実際何を意味するのか？ | 5つのサブシステム：インストラクション、状態、検証、スコープ、ライフサイクル |
| [L03](../../docs/lectures/lecture-03-why-the-repository-must-become-the-system-of-record/index.md) | なぜリポジトリが唯一の信頼できる情報源でなければならないのか？ | エージェントが見られないものは存在しない |
| [L04](../../docs/lectures/lecture-04-why-one-giant-instruction-file-fails/index.md) | なぜ一つの巨大な指示ファイルは失敗するのか？ | 段階的開示：百科事典ではなく地図を与える |
| [L05](../../docs/lectures/lecture-05-why-long-running-tasks-lose-continuity/index.md) | なぜ長時間実行タスクは連続性を失うのか？ | 進捗をディスクに永続化し、前回の続きから再開する |
| [L06](../../docs/lectures/lecture-06-why-initialization-needs-its-own-phase/index.md) | なぜ初期化に独自のフェーズが必要なのか？ | エージェントが作業を開始する前に環境が健全であることを確認する |
| [L07](../../docs/lectures/lecture-07-why-agents-overreach-and-under-finish/index.md) | なぜエージェントは過剰に手を出し、不足して終わるのか？ | 一度に一つの機能、明確な完了の定義 |
| [L08](../../docs/lectures/lecture-08-why-feature-lists-are-harness-primitives/index.md) | なぜ機能リストはハーネスのプリミティブなのか？ | エージェントが無視できない機械可読なスコープ境界 |
| [L09](../../docs/lectures/lecture-09-why-agents-declare-victory-too-early/index.md) | なぜエージェントは早すぎる完了を宣言するのか？ | 検証のギャップ：確信 ≠ 正確性 |
| [L10](../../docs/lectures/lecture-10-why-end-to-end-testing-changes-results/index.md) | なぜエンドツーエンドテストが結果を変えるのか？ | 完全なパイプライン実行のみが本当の検証として認められる |
| [L11](../../docs/lectures/lecture-11-why-observability-belongs-inside-the-harness/index.md) | なぜオブザーバビリティはハーネス内にあるべきなのか？ | エージェントが何をしたか見えなければ、何を壊したか修正できない |
| [L12](../../docs/lectures/lecture-12-why-every-session-must-leave-a-clean-state/index.md) | なぜすべてのセッションがクリーンな状態を残さなければならないのか？ | 次のセッションの成功は、このセッションのクリーンアップに依存する |

### プロジェクト — レクチャーの手法を同じ Electron アプリに適用する6つのハンズオンプロジェクト

| プロジェクト | やること | ハーネスメカニズム |
|---------|------------|-------------------|
| [P01](../../docs/projects/project-01-baseline-vs-minimal-harness/index.md) | 同じタスクを2回実行：プロンプトのみ vs. ルール優先 | 最小ハーネス：AGENTS.md + init.sh + feature_list.json |
| [P02](../../docs/projects/project-02-agent-readable-workspace/index.md) | エージェントが読めるようにリポジトリを再構築する | エージェント可読ワークスペース + 永続状態ファイル |
| [P03](../../docs/projects/project-03-multi-session-continuity/index.md) | エージェントが前回の続きから再開できるようにする | 進捗ログ + セションハンドオフ + マルチセッション連続性 |
| [P04](../../docs/projects/project-04-incremental-indexing/index.md) | エージェントがやりすぎたり、やらなすぎたりするのを防ぐ | ランタイムフィードバック + スコープ制御 + インクリメンタルインデキシング |
| [P05](../../docs/projects/project-05-grounded-qa-verification/index.md) | エージェントが自分の作業を検証するようにする | 自己検証 + グラウンデッドQ&A + 証拠ベースの完了 |
| [P06](../../docs/projects/project-06-runtime-observability-and-debugging/index.md) | ゼロから完全なハーネスを構築する（カプロジェクト） | フルハーネス：全メカニズム + オブザーバビリティ + アブレーションスタディ |

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

### リソースライブラリ

- [英語リソースライブラリ](https://walkinglabs.github.io/learn-harness-engineering/en/resources/) — テンプレート、チェックリスト、方法論リファレンス
- [中国語リソースライブラリ](https://walkinglabs.github.io/learn-harness-engineering/zh/resources/) — 中文模板、清单和方法参考
- [ロシア語リソースライブラリ](https://walkinglabs.github.io/learn-harness-engineering/ru/resources/) — шаблоны, чек-листы и справочники
- [ベトナム語リソースライブラリ](https://walkinglabs.github.io/learn-harness-engineering/vi/resources/) — mẫu, danh sách kiểm tra và tài liệu tham khảo

---

## エージェントセッションライフサイクル

このコースのコアアイデアの一つ：**エージェントのセッションは自由放任ではなく、構造化されたライフサイクルに従うべきです。** どのようなものか：

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

## 対象者

このコースは以下の方を対象としています：

- コーディングエージェントをすでに使用しており、安定性と品質を向上させたいエンジニア
- ハーネス設計の体系的な理解を求める研究者やビルダー
- 環境設計がエージェントのパフォーマンスにどう影響するかを理解する必要があるテックリード

このコースは以下の方を対象としていません：

- ゼロコードの AI 入門を求める方
- プロンプトにしか関心がなく、実際の実装を構築する予定のない方
- エージェントを実際のリポジトリ内で動かす準備ができていない学習者

---

## 必要なツール

このコースでは実際にコーディングエージェントを動かします。

以下のツールのうち少なくとも1つが必要です：

- Claude Code
- Codex
- ファイル編集、コマンド実行、マルチステップタスクをサポートする他の IDE または CLI コーディングエージェント

このコースでは以下ができることを前提としています：

- ローカルリポジトリを開く
- エージェントにファイルの編集を許可する
- エージェントにコマンドの実行を許可する
- 出力を確認し、タスクを再実行する

このようなツールがない場合でも、コースコンテンツを読むことはできますが、プロジェクトを意図通りに完了することはできません。

---

## ローカルプレビュー

このリポジトリは VitePress をドキュメントビューアとして使用しています。

```sh
npm install
npm run docs:dev        # ホットリロード付き開発サーバー
npm run docs:build      # プロダクションビルド
npm run docs:preview    # ビルド済みサイトのプレビュー
```

その後、VitePress が出力するローカル URL をブラウザで開いてください。

---

## 前提条件

必須：

- ターミナル、git、ローカル開発環境に慣れていること
- 少なくとも1つの一般的なアプリケーションスタックでコードの読み書きができること
- 基本的なソフトウェアデバッグ経験（ログ、テスト、ランタイム動作の読み取り）
- 実装重視のコースワークに十分な時間を投入できること

あれば役立つが必須ではない：

- Electron、デスクトップアプリ、ローカルファーストツールの経験
- テスト、ロギング、ソフトウェアアーキテクチャの背景知識
- Codex、Claude Code、または類似のコーディングエージェントの使用経験

---

## 主な参考文献

主要：

- [OpenAI: Harness engineering: leveraging Codex in an agent-first world](https://openai.com/index/harness-engineering/)
- [Anthropic: Effective harnesses for long-running agents](https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents)
- [Anthropic: Harness design for long-running application development](https://www.anthropic.com/engineering/harness-design-long-running-apps)
- [OpenAI: Unrolling the Codex agent loop](https://openai.com/index/unrolling-the-codex-agent-loop/)
- [Anthropic: Demystifying evals for AI agents](https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents)
- [LangChain: Improving Deep Agents with harness engineering](https://www.langchain.com/blog/improving-deep-agents-with-harness-engineering)
- [Thoughtworks / Martin Fowler: Harness engineering for coding agent users](https://martinfowler.com/articles/harness-engineering.html)
- [Cursor: Continually improving our agent harness](https://cursor.com/blog/continually-improving-agent-harness)

完全な階層別参考文献リストは [`docs/en/resources/reference/`](../../docs/en/resources/reference/index.md) をご覧ください。

---

## リポジトリ構造

```text
learn-harness-engineering/
├── docs/                          # VitePress ドキュメントサイト
│   ├── lectures/                  # 12のレクチャー（index.md + code/ 例）
│   │   ├── lecture-01-*/
│   │   ├── lecture-02-*/
│   │   └── ... (全12)
│   ├── projects/                  # 6つのプロジェクト説明
│   │   ├── project-01-*/
│   │   └── ... (全6)
│   └── resources/                 # 多言語テンプレートとリファレンス
│       ├── en/                    # 英語テンプレート、チェックリスト、ガイド
│       ├── zh/                    # 中国語テンプレート、チェックリスト、ガイド
│       ├── ru/                    # ロシア語テンプレート、チェックリスト、ガイド
│       └── vi/                    # ベトナム語テンプレート、チェックリスト、ガイド
├── projects/
│   ├── shared/                    # 共有 Electron + TypeScript + React 基盤
│   └── project-NN/               # プロジェクトごとの starter/ と solution/ ディレクトリ
├── skills/                        # 再利用可能な AI エージェントスキル
│   └── harness-creator/           # Harness Engineering スキル
├── package.json                   # VitePress + 開発ツール
└── CLAUDE.md                      # このリポジトリの Claude Code 指示
```

---

## コースの構成

- 各レクチャーは一つの問いに焦点を当てる
- コースには6つのプロジェクトが含まれる
- すべてのプロジェクトでエージェントが実際の作業を行う
- すべてのプロジェクトで弱いハーネスと強いハーネスの結果を比較する
- 重要なのは測定された差であり、書かれたドキュメントの数ではない

---

## スキル

このリポジトリには、IDE やエージェントワークスペースに直接インストールできる再利用可能な AI エージェントスキルも含まれています。

- [**harness-creator**](../../skills/harness-creator/): 自分のプロジェクト向けに本格的なハーネスを数分でスキャフォールドするスキル。

---

## その他のコース

私たちのチームは他のコースも作成しています！ぜひご覧ください：

[![Hands-on Modern RL](https://img.shields.io/badge/HANDS--ON_MODERN_RL-0052cc?style=for-the-badge)](https://github.com/walkinglabs/hands-on-modern-rl)

**Hands-on Modern RL**：基本的な強化学習の概念から LLM アライメント、RLVR、高度なエージェントシステムまでをつなぐ、オープンソースのハンズオンカリキュラム。

---

## スター履歴

[![Star History Chart](https://api.star-history.com/svg?repos=walkinglabs/learn-harness-engineering&type=date&legend=top-left)](https://www.star-history.com/#walkinglabs/learn-harness-engineering&type=date&legend=top-left)

---

## 謝辞

このコースは [learn-claude-code](https://github.com/shareAI-lab/learn-claude-code) にインスピレーションを受け、アイデアを得ています — 単一のループから独立した自律実行まで、ゼロからエージェントを構築する段階的ガイド。
