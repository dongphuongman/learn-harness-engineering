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

# تعلّم هندسة الحزام (Learn Harness Engineering)

> **دورة تعليمية قائمة على المشاريع حول بناء البيئة وإدارة الحالة وآليات التحقق والتحكم التي تجعل وكلاء البرمجة بالذكاء الاصطناعي يعملون بشكل موثوق.**

تعلّم هندسة الحزام (Learn Harness Engineering) هي دورة تعليمية مكرّسة لهندسة وكلاء البرمجة بالذكاء الاصطناعي. لقد قمنا بدراسة وتوليف أحدث نظريات وممارسات هندسة الحزام في الصناعة بعمق. تشمل مراجعنا الأساسية:

- [OpenAI: Harness engineering: leveraging Codex in an agent-first world](https://openai.com/index/harness-engineering/)
- [Anthropic: Effective harnesses for long-running agents](https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents)
- [Anthropic: Harness design for long-running application development](https://www.anthropic.com/engineering/harness-design-long-running-apps)
- [Awesome Harness Engineering](https://github.com/walkinglabs/awesome-harness-engineering)

> **تبدأ سريعاً؟** مهارة [`skills/harness-creator/`](../../skills/) يمكن أن تساعدك في إنشاء حزام بمستوى الإنتاج (AGENTS.md، قوائم الميزات، init.sh، سير عمل التحقق) لمشروعك الخاص في دقائق.

---

## جدول المحتويات

- [✨ معاينة بصرية](#-معاينة-بصرية)
- [ما تعنيه هندسة الحزام فعلياً](#ما-تعنيه-هندسة-الحزام-فعليا)
- [ابدأ بسرعة: حسّن وكيلك اليوم](#ابدأ-بسرعة-حسّن-وكيلك-اليوم)
- [مشروع التخرج: تطبيق حقيقي](#مشروع-التخرج-تطبيق-حقيقي)
- [مسار التعلم](#مسار-التعلم)
- [المنهج الدراسي](#المنهج-الدراسي)
- [المهارات](#المهارات)
- [دورات أخرى](#دورات-أخرى)

---

## ✨ معاينة بصرية

### 🏠 الصفحة الرئيسية للدورة
> مخطط شامل للدورة ومقدمة للفلسفات الأساسية، توفر مساراً واضحاً للبدء.

![معاينة الصفحة الرئيسية للدورة](../../docs/public/screenshots/readme/zh-home.png)

### 📖 محاضرات تفاعلية
> غوص عميق في نقاط الألم الواقعية ومشاريع عملية (مثل المشروع 01) لتجربة تعليمية تفاعلية.

![معاينة محاضرة الدورة](../../docs/public/screenshots/readme/zh-lecture-01.png)

### 🗂️ مكتبة موارد جاهزة للاستخدام
> قوالب وتكوينات مرجعية مصممة لحل المشكلات الشائعة في تطوير وكلاء الذكاء الاصطناعي متعددة الأدوار، مثل فقدان السياق والإنهاء المبكر للمهام.

![معاينة مكتبة الموارد](../../docs/public/screenshots/readme/zh-resources.png)

## كتيبات الدورة بصيغة PDF

يحتوي هذا المستودع الآن على خط أنابيب لبناء كتيبات الدورة بصيغة PDF.

- شغّل `npm run pdf:build` لتوليد ملفات PDF باللغتين الإنجليزية والصينية محلياً.
- تُكتب ملفات المخرجات إلى `artifacts/pdfs/`.
- شغّل `npm run screenshots:readme` إذا كنت تريد تحديث صور معاينة README.
- سير عمل GitHub Actions [`release-course-pdfs.yml`](../../.github/workflows/release-course-pdfs.yml) يمكنه بناء ملفات PDF ونشرها على GitHub Releases.

---

## النموذج ذكي، الحزام يجعله موثوقاً

هناك حقيقة قاسية يتعلمها معظم الناس بالطريقة الصعبة: **أقوى نموذج في العالم سيفشل في مهام الهندسة الحقيقية إذا لم تبني بيئة مناسبة حوله.**

ربما رأيت هذا بنفسك. تعطي Claude أو GPT مهمة في مستودعك. يبدأ بشكل جيد — يقرأ الملفات، يكتب الكود، يبدو منتجاً. ثم يحدث خطأ ما. يتخطى خطوة. يكسر اختباراً. يقول "تم" لكن لا شيء يعمل فعلياً. تقضي وقتاً أطول في الإصلاح مما لو كنت فعلت ذلك بنفسك.

هذه ليست مشكلة نموذج. إنها مشكلة حزام.

الدليل واضح. أجرت Anthropic تجربة محكومة: نفس النموذج (Opus 4.5)، نفس الموجه ("بناء محرر ألعاب ريترو ثنائي الأبعاد"). بدون حزام، أنفق 9 دولارات في 20 دقيقة وأنتج شيئاً لا يعمل. مع حزام كامل (مخطط + مولّد + مقيّم)، أنفق 200 دولار في 6 ساعات وبنى لعبة يمكنك اللعب بها فعلياً. النموذج لم يتغير. الحزام هو الذي تغيّر.

أبلغت OpenAI عن الشيء نفسه مع Codex: في مستودع مزود بحزام جيد، ينتقل نفس النموذج من "غير موثوق" إلى "موثوق." ليس تحسناً هامشياً — بل تحولاً نوعياً.

**هذه الدورة تعلّمك كيف تبني تلك البيئة.**

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

## ما تعنيه هندسة الحزام فعلياً

هندسة الحزام تدور حول بناء بيئة عمل كاملة حول النموذج حتى ينتج نتائج موثوقة. الأمر لا يتعلق بكتابة موجهات أفضل. بل يتعلق بتصميم النظام الذي يعمل النموذج داخله.

يتكون الحزام من خمس أنظمة فرعية:

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

لكل نظام فرعي وظيفة واحدة:

- **التعليمات** — تخبر الوكيل بما يجب فعله، بأي ترتيب، وما يجب قراءته قبل البدء. ليس ملفاً ضخماً واحداً؛ بل هيكل إفصاح تدريجي يتنقل فيه الوكيل حسب الحاجة.
- **الحالة** — تتبع ما تم إنجازه، ما قيد التنفيذ، وما هو التالي. محفوظة على القرص حتى تلتقط الجلسة التالية من حيث توقفت الجلسة السابقة تماماً.
- **التحقق** — مجموعة اختبارات ناجحة فقط تُحسب كدليل. لا يمكن للوكيل إعلان النصر بدون دليل قابل للتشغيل.
- **النطاق** — تقييد الوكيل بميزة واحدة في كل مرة. لا تجاوز. لا إنهاء نصف ثلاثة أشياء. لا إعادة كتابة قائمة الميزات لإخفاء العمل غير المنجز.
- **دورة حياة الجلسة** — التهيئة في البداية. التنظيف في النهاية. ترك مسار إعادة تشغيل نظيف للجلسة التالية.

---

## لماذا توجد هذه الدورة

السؤال ليس "هل يمكن للنماذج كتابة الكود؟" يمكنها ذلك. السؤال هو: **هل يمكنها إكمال مهام هندسية حقيقية بشكل موثوق داخل مستودعات حقيقية، عبر جلسات متعددة، بدون إشراف بشري مستمر؟**

حالياً، الإجابة هي: ليس بدون حزام.

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

الأسئلة التي تهتم بها هذه الدورة فعلياً:

- أي تصاميم حزام تحسّن معدلات إكمال المهام؟
- أي تصاميم تقلل إعادة العمل والإكمالات غير الصحيحة؟
- أي آليات تحافظ على تقدم المهام طويلة التشغيل بشكل ثابت؟
- أي هياكل تحافظ على قابلية صيانة النظام بعد عمليات تشغيل وكيل متعددة؟

---

## المنهج الدراسي والتوثيق

للحصول على مواد الدورة الكاملة، يرجى زيارة **[موقع التوثيق](https://walkinglabs.github.io/learn-harness-engineering/)**.

ينقسم المنهج إلى ثلاثة أجزاء:

1. **المحاضرات**: 12 وحدة مفاهيمية تشرح النظرية وراء هندسة الحزام.
2. **المشاريع**: 6 مشاريع عملية حيث تبني مساحة عمل وكيلية من الصفر.
3. **مكتبة الموارد**: قوالب جاهزة للنسخ (`AGENTS.md`، `feature_list.json`، `init.sh`، إلخ) لاستخدامها في مستودعاتك الخاصة اليوم.

---

## ابدأ بسرعة: حسّن وكيلك اليوم

لا تحتاج إلى قراءة جميع المحاضرات الـ 12 قبل أن تبدأ في الحصول على قيمة. إذا كنت تستخدم بالفعل وكيل برمجة في مشروع حقيقي، إليك كيفية تحسينه الآن.

الفكرة بسيطة: بدلاً من مجرد كتابة الموجهات، أعطِ وكيلك مجموعة من الملفات المنظمة التي تحدد ما يجب فعله، ما تم إنجازه، وكيفية التحقق من العمل. هذه الملفات تعيش داخل مستودعك، لذا تبدأ كل جلسة من نفس الحالة.

```text
    YOUR PROJECT ROOT
    ├── AGENTS.md              <-- the agent's operating manual
    ├── CLAUDE.md              <-- (alternative, if using Claude Code)
    ├── init.sh                <-- runs install + verify + start
    ├── feature_list.json      <-- what features exist, which are done
    ├── claude-progress.md     <-- what happened each session
    └── src/                   <-- your actual code
```

احصل على القوالب الأولية من [مكتبة الموارد](https://walkinglabs.github.io/learn-harness-engineering/en/resources/) وأضفها إلى مشروعك. هذا كل شيء. أربعة ملفات، وستكون جلسات وكيلك أكثر استقراراً بشكل ملحوظ مقارنة بالاعتماد على الموجهات وحدها.

---

## مشروع التخرج: تطبيق حقيقي

جميع مشاريع الدورة الستة تدور حول نفس المنتج: **تطبيق سطح مكتب لقاعدة المعرفة الشخصية مبني على Electron**.

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

تم اختيار هذا المشروع لأنه يجمع بين قيمة عملية قوية، تعقيد كافٍ في المنتج الحقيقي، وبيئة جيدة لمراقبة تحسينات الحزام قبل وبعد.

كل ملف بدء/حل لمشروع في الدورة هو نسخة كاملة من تطبيق Electron في تلك المرحلة التطورية. ملف بدء P(N+1) مشتق من حل P(N) — التطبيق يتطور مع نمو مهاراتك في الحزام.

---

## مسار التعلم

الدورة مصممة لتُنفذ بالترتيب. كل مرحلة تبني على سابقتها.

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

كل مرحلة تستغرق حوالي أسبوع إذا كنت تعمل بدوام جزئي. إذا كنت تريد السرعة، يمكن إنجاز المراحل 1-3 في عطلة نهاية أسبوع طويلة.

---

## المنهج الدراسي

### المحاضرات — 12 وحدة مفاهيمية، كل منها يجيب عن سؤال أساسي واحد

*اقرأ النص الكامل لكل محاضرة على [موقع التوثيق](https://walkinglabs.github.io/learn-harness-engineering/).*

| الجلسة | السؤال | الفكرة الأساسية |
|---------|--------|-----------------|
| [L01](../../docs/lectures/lecture-01-why-capable-agents-still-fail/index.md) | لماذا تفشل النماذج القوية في المهام الحقيقية؟ | الفجوة في القدرة بين المعايير القياسية والهندسة الحقيقية |
| [L02](../../docs/lectures/lecture-02-what-a-harness-actually-is/index.md) | ماذا يعني "الحزام" فعلياً؟ | خمسة أنظمة فرعية: التعليمات، الحالة، التحقق، النطاق، دورة الحياة |
| [L03](../../docs/lectures/lecture-03-why-the-repository-must-become-the-system-of-record/index.md) | لماذا يجب أن يكون المستودع هو المصدر الوحيد للحقيقة؟ | إذا لم يستطع الوكيل رؤيته، فهو غير موجود |
| [L04](../../docs/lectures/lecture-04-why-one-giant-instruction-file-fails/index.md) | لماذا يفشل ملف التعليمات الضخم الواحد؟ | الإفصاح التدريجي: أعط خريطة، لا موسوعة |
| [L05](../../docs/lectures/lecture-05-why-long-running-tasks-lose-continuity/index.md) | لماذا تفقد المهام طويلة التشغيل الاستمرارية؟ | احفظ التقدم على القرص؛ التقط من حيث توقفت |
| [L06](../../docs/lectures/lecture-06-why-initialization-needs-its-own-phase/index.md) | لماذا تحتاج التهيئة إلى مرحلة خاصة بها؟ | تحقق من صحة البيئة قبل أن يبدأ الوكيل العمل |
| [L07](../../docs/lectures/lecture-07-why-agents-overreach-and-under-finish/index.md) | لماذا يتجاوز الوكلاء الحدود وينهون أعمالاً بشكل ناقص؟ | ميزة واحدة في كل مرة؛ تعريف صريح للإتمام |
| [L08](../../docs/lectures/lecture-08-why-feature-lists-are-harness-primitives/index.md) | لماذا تُعد قوائم الميزات عناصر أساسية للحزام؟ | حدود نطاق قابلة للقراءة آلياً لا يمكن للوكيل تجاهلها |
| [L09](../../docs/lectures/lecture-09-why-agents-declare-victory-too-early/index.md) | لماذا يعلن الوكلاء النصر مبكراً جداً؟ | فجوات التحقق: الثقة ≠ الصحة |
| [L10](../../docs/lectures/lecture-10-why-end-to-end-testing-changes-results/index.md) | لماذا يغيّر الاختبار من طرف إلى طرف النتائج؟ | تشغيل خط أنابيب كامل فقط يُحسب كتحقق حقيقي |
| [L11](../../docs/lectures/lecture-11-why-observability-belongs-inside-the-harness/index.md) | لماذا تنتمي قابلية الملاحظة داخل الحزام؟ | إذا لم تستطع رؤية ما فعله الوكيل، لا يمكنك إصلاح ما أفسده |
| [L12](../../docs/lectures/lecture-12-why-every-session-must-leave-a-clean-state/index.md) | لماذا يجب أن تترك كل جلسة حالة نظيفة؟ | نجاح الجلسة التالية يعتمد على تنظيف هذه الجلسة |

### المشاريع — 6 مشاريع عملية تطبق طرق المحاضرات على نفس تطبيق Electron

| المشروع | ماذا تفعل | آلية الحزام |
|---------|-----------|-------------|
| [P01](../../docs/projects/project-01-baseline-vs-minimal-harness/index.md) | شغّل نفس المهمة مرتين: بالموجهات فقط مقابل القواعد أولاً | حزام أدنى: AGENTS.md + init.sh + feature_list.json |
| [P02](../../docs/projects/project-02-agent-readable-workspace/index.md) | أعد هيكلة المستودع ليتمكن الوكيل من قراءته | مساحة عمل قابلة للقراءة بواسطة الوكيل + ملفات حالة مستمرة |
| [P03](../../docs/projects/project-03-multi-session-continuity/index.md) | اجعل الوكيل يلتقط من حيث توقف | سجل التقدم + تسليم الجلسة + استمرارية متعددة الجلسات |
| [P04](../../docs/projects/project-04-incremental-indexing/index.md) | أوقف الوكيل عن القيام بالكثير جداً أو القليل جداً | ملاحظات وقت التشغيل + التحكم في النطاق + الفهرسة التدريجية |
| [P05](../../docs/projects/project-05-grounded-qa-verification/index.md) | اجعل الوكيل يتحقق من عمله بنفسه | التحقق الذاتي + أسئلة وأجوبة مبنية على أدلة + إكمال قائم على الأدلة |
| [P06](../../docs/projects/project-06-runtime-observability-and-debugging/index.md) | ابنِ حزاماً كاملاً من الصفر (مشروع التخرج) | حزام كامل: جميع الآليات + قابلية الملاحظة + دراسة الاستئصال |

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

### مكتبة الموارد

- [مكتبة الموارد بالإنجليزية](https://walkinglabs.github.io/learn-harness-engineering/en/resources/) — قوالب، قوائم مراجعة، ومراجع منهجية
- [مكتبة الموارد بالصينية](https://walkinglabs.github.io/learn-harness-engineering/zh/resources/) — 中文模板、清单和方法参考
- [مكتبة الموارد بالروسية](https://walkinglabs.github.io/learn-harness-engineering/ru/resources/) — шаблоны, чек-листы и справочники
- [مكتبة الموارد بالفيتنامية](https://walkinglabs.github.io/learn-harness-engineering/vi/resources/) — mẫu, danh sách kiểm tra và tài liệu tham khảo

---

## دورة حياة جلسة الوكيل

إحدى الأفكار الأساسية في هذه الدورة: **يجب أن تتبع جلسة الوكيل دورة حياة منظمة، وليست عشوائية.** إليك كيف تبدو:

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

## لمن هذه الدورة

هذه الدورة موجهة لـ:

- المهندسين الذين يستخدمون بالفعل وكلاء البرمجة ويرغبون في تحسين الاستقرار والجودة
- الباحثين أو البناة الذين يريدون فهماً منهجياً لتصميم الحزام
- قادة التكنولوجيا الذين يحتاجون لفهم كيف يؤثر تصميم البيئة على أداء الوكيل

هذه الدورة ليست لـ:

- الأشخاص الذين يبحثون عن مقدمة للذكاء الاصطناعي بدون كود
- الأشخاص الذين يهتمون فقط بالموجهات ولا يخططون لبناء تطبيقات حقيقية
- المتعلمين غير المستعدين للسماح للوكلاء بالعمل داخل مستودعات حقيقية

---

## المتطلبات

هذه دورة حيث تقوم بتشغيل وكلاء البرمجة فعلياً.

تحتاج إلى واحد على الأقل من هذه الأدوات:

- Claude Code
- Codex
- وكيل برمجة IDE أو سطر أوامر آخر يدعم تعديل الملفات وتنفيذ الأوامر والمهام متعددة الخطوات

تفترض الدورة أنك تستطيع:

- فتح مستودع محلي
- السماح للوكيل بتعديل الملفات
- السماح للوكيل بتشغيل الأوامر
- فحص المخرجات وإعادة تشغيل المهام

إذا لم تكن لديك هذه الأداة، لا يزال بإمكانك قراءة محتوى الدورة، لكن لن تتمكن من إكمال المشاريع كما هو مقصود.

---

## المعاينة المحلية

يستخدم هذا المستودع VitePress كعارض للتوثيق.

```sh
npm install
npm run docs:dev        # Dev server with hot reload
npm run docs:build      # Production build
npm run docs:preview    # Preview built site
```

ثم افتح URL المحلي الذي يُخرجه VitePress في متصفحك.

---

## المتطلبات المسبقة

المطلوب:

- الإلمام بسطر الأوامر وgit وبيئات التطوير المحلية
- القدرة على قراءة وكتابة الكود في مجموعة تطوير تطبيقات شائعة واحدة على الأقل
- خبرة أساسية في تصحيح البرمجيات (قراءة السجلات والاختبارات وسلوك وقت التشغيل)
- وقت كافٍ للالتزام بدورة عمل تركز على التنفيذ

مفيد ولكن ليس مطلوباً:

- خبرة مع Electron أو تطبيقات سطح المكتب أو الأدوات المحلية أولاً
- خلفية في الاختبار أو التسجيل أو هندسة البرمجيات
- تعرض سابق لـ Codex أو Claude Code أو وكلاء برمجة مشابهين

---

## المراجع الأساسية

المراجع الأولية:

- [OpenAI: Harness engineering: leveraging Codex in an agent-first world](https://openai.com/index/harness-engineering/)
- [Anthropic: Effective harnesses for long-running agents](https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents)
- [Anthropic: Harness design for long-running application development](https://www.anthropic.com/engineering/harness-design-long-running-apps)
- [OpenAI: Unrolling the Codex agent loop](https://openai.com/index/unrolling-the-codex-agent-loop/)
- [Anthropic: Demystifying evals for AI agents](https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents)
- [LangChain: Improving Deep Agents with harness engineering](https://www.langchain.com/blog/improving-deep-agents-with-harness-engineering)
- [Thoughtworks / Martin Fowler: Harness engineering for coding agent users](https://martinfowler.com/articles/harness-engineering.html)
- [Cursor: Continually improving our agent harness](https://cursor.com/blog/continually-improving-agent-harness)

راجع قائمة المراجع الطبقية الكاملة في [`docs/en/resources/reference/`](../../docs/en/resources/reference/index.md).

---

## هيكل المستودع

```text
learn-harness-engineering/
├── docs/                          # VitePress documentation site
│   ├── lectures/                  # 12 lectures (index.md + code/ examples)
│   │   ├── lecture-01-*/
│   │   ├── lecture-02-*/
│   │   └── ... (12 total)
│   ├── projects/                  # 6 project descriptions
│   │   ├── project-01-*/
│   │   └── ... (6 total)
│   └── resources/                 # Multilingual templates & references
│       ├── en/                    # English templates, checklists, guides
│       ├── zh/                    # Chinese templates, checklists, guides
│       ├── ru/                    # Russian templates, checklists, guides
│       └── vi/                    # Vietnamese templates, checklists, guides
├── projects/
│   ├── shared/                    # Shared Electron + TypeScript + React foundation
│   └── project-NN/               # Per-project starter/ and solution/ directories
├── skills/                        # Reusable AI agent skills
│   └── harness-creator/           # Harness engineering skill
├── package.json                   # VitePress + dev tooling
└── CLAUDE.md                      # Claude Code instructions for this repo
```

---

## كيف تم تنظيم الدورة

- كل محاضرة تركز على سؤال واحد
- الدورة تتضمن 6 مشاريع
- كل مشروع يتطلب من الوكيل القيام بعمل حقيقي
- كل مشروع يقارن نتائج الحزام الضعيف بالقوي
- ما يهم هو الفرق المقاس، وليس عدد الوثائق المكتوبة

---

## المهارات

يحتوي هذا المستودع أيضاً على مهارات وكلاء ذكاء اصطناعي قابلة لإعادة الاستخدام والتي يمكنك تثبيتها مباشرة في IDE أو مساحة عمل وكيلك.

- [**harness-creator**](../../skills/harness-creator/): مهارة تساعدك في إنشاء حزام بمستوى الإنتاج لمشروعك الخاص في دقائق.

---

## دورات أخرى

فريقنا أنشأ دورات أخرى أيضاً! اطلع عليها:

[![Hands-on Modern RL](https://img.shields.io/badge/HANDS--ON_MODERN_RL-0052cc?style=for-the-badge)](https://github.com/walkinglabs/hands-on-modern-rl)

**Hands-on Modern RL**: منهج عملي مفتوح المصدر يسد الفجوة من مفاهيم التعلم المعزز الأساسية إلى محاذاة نماذج اللغة الكبيرة (LLM) وRLVR والأنظمة الوكيلية المتقدمة.

---

## تاريخ النجوم

[![Star History Chart](https://api.star-history.com/svg?repos=walkinglabs/learn-harness-engineering&type=date&legend=top-left)](https://www.star-history.com/#walkinglabs/learn-harness-engineering&type=date&legend=top-left)

---

## شكر وتقدير

هذه الدورة مستوحاة وتستمد أفكاراً من [learn-claude-code](https://github.com/shareAI-lab/learn-claude-code) — دليل تدريجي لبناء وكيل من الصفر، من حلقة واحدة إلى تنفيذ مستقل معزول.
