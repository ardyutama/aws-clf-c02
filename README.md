# AWS Certified Cloud Practitioner (CLF-C02) — 8-Day Recovery Sprint Study Kit

> **Target Exam Date:** Saturday, **December 5, 2026** (Morning slot, English, Pearson VUE **OnVUE** online proctored)  
> **Recovery Window:** Friday, **November 27, 2026** → Saturday, **December 5, 2026** (re-baselined from mid-Module 3, OnVUE Stage 1 done, **20/150** Anki cards done; **Sunday, Nov 29 = ~30m Anki reviews ONLY**)  
> **Remaining Budget:** **20.0 study hours** (2.5h/weekday Fri + Mon–Fri, 4.0h Sat Nov 28, 0.5h Sun Anki-only, 0.5h Exam Morning warm-up)  
> **Resource Budget:** **$0 (100% Free)** — AWS Skill Builder Free Tier, Official AWS Documentation/Learning, Free Practice Exams, and Anki Spaced Repetition

---

## Repository Map

| File | Purpose | When to Use |
| --- | --- | --- |
| [study-plan.md](study-plan.md) | Restructured **8-Day Recovery Plan (Nov 27 – Dec 5)** with checkboxes, exact free URLs, Anki quotas (`150/150` by Tue Dec 1), Sunday Anki-only rest, and Week 2 mock sprint — synced to the **Nov 25, 2026** `SB-ESS` update | Open **every day** and check off completed blocks |
| [aws-skillbuilder-research-2026.md](aws-skillbuilder-research-2026.md) | Primary-source verification of all AWS Skill Builder & official CLF-C02 resources (verified Nov 26, 2026): full 13-module `SB-ESS` syllabus, 19-item `SB-PLAN` breakdown, and update timestamps | Reference whenever checking exact Skill Builder modules or course freshness |
| [reddit-insights-2026.md](reddit-insights-2026.md) | Synthesis of the **5 latest `r/AWSCertifications` CLF-C02 passed threads** (Oct–Nov 2026) + **2026 Exam Guide v1.3 Delta & Outdated-Bank Errata Filter** | Keep open while grading GitHub mocks and on **Fri Dec 4** |
| [lookalike-cheatsheet.md](lookalike-cheatsheet.md) | High-yield comparison tables: confusable services, 2026 Support Plans, CAF 6 perspectives, Well-Architected 6 pillars, Shared Responsibility, S3/EC2 pricing | Use during **review blocks**, after mocks, and on **Thu–Fri Dec 3–4** |
| [mock-tracker.md](mock-tracker.md) | Timed mock score log, domain gap breakdown, pass-readiness gates, and the Mistake-to-Anki conversion workflow | Log **every** quiz/mock immediately after finishing |
| [onvue-checklist.md](onvue-checklist.md) | Verified 2026 Pearson VUE OnVUE system/room/ID protocol (Stage 1 done; Stage 2 rehearsal **Thu Dec 3**), and two-pass 90-minute exam pacing strategy | Run dress rehearsal on **Thu Dec 3** and final check on **Dec 4–5** |
| [anki/anki-setup-guide.md](anki/anki-setup-guide.md) | Tightened **8-day recovery** Anki setup (`35 new/day`, `Max interval = 3 days`), Sunday reviews-only rule, Mistake Cards, and Thu–Fri Filtered Cram Deck | Update preset **today (Fri Nov 27)** before starting new cards |
| `anki/01–05_*.tsv` | 5 ready-to-import tab-separated Anki decks (**150** verified 2026 CLF-C02 cards; **20 done, 130 left**) | Unlock 30–35/day Fri–Tue per [study-plan.md](study-plan.md) |

---

## Verified CLF-C02 Exam Specs (Exam Guide v1.3 — Oct 29, 2026)

| Attribute | Official Specification |
| --- | --- |
| **Exam Code & Version** | **CLF-C02** (active as of Nov 2026; Exam Guide v1.3 published Oct 29, 2026) |
| **Questions** | **65 total** — **50 scored** + **15 unscored** (unidentified pretest questions) |
| **Question Formats** | Multiple choice (1 of 4) & Multiple response (2+ of 5+) — **never leave blanks** (no guessing penalty) |
| **Time Limit** | **90 minutes** (~83 seconds/question; target 50–55 min first pass + 35–40 min review) |
| **Passing Score** | **700 / 1,000** (scaled, compensatory — overall pass only, no per-domain fail) |
| **Out of Scope** | Coding, architecture design, troubleshooting, implementation, load/performance testing |
| **Official Exam Guide** | [AWS CLF-C02 Exam Guide (HTML)](https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02.html) |

### Official Domain Weighting & Study Allocation

| Domain | Exam Weight | Approx. Scored Qs | Core Focus |
| --- | :---: | :---: | --- |
| **Domain 1:** Cloud Concepts | **24%** | ~12 | 6 Cloud benefits, Well-Architected 6 pillars, AWS CAF 6 perspectives, 7 Rs migration, Cloud Economics |
| **Domain 2:** Security & Compliance | **30%** | ~15 | Shared Responsibility nuances, IAM/Root/Identity Center, GuardDuty/Inspector/Macie/WAF/Shield/KMS/Artifact/CloudTrail/Config |
| **Domain 3:** Cloud Technology & Services | **34%** | ~17 | Global infra, EC2/Lambda/ECS/EKS/Fargate, VPC/SG/NACL/Route 53/CloudFront/Global Accelerator, S3/EBS/EFS/FSx, RDS/Aurora/DynamoDB, AI/ML & Analytics |
| **Domain 4:** Billing, Pricing & Support | **12%** | ~6 | EC2 purchasing models (On-Demand/RI/Savings Plans/Spot/Dedicated), Cost Explorer/Budgets/CUR/Pricing Calculator, Organizations, **2026 Support Plans** |

> **High-Yield Insight:** **Domains 2 + 3 = 64%** of your scored exam. **Domain 4 is only 12%**, yet its concepts (Support Plans, Pricing Tools, EC2 Purchasing Models) are the easiest guaranteed points if you avoid outdated 2024/2025 material.

---

## Core Daily Operating Loop (Non-Negotiable Rules)

1. **Anki First (25–35 min/day):** Clear all due reviews *before* watching videos or starting new cards. Never skip due reviews — even on Sunday, Nov 29, do a quick ~30m review-only pass (`0 new cards`).
2. **Active Watching at 1.5x (Skip Console Demos):** Watch *AWS Cloud Practitioner Essentials* (M3–M13) and your 2 surgical *Domain Reviews* at **1.5x** speed. Skip click-through AWS Console demos, always complete per-module Assessments, and do **not** transcribe slides.
3. **Every Mock Error → Anki Mistake Card:** For every missed question **and every lucky guess**, write a short Q&A card in your `CLF-C02::06_Mistakes` subdeck explaining *why the right answer beats the distractor*.
4. **Filter Outdated Free Questions:** Whenever a free GitHub practice question tests legacy Support Plan tiers (*Developer / Business / Enterprise On-Ramp*), *Simple Monthly Calculator*, *QuickSight*, or pre-2019 pen-test approval myths, check [reddit-insights-2026.md](reddit-insights-2026.md#2026-exam-guide-v13-delta--outdated-bank-errata-filter) before memorizing it.
5. **Sunday, Nov 29 = Active Rest (Anki Reviews ONLY):** Spend ~30m clearing due Anki reviews (`0 new cards`), then close everything for the rest of the day.

---

## Recovery Start Checklist (Do This First Today — Fri, Nov 27)

- [x] Free AWS Skill Builder account + [Exam Prep Plan (CLF-C02)](https://skillbuilder.aws/learning-plan/8UUCEZGNX4/exam-prep-plan-aws-certified-cloud-practitioner-clfc02--english/1J2VTQSGU2), `SB-20Q` Cold Baseline (30%), OnVUE Stage 1 Audit, `SB-ESS` M1–M2, and first **20/150** Anki cards complete.
- [ ] Update your Anki options preset to the **8-Day Recovery Sprint** (`New cards/day = 35`, `Maximum interval = 3 days`) per [anki/anki-setup-guide.md](anki/anki-setup-guide.md).
- [ ] Open [study-plan.md](study-plan.md) and start **Recovery Day 1 (Fri, Nov 27)** — finish **Module 3** + complete **Modules 4–6**.
