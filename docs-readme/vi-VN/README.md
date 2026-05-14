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

> **Khóa học dựa trên dự án về xây dựng môi trường, quản lý trạng thái, cơ chế kiểm chứng và điều khiển giúp các agent viết code AI hoạt động đáng tin cậy.**

Learn Harness Engineering là một khóa học dành riêng cho kỹ thuật liên quan đến các agent viết code AI. Chúng tôi đã nghiên cứu sâu và tổng hợp các lý thuyết và thực tiễn Harness Engineering tiên tiến nhất trong ngành. Các tài liệu tham khảo cốt lõi của chúng tôi bao gồm:

- [OpenAI: Harness engineering: leveraging Codex in an agent-first world](https://openai.com/index/harness-engineering/)
- [Anthropic: Effective harnesses for long-running agents](https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents)
- [Anthropic: Harness design for long-running application development](https://www.anthropic.com/engineering/harness-design-long-running-apps)
- [Awesome Harness Engineering](https://github.com/walkinglabs/awesome-harness-engineering)

> **Bắt đầu nhanh?** Skill [`skills/harness-creator/`](../../skills/) có thể giúp bạn tạo nhanh một harness cấp sản xuất (AGENTS.md, feature lists, init.sh, quy trình kiểm chứng) cho dự án của riêng bạn chỉ trong vài phút.

---

## Mục lục

- [Xem trước trực quan](#xem-trước-trực-quan)
- [Harness Engineering thực sự có nghĩa là gì](#harness-engineering-thực-sự-có-nghĩa-là-gì)
- [Bắt đầu nhanh: Cải thiện Agent của bạn ngay hôm nay](#bắt-đầu-nhanh-cải-thiện-agent-của-bạn-ngay-hôm-nay)
- [Dự án tổng kết: Một ứng dụng thực tế](#dự-án-tổng-kết-một-ứng-dụng-thực-tế)
- [Lộ trình học tập](#lộ-trình-học-tập)
- [Giáo trình](#giáo-trình)
- [Skills](#skills)
- [Các khóa học khác](#các-khóa-học-khác)

---

## Xem trước trực quan

### Trang chủ khóa học
> Tổng quan khóa học toàn diện và giới thiệu về các triết lý cốt lõi, cung cấp lộ trình rõ ràng để bắt đầu.

![Xem trước trang chủ khóa học](../../docs/public/screenshots/readme/zh-home.png)

### Bài giảng nhập môn
> Đi sâu vào các vấn đề thực tế và dự án thực hành (như Dự án 01) mang đến trải nghiệm học tập nhập môn.

![Xem trước bài giảng khóa học](../../docs/public/screenshots/readme/zh-lecture-01.png)

### Thư viện tài nguyên sẵn sàng sử dụng
> Các mẫu và cấu hình tham khảo được thiết kế để giải quyết các vấn đề phổ biến trong phát triển agent AI nhiều lượt, chẳng hạn như mất ngữ cảnh và hoàn thành tác vụ quá sớm.

![Xem trước thư viện tài nguyên](../../docs/public/screenshots/readme/zh-resources.png)

## Sách giáo trình PDF

Kho lưu trữ hiện đã bao gồm quy trình xây dựng PDF cho nội dung khóa học.

- Chạy `npm run pdf:build` để tạo PDF tiếng Anh và tiếng Trung tại máy cục bộ.
- Các tệp đầu ra được ghi vào `artifacts/pdfs/`.
- Chạy `npm run screenshots:readme` nếu bạn muốn làm mới hình ảnh xem trước README.
- GitHub Actions workflow [`release-course-pdfs.yml`](../../.github/workflows/release-course-pdfs.yml) có thể xây dựng PDF và xuất bản chúng lên GitHub Releases.

---

## Mô hình thì thông minh, Harness giúp nó đáng tin cậy

Có một sự thật khắc nghiệt mà hầu hết mọi người đều học theo cách khó khăn nhất: **mô hình mạnh nhất thế giới vẫn sẽ thất bại trên các tác vụ kỹ thuật thực tế nếu bạn không xây dựng một môi trường phù hợp xung quanh nó.**

Bạn có thể đã tự thấy điều này. Bạn giao một tác vụ cho Claude hoặc GPT trong kho mã của mình. Nó bắt đầu tốt — đọc tệp, viết code, trông có vẻ hiệu quả. Sau đó có điều gì đó sai. Nó bỏ qua một bước. Nó làm hỏng một bài kiểm tra. Nó nói "xong" nhưng thực tế không có gì hoạt động. Bạn dành nhiều thời gian hơn để dọn dẹp so với việc tự làm.

Đây không phải là vấn đề của mô hình. Đây là vấn đề của harness.

Bằng chứng là rõ ràng. Anthropic đã thực hiện một thí nghiệm đối chứng: cùng mô hình (Opus 4.5), cùng prompt ("xây dựng trình soạn thảo game retro 2D"). Không có harness, nó tiêu tốn 9 đô la trong 20 phút và tạo ra thứ gì đó không hoạt động. Với harness đầy đủ (planner + generator + evaluator), nó tiêu tốn 200 đô la trong 6 giờ và xây dựng một game mà bạn có thể thực sự chơi được. Mô hình không thay đổi. Harness đã thay đổi.

OpenAI cũng báo cáo điều tương tự với Codex: trong một kho mã được harness tốt, cùng mô hình chuyển từ "không đáng tin cậy" sang "đáng tin cậy." Không phải là cải thiện nhỏ — mà là sự chuyển đổi về chất.

**Khóa học này dạy bạn cách xây dựng môi trường đó.**

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

## Harness Engineering thực sự có nghĩa là gì

Harness engineering là về việc xây dựng một môi trường làm việc hoàn chỉnh xung quanh mô hình để nó tạo ra kết quả đáng tin cậy. Nó không phải là về việc viết prompt tốt hơn. Nó là về việc thiết kế hệ thống mà mô hình hoạt động bên trong.

Một harness có năm hệ thống con:

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

Mỗi hệ thống con có một nhiệm vụ duy nhất:

- **Instructions** — Cho agent biết phải làm gì, theo thứ tự nào, và phải đọc gì trước khi bắt đầu. Không phải một tệp khổng lồ duy nhất; mà là cấu trúc tiết lộ dần mà agent điều hướng theo nhu cầu.
- **State** — Theo dõi những gì đã làm, những gì đang tiến hành, và những gì tiếp theo. Được lưu trữ trên đĩa để phiên tiếp theo tiếp tục chính xác nơi phiên trước đã dừng.
- **Verification** — Chỉ một bộ bài kiểm tra đạt mới được tính là bằng chứng. Agent không thể tuyên bố hoàn thành mà không có bằng chứng có thể chạy được.
- **Scope** — Giới hạn agent ở một tính năng tại một thời điểm. Không vượt quá phạm vi. Không hoàn thành một nửa ba việc. Không viết lại danh sách tính năng để che giấu công việc chưa hoàn thành.
- **Session Lifecycle** — Khởi tạo ở đầu. Dọn dẹp ở cuối. Để lại đường dẫn khởi động lại sạch cho phiên tiếp theo.

---

## Tại sao khóa học này tồn tại

Câu hỏi không phải là "mô hình có thể viết code không?" Chúng có thể. Câu hỏi là: **chúng có thể hoàn thành đáng tin cậy các tác vụ kỹ thuật thực tế bên trong các kho mã thực tế, qua nhiều phiên, mà không cần giám sát liên tục từ con người không?**

Hiện tại, câu trả lời là: không thể nếu không có harness.

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

Những câu hỏi mà khóa học này thực sự quan tâm:

- Những thiết kế harness nào cải thiện tỷ lệ hoàn thành tác vụ?
- Những thiết kế nào giảm thiểu việc làm lại và hoàn thành không chính xác?
- Những cơ chế nào giữ cho các tác vụ chạy dài tiến triển ổn định?
- Những cấu trúc nào giữ cho hệ thống có thể bảo trì sau nhiều lần chạy agent?

---

## Giáo trình & Tài liệu khóa học

Để xem đầy đủ tài liệu khóa học, vui lòng truy cập **[Trang web Tài liệu](https://walkinglabs.github.io/learn-harness-engineering/)**.

Giáo trình được chia thành ba phần:

1. **Bài giảng**: 12 đơn vị khái niệm giải thích lý thuyết đằng sau harness engineering.
2. **Dự án**: 6 dự án thực hành nơi bạn xây dựng một không gian làm việc agentic từ đầu.
3. **Thư viện tài nguyên**: Các mẫu sẵn sàng sử dụng (`AGENTS.md`, `feature_list.json`, `init.sh`, v.v.) để sử dụng trong kho mã của riêng bạn ngay hôm nay.

---

## Bắt đầu nhanh: Cải thiện Agent của bạn ngay hôm nay

Bạn không cần phải đọc cả 12 bài giảng trước khi bắt đầu nhận được giá trị. Nếu bạn đang sử dụng một agent viết code trên một dự án thực tế, đây là cách cải thiện nó ngay bây giờ.

Ý tưởng rất đơn giản: thay vì chỉ viết prompt, hãy cho agent của bạn một bộ tệp có cấu trúc xác định phải làm gì, những gì đã làm, và cách kiểm chứng công việc. Các tệp này nằm trong kho mã của bạn, vì vậy mỗi phiên bắt đầu từ cùng một trạng thái.

```text
    YOUR PROJECT ROOT
    ├── AGENTS.md              <-- the agent's operating manual
    ├── CLAUDE.md              <-- (alternative, if using Claude Code)
    ├── init.sh                <-- runs install + verify + start
    ├── feature_list.json      <-- what features exist, which are done
    ├── claude-progress.md     <-- what happened each session
    └── src/                   <-- your actual code
```

Lấy các mẫu khởi đầu từ [Thư viện tài nguyên](https://walkinglabs.github.io/learn-harness-engineering/en/resources/) và đưa chúng vào dự án của bạn. Đó là tất cả. Bốn tệp, và các phiên agent của bạn sẽ đã ổn định hơn đáng kể so với việc chỉ chạy trên prompt.

---

## Dự án tổng kết: Một ứng dụng thực tế

Tất cả sáu dự án khóa học đều xoay quanh cùng một sản phẩm: **một ứng dụng desktop cơ sở tri thức cá nhân dựa trên Electron**.

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

Dự án này được chọn vì nó kết hợp giá trị thực tế cao, đủ độ phức tạp sản phẩm thực tế, và môi trường tốt để quan sát sự cải thiện harness trước/sau.

Mỗi starter/solution của dự án khóa học là một bản sao hoàn chỉnh của ứng dụng Electron ở giai đoạn tiến hóa đó. Starter của P(N+1) được tạo từ solution của P(N) — ứng dụng tiến hóa khi kỹ năng harness của bạn phát triển.

---

## Lộ trình học tập

Khóa học được thiết kế để hoàn thành theo thứ tự. Mỗi giai đoạn xây dựng dựa trên giai đoạn trước.

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

Mỗi giai đoạn mất khoảng một tuần nếu bạn học bán thời gian. Nếu bạn muốn đi nhanh hơn, các giai đoạn 1-3 có thể hoàn thành trong một cuối tuần dài.

---

## Giáo trình

### Bài giảng — 12 đơn vị khái niệm, mỗi đơn vị trả lời một câu hỏi cốt lõi

*Đọc toàn bộ văn bản cho mỗi bài giảng trên [Trang web Tài liệu](https://walkinglabs.github.io/learn-harness-engineering/).*

| Phiên | Câu hỏi | Ý tưởng cốt lõi |
|-------|---------|------------------|
| [L01](../../docs/lectures/lecture-01-why-capable-agents-still-fail/index.md) | Tại sao các mô hình mạnh vẫn thất bại trên tác vụ thực tế? | Khoảng cách năng lực giữa benchmark và kỹ thuật thực tế |
| [L02](../../docs/lectures/lecture-02-what-a-harness-actually-is/index.md) | "Harness" thực sự có nghĩa là gì? | Năm hệ thống con: instructions, state, verification, scope, lifecycle |
| [L03](../../docs/lectures/lecture-03-why-the-repository-must-become-the-system-of-record/index.md) | Tại sao kho mã phải là nguồn chân lý duy nhất? | Nếu agent không thể thấy nó, nó không tồn tại |
| [L04](../../docs/lectures/lecture-04-why-one-giant-instruction-file-fails/index.md) | Tại sao một tệp hướng dẫn khổng lồ lại thất bại? | Tiết lộ dần: cho một bản đồ, không phải một bộ bách khoa toàn thư |
| [L05](../../docs/lectures/lecture-05-why-long-running-tasks-lose-continuity/index.md) | Tại sao các tác vụ chạy dài mất tính liên tục? | Lưu trữ tiến trình vào đĩa; tiếp tục từ nơi bạn đã dừng |
| [L06](../../docs/lectures/lecture-06-why-initialization-needs-its-own-phase/index.md) | Tại sao khởi tạo cần một giai đoạn riêng? | Xác minh môi trường khỏe mạnh trước khi agent bắt đầu làm việc |
| [L07](../../docs/lectures/lecture-07-why-agents-overreach-and-under-finish/index.md) | Tại sao agent lại vượt quá phạm vi và không hoàn thành? | Một tính năng tại một thời điểm; định nghĩa rõ ràng về "hoàn thành" |
| [L08](../../docs/lectures/lecture-08-why-feature-lists-are-harness-primitives/index.md) | Tại sao danh sách tính năng là nguyên thủy của harness? | Ranh giới phạm vi có thể đọc bởi máy mà agent không thể bỏ qua |
| [L09](../../docs/lectures/lecture-09-why-agents-declare-victory-too-early/index.md) | Tại sao agent tuyên bố hoàn thành quá sớm? | Khoảng trống kiểm chứng: sự tự tin ≠ sự chính xác |
| [L10](../../docs/lectures/lecture-10-why-end-to-end-testing-changes-results/index.md) | Tại sao kiểm thử đầu-cuối lại thay đổi kết quả? | Chỉ một lần chạy toàn bộ pipeline mới được tính là kiểm chứng thực sự |
| [L11](../../docs/lectures/lecture-11-why-observability-belongs-inside-the-harness/index.md) | Tại sao khả năng quan sát thuộc về bên trong harness? | Nếu bạn không thể thấy agent đã làm gì, bạn không thể sửa những gì nó đã làm hỏng |
| [L12](../../docs/lectures/lecture-12-why-every-session-must-leave-a-clean-state/index.md) | Tại sao mỗi phiên phải để lại trạng thái sạch? | Sự thành công của phiên tiếp theo phụ thuộc vào việc dọn dẹp của phiên này |

### Dự án — 6 dự án thực hành áp dụng phương pháp bài giảng vào cùng ứng dụng Electron

| Dự án | Những gì bạn làm | Cơ chế Harness |
|-------|-------------------|----------------|
| [P01](../../docs/projects/project-01-baseline-vs-minimal-harness/index.md) | Chạy cùng tác vụ hai lần: chỉ dùng prompt vs. ưu tiên quy tắc | Harness tối thiểu: AGENTS.md + init.sh + feature_list.json |
| [P02](../../docs/projects/project-02-agent-readable-workspace/index.md) | Tái cấu trúc kho mã để agent có thể đọc được | Không gian làm việc agent có thể đọc + các tệp trạng thái liên tục |
| [P03](../../docs/projects/project-03-multi-session-continuity/index.md) | Khiến agent tiếp tục từ nơi nó đã dừng | Nhật ký tiến trình + bàn giao phiên + tính liên tục đa phiên |
| [P04](../../docs/projects/project-04-incremental-indexing/index.md) | Ngăn agent làm quá nhiều hoặc quá ít | Phản hồi thời gian chạy + kiểm soát phạm vi + lập chỉ mục gia tăng |
| [P05](../../docs/projects/project-05-grounded-qa-verification/index.md) | Khiến agent tự kiểm chứng công việc của mình | Tự kiểm chứng + Q&A có căn cứ + hoàn thành dựa trên bằng chứng |
| [P06](../../docs/projects/project-06-runtime-observability-and-debugging/index.md) | Xây dựng một harness hoàn chỉnh từ đầu (tổng kết) | Harness đầy đủ: tất cả cơ chế + khả năng quan sát + nghiên cứu ablation |

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

### Thư viện tài nguyên

- [Thư viện tài nguyên tiếng Anh](https://walkinglabs.github.io/learn-harness-engineering/en/resources/) — mẫu, danh sách kiểm tra và tài liệu tham khảo phương pháp
- [Thư viện tài nguyên tiếng Trung](https://walkinglabs.github.io/learn-harness-engineering/zh/resources/) — 中文模板、清单和方法参考
- [Thư viện tài nguyên tiếng Nga](https://walkinglabs.github.io/learn-harness-engineering/ru/resources/) — шаблоны, чек-листы и справочники
- [Thư viện tài nguyên tiếng Việt](https://walkinglabs.github.io/learn-harness-engineering/vi/resources/) — mẫu, danh sách kiểm tra và tài liệu tham khảo

---

## Vòng đời phiên Agent

Một trong những ý tưởng cốt lõi trong khóa học này: **phiên của agent nên tuân theo một vòng đời có cấu trúc, không phải tự do không kiểm soát.** Đây là cách nó trông như thế này:

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

## Khóa học này dành cho ai

Khóa học này dành cho:

- Các kỹ sư đang sử dụng agent viết code và muốn sự ổn định và chất lượng tốt hơn
- Các nhà nghiên cứu hoặc nhà xây dựng muốn hiểu biết hệ thống về thiết kế harness
- Các trưởng nhóm kỹ thuật cần hiểu cách thiết kế môi trường ảnh hưởng đến hiệu suất agent

Khóa học này không dành cho:

- Những người tìm kiếm một giới thiệu AI không cần viết code
- Những người chỉ quan tâm đến prompt và không có kế hoạch xây dựng các triển khai thực tế
- Những người học không sẵn sàng để các agent làm việc bên trong các kho mã thực tế

---

## Yêu cầu

Đây là một khóa học mà bạn thực sự chạy các agent viết code.

Bạn cần ít nhất một trong các công cụ sau:

- Claude Code
- Codex
- Một agent viết code IDE hoặc CLI khác hỗ trợ chỉnh sửa tệp, thực thi lệnh và tác vụ nhiều bước

Khóa học giả định rằng bạn có thể:

- Mở một kho mã cục bộ
- Cho phép agent chỉnh sửa tệp
- Cho phép agent chạy lệnh
- Kiểm tra đầu ra và chạy lại tác vụ

Nếu bạn không có công cụ như vậy, bạn vẫn có thể đọc nội dung khóa học, nhưng bạn sẽ không thể hoàn thành các dự án như dự kiến.

---

## Xem trước cục bộ

Kho lưu trữ này sử dụng VitePress làm trình xem tài liệu.

```sh
npm install
npm run docs:dev        # Dev server với tải lại nóng
npm run docs:build      # Build sản xuất
npm run docs:preview    # Xem trước trang đã build
```

Sau đó mở URL cục bộ mà VitePress hiển thị trong trình duyệt của bạn.

---

## Điều kiện tiên quyết

Bắt buộc:

- Quen thuộc với terminal, git và môi trường phát triển cục bộ
- Khả năng đọc và viết code trong ít nhất một ngăn xếp ứng dụng phổ biến
- Kinh nghiệm gỡ lỗi phần mềm cơ bản (đọc log, kiểm thử và hành vi thời gian chạy)
- Đủ thời gian để cam kết với khóa học tập trung vào triển khai

Có ích nhưng không bắt buộc:

- Kinh nghiệm với Electron, ứng dụng desktop hoặc công cụ local-first
- Nền tảng về kiểm thử, logging hoặc kiến trúc phần mềm
- Đã tiếp xúc với Codex, Claude Code hoặc các agent viết code tương tự

---

## Tài liệu tham khảo cốt lõi

Chính:

- [OpenAI: Harness engineering: leveraging Codex in an agent-first world](https://openai.com/index/harness-engineering/)
- [Anthropic: Effective harnesses for long-running agents](https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents)
- [Anthropic: Harness design for long-running application development](https://www.anthropic.com/engineering/harness-design-long-running-apps)
- [OpenAI: Unrolling the Codex agent loop](https://openai.com/index/unrolling-the-codex-agent-loop/)
- [Anthropic: Demystifying evals for AI agents](https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents)
- [LangChain: Improving Deep Agents with harness engineering](https://www.langchain.com/blog/improving-deep-agents-with-harness-engineering)
- [Thoughtworks / Martin Fowler: Harness engineering for coding agent users](https://martinfowler.com/articles/harness-engineering.html)
- [Cursor: Continually improving our agent harness](https://cursor.com/blog/continually-improving-agent-harness)

Xem danh sách tài liệu tham khảo phân tầng đầy đủ tại [`docs/en/resources/reference/`](../../docs/en/resources/reference/index.md).

---

## Cấu trúc kho lưu trữ

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

## Khóa học được tổ chức như thế nào

- Mỗi bài giảng tập trung vào một câu hỏi
- Khóa học bao gồm 6 dự án
- Mọi dự án đều yêu cầu agent thực hiện công việc thực tế
- Mọi dự án đều so sánh kết quả harness yếu vs. mạnh
- Điều quan trọng là sự khác biệt được đo lường, không phải số lượng tài liệu đã viết

---

## Skills

Kho lưu trữ này cũng bao gồm các skill agent AI có thể tái sử dụng mà bạn có thể cài đặt trực tiếp vào IDE hoặc không gian làm việc agent của mình.

- [**harness-creator**](../../skills/harness-creator/): Một skill giúp bạn tạo nhanh một harness cấp sản xuất cho dự án của riêng bạn chỉ trong vài phút.

---

## Các khóa học khác

Đội ngũ của chúng tôi cũng đã tạo các khóa học khác! Hãy xem:

[![Hands-on Modern RL](https://img.shields.io/badge/HANDS--ON_MODERN_RL-0052cc?style=for-the-badge)](https://github.com/walkinglabs/hands-on-modern-rl)

**Hands-on Modern RL**: Một giáo trình thực hành mã nguồn mở kết nối khoảng cách từ các khái niệm RL cơ bản đến LLM alignment, RLVR và các hệ thống Agentic nâng cao.

---

## Lịch sử Star

[![Star History Chart](https://api.star-history.com/svg?repos=walkinglabs/learn-harness-engineering&type=date&legend=top-left)](https://www.star-history.com/#walkinglabs/learn-harness-engineering&type=date&legend=top-left)

---

## Lời cảm ơn

Khóa học này được truyền cảm hứng và rút ra ý tưởng từ [learn-claude-code](https://github.com/shareAI-lab/learn-claude-code) — một hướng dẫn tiệm tiến về việc xây dựng một agent từ đầu, từ một vòng lặp đơn giản đến thực thi tự chủ cô lập.
