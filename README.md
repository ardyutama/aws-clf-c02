# AWS Certified Cloud Practitioner (CLF-C02) — 11-Day Sprint Study Kit

> **Target Exam Date:** Saturday, **December 5, 2026** (Morning slot, English, Pearson VUE **OnVUE** online proctored)  
> **Study Window:** Monday, **November 23, 2026** → Friday, **December 4, 2026** (**11 active study days**, **Sunday, November 29 strictly OFF**)  
> **Total Budget:** **~29 study hours** (~2.5h/weekday, ~4h Sat Nov 28, 30m warm-up on Exam Day)  
> **Resource Budget:** **$0 (100% Free)** — AWS Skill Builder Free Tier, Official AWS Documentation/Learning, Free Practice Exams, and Anki Spaced Repetition

---

## Repository Map

| File | Purpose | When to Use |
| --- | --- | --- |
| [study-plan.md](study-plan.md) | Day-by-day session schedule (Nov 23 – Dec 5) with checkboxes, exact free URLs, Anki quotas, Sunday rest, and Monday catch-up — synced to the **Nov 25, 2026** `SB-ESS` update | Open **every day** and check off completed blocks |
| [aws-skillbuilder-research-2026.md](aws-skillbuilder-research-2026.md) | Primary-source verification of all AWS Skill Builder & official CLF-C02 resources (verified Nov 26, 2026): full 13-module `SB-ESS` syllabus, 19-item `SB-PLAN` breakdown, and update timestamps | Reference whenever checking exact Skill Builder modules or course freshness |
| [reddit-insights-2026.md](reddit-insights-2026.md) | Synthesis of the **5 latest `r/AWSCertifications` CLF-C02 passed threads** (Oct–Nov 2026) + **2026 Exam Guide v1.3 Delta & Outdated-Bank Errata Filter** | Read on **Day 1** and keep open while grading GitHub mocks |
| [lookalike-cheatsheet.md](lookalike-cheatsheet.md) | High-yield comparison tables: confusable services, 2026 Support Plans, CAF 6 perspectives, Well-Architected 6 pillars, Shared Responsibility, S3/EC2 pricing | Use during **review blocks**, after mocks, and on **Days 10–11** |
| [mock-tracker.md](mock-tracker.md) | Timed mock score log, domain gap breakdown, pass-readiness gates, and the Mistake-to-Anki conversion workflow | Log **every** quiz/mock immediately after finishing |
| [onvue-checklist.md](onvue-checklist.md) | Verified 2026 Pearson VUE OnVUE system/room/ID protocol, Day 2 & Day 10 dry-runs, and two-pass 90-minute exam pacing strategy | Run audit on **Day 2**, dress rehearsal on **Day 10**, and final check on **Dec 5** |
| [anki/anki-setup-guide.md](anki/anki-setup-guide.md) | Exact 11-day cram-mode Anki setup (FSRS & SM-2), import steps, Sunday-off handling, Mistake Cards, and Days 10–11 Filtered Cram Deck | Configure **Day 1 (Session 1)** before starting new cards |
| `anki/01–05_*.tsv` | 5 ready-to-import tab-separated Anki decks (~150 verified 2026 CLF-C02 cards) | Import on **Day 1**; unlock one domain deck at a time per [study-plan.md](study-plan.md) |

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

1. **Anki First (20–30 min/day):** Clear all due reviews *before* watching videos or starting new cards. Never skip reviews on study days (only Sunday, Nov 29 is 100% off).
2. **Active Watching at 1.25x–1.5x:** Watch *AWS Cloud Practitioner Essentials* and the 4 *Domain Reviews* at 1.25x–1.5x speed. Pause only to note confusing services — do **not** transcribe slides.
3. **Every Mock Error → Anki Mistake Card:** For every missed question **and every lucky guess**, write a short Q&A card in your `CLF-C02::06_Mistakes` subdeck explaining *why the right answer beats the distractor*.
4. **Filter Outdated Free Questions:** Whenever a free GitHub practice question tests legacy Support Plan tiers (*Developer / Business / Enterprise On-Ramp*), *Simple Monthly Calculator*, *QuickSight*, or pre-2019 pen-test approval myths, check [reddit-insights-2026.md](reddit-insights-2026.md#2026-exam-guide-v13-delta--outdated-bank-errata-filter) before memorizing it.
5. **Sunday, Nov 29 = 100% Zero Study:** Close laptops, close Anki, rest your brain. Monday's schedule already includes a 35-minute Anki catch-up buffer.

---

## Quick-Start Checklist (Do This First on Day 1)

- [ ] Create/log in to a **free AWS Skill Builder account** and enroll in the [Exam Prep Plan: AWS Certified Cloud Practitioner (CLF-C02 - English)](https://skillbuilder.aws/learning-plan/8UUCEZGNX4/exam-prep-plan-aws-certified-cloud-practitioner-clfc02--english/1J2VTQSGU2) via the [CLF-C02 Exam Prep Hub](https://skillbuilder.aws/category/exam-prep/cloud-practitioner-foundational-CLF-C02) *(9 Free / 10 Subscription items — use only the free items listed in [study-plan.md](study-plan.md), including the **Nov 25, 2026** 13-module `AWS Cloud Practitioner Essentials` update)*.
- [ ] Bookmark the free [Cloud Essentials Knowledge Badge Assessment](https://skillbuilder.aws/learn/63URRERNTS/cloud-essentials-knowledge-badge-assessment/VYB4663QV9) (updated Apr 30, 2026; randomized every attempt — your primary free AWS-authored exam engine).
- [ ] Bookmark the [Tutorials Dojo Free CLF-C02 Sampler (30 Qs)](https://portal.tutorialsdojo.com/courses/free-aws-certified-cloud-practitioner-practice-exams-sampler/) and [kananinirav Free Practice Exams](https://kananinirav.com/practice-exam/exams.html).
- [ ] Install **Anki** (Desktop + optional AnkiDroid/AnkiMobile sync) and follow [anki/anki-setup-guide.md](anki/anki-setup-guide.md) to import the 5 starter `.tsv` decks.
- [ ] Read [reddit-insights-2026.md](reddit-insights-2026.md) (10 minutes) so you start with 2026 pitfalls front-of-mind.
- [ ] Open [study-plan.md](study-plan.md) and start **Day 1 (Mon, Nov 23)**.
