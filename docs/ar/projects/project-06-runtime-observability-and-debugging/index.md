[中文版本 →](../../../zh/projects/project-06-runtime-observability-and-debugging/)

> محاضرات مرتبطة: [المحاضرة 11. اجعل runtime الخاص بالوكيل قابلًا للملاحظة](./../../lectures/lecture-11-why-observability-belongs-inside-the-harness/index.md) · [المحاضرة 12. Handoff نظيف في نهاية كل جلسة](./../../lectures/lecture-12-why-every-session-must-leave-a-clean-state/index.md)
> ملفات القوالب: [templates/](https://github.com/walkinglabs/learn-harness-engineering/blob/main/docs/ar/resources/templates/)

# المشروع 06. ابنِ harness كاملًا للوكيل (Capstone)

## ما الذي ستفعله

هذا هو مشروع التخرج. اجمع كل ما تعلمته في المشاريع الخمسة الأولى، وشغّل benchmark كاملًا، ثم نفذ جولة تنظيف للتحقق من أن الجودة قابلة للصيانة.

استخدم مجموعة مهام ثابتة متعددة الميزات تغطي شريحة منتج كاملة: استيراد المستندات، الفهرسة، Q&A مع الاستشهادات، قابلية ملاحظة runtime، وحالة مستودع قابلة للقراءة والاستئناف. ابدأ بتشغيل baseline مع harness ضعيف، ثم شغّل أقوى harness لديك، ثم نظف وأعد التشغيل. أخيرًا، نفذ تجربة ablation للـ harness: أزل مكونًا واحدًا كل مرة وانظر أيها مهم فعليًا.

## استخدم المشروع الموجود في المستودع

مسار المستودع: `projects/project-06/`

| المجلد | ماذا يحتوي | ماذا تقارن |
|------|------|------|
| `starter/` | المنتج شبه مكتمل، لكن سطح harness ضعيف عمدًا: يوجد `AGENTS.md` أساسي فقط، ولا يوجد `feature_list.json` أو `session-handoff.md` أو clean-state checklist أو benchmark/cleanup scripts. | ملاحظات يدوية لخط baseline مع harness ضعيف. |
| `solution/` | harness كامل: `AGENTS.md`, `CLAUDE.md`, `feature_list.json`, `init.sh`, `session-handoff.md`, `clean-state-checklist.md`, quality/evaluator docs و scripts. | شغّل `projects/project-06/solution/scripts/benchmark.sh` و `projects/project-06/solution/scripts/cleanup-scanner.sh` ثم قارن أدلة الجودة. |

## الأدوات

- Claude Code أو Codex
- Git
- Node.js + Electron
- قالب وثيقة جودة
- rubric للمقيّم
- كل مكونات harness المتراكمة من المشاريع الخمسة الأولى

## آلية harness

Harness كامل: كل الآليات + قابلية الملاحظة + دراسة ablation
