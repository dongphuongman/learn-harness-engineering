[English version →](../../../en/projects/project-03-multi-session-continuity/)

> Tegishli maʼruzalar: [5-maʼruza. Sessiyalar oʻrtasida kontekstni saqlab qoling](./../../lectures/lecture-05-why-long-running-tasks-lose-continuity/index.md) · [6-maʼruza. Har bir agent sessiyasidan oldin inisializatsiya qiling](./../../lectures/lecture-06-why-initialization-needs-its-own-phase/index.md)
> Andoza fayllari: [templates/](https://github.com/walkinglabs/learn-harness-engineering/blob/main/docs/en/resources/templates/)

# Loyiha 03. Agentning ishlashini sessiyalar boʻylab uzluksiz taʼminlang

## Nima qilasiz

Agentga skoup nazorati (scope control) va tekshirish eshiklarini (verification gates) qoʻshing. Hujjatlarni qismlarga boʻlish (chunking), metamaʼlumotlarni (metadata) ajratib olish, indekslash jarayonini koʻrsatish va iqtiboslarga asoslangan Q&A (savol-javob) oqimini amalga oshiring. Funksiyalar (features) holatini kuzatish uchun `feature_list.json` dan foydalaning — bir vaqtda bitta funksiya ustida ishlansin, tekshiruv dalilisiz (verification evidence) “pass” (oʻtdi) deb belgilash mumkin emas.

Siz buni ikki marta bajarasiz: birinchisida hech qanday cheklovlarsiz, ikkinchisida esa qatʼiy talablar asosida.

## Repodagi tayyor loyihadan foydalaning

Repo yoʻli: `projects/project-03/`

| Katalog | Nimalar bor | Nimani taqqoslash |
|------|------|------|
| `starter/` | Project 02 kodi, indexing va citation-based Q&A hali tugallanmagan. Boshlangʻich `feature_list.json` bor, lekin yakuniy handoff/restart artefaktlari yoʻq. | Agent bir nechta feature orasida chalgʻiydimi yoki restartdan keyin holatni yoʻqotadimi. |
| `solution/` | Chunking, metadata, index status va citation-based Q&A tugallangan; `init.sh`, `session-handoff.md`, `claude-progress.md`, `clean-state-checklist.md` bor. | Har bir feature pass bo‘lishidan oldin aniq tekshiruv daliliga egami. |

## Vositalar

- Claude Code yoki Codex
- Git
- Node.js + Electron

## Harness mexanizmi

Jarayon jurnali (Progress log) + sessiyani topshirish (session handoff) + koʻp sessiyali uzluksizlik (multi-session continuity)
