# Timed Mock Score Log & Mistake-to-Anki Tracker

> **Pass Readiness Target (Calibrated from Oct–Nov 2026 Reddit Reports):**  
> Real CLF-C02 passing score is **700/1,000 (~70% scaled)**. Across recent passed threads, candidates scoring **75–85% consistently on timed mocks** passed comfortably on their first attempt.

---

## Readiness Gates (Check on Thursday, Dec 3 & Friday, Dec 4)

| Status | Benchmark | Action |
| :---: | --- | --- |
| **GREEN (Ready to Pass)** | **≥ 80%** on `SB-KBA` (Run #2 or #3) **AND** **≥ 80%** average on last 3 `GH-MOCK` sets **AND** **≥ 90%** on `SB-20Q` retake | Proceed confidently on Sat, Dec 5; stop studying by 8 PM Fri. |
| **YELLOW (Borderline)** | **72–79%** on `SB-KBA` or recent mocks | Spend Friday morning exclusively on your weakest 2 domains + `CLF-C02::06_Mistakes` Anki Cram Deck. |
| **RED (Danger Zone)** | **< 70%** by Thursday, Dec 3 | Check AWS's 24-hour reschedule policy on [CertMetrics](https://cp.certmetrics.com/amazon/en/login) — reschedule before the 24-hour cutoff rather than burning the $100 fee. |

---

## Master Practice Exam Log

> **Tip:** Always record **both** your raw score and your **errata-adjusted score** for `GH-MOCK` sets if any question tested retired CLF-C01 traps (see [reddit-insights-2026.md](reddit-insights-2026.md#2026-exam-guide-v13-delta--outdated-bank-errata-filter)).

| Day | Date | Source & Set | Qs | Time Used | Raw Score (%) | Target | Weakest Domain(s) | Mistake Cards Added | Notes |
| --- | --- | --- | :-: | :-: | :-: | :-: | --- | :-: | --- |
| **Day 1** | Nov 23 | `SB-20Q` Official Practice Set (Cold Baseline) | 20 | /30m | __% | Diagnostic | | | Learn AWS question phrasing |
| **Day 5** | Nov 27 | `GH-MOCK` Practice Exam 1 | 50 | /40m | __% | ≥65% | | | First timed run |
| **Day 6** | Nov 28 | `SB-KBA` Knowledge Badge Assessment (**Run #1**) | Full | /90m | __% | ≥70% | | | Official randomized AWS engine |
| **Day 6** | Nov 28 | `TD-FREE` Sampler — Timed Mode | 15 | /20m | __% | ≥73% | | | Read ALL explanations |
| **Day 6** | Nov 28 | `TD-FREE` Sampler — Review Mode | 15 | Untimed | __% | ≥73% | | | Read ALL explanations |
| **Day 7** | Nov 30 | `GH-MOCK` Practice Exam 2 | 50 | /35m | __% | ≥72% | | | Two-pass method |
| **Day 7** | Nov 30 | `GH-MOCK` Practice Exam 17 *(with explanations)* | 50 | /35m | __% | ≥74% | | | Two-pass method |
| **Day 8** | Dec 1 | `SB-KBA` Knowledge Badge Assessment (**Run #2**) | Full | /90m | __% | **≥80%** | | | ≥80% earns free Credly badge! |
| **Day 8** | Dec 1 | `GH-MOCK` Practice Exam 18 *(with explanations)* | 50 | /35m | __% | ≥76% | | | Apply 2026 Errata Filter |
| **Day 9** | Dec 2 | `GH-MOCK` Practice Exam 19 *(with explanations)* | 50 | /35m | __% | ≥78% | | | Watch Select TWO/THREE |
| **Day 9** | Dec 2 | `GH-MOCK` Practice Exam 20 *(with explanations)* | 50 | /35m | __% | ≥80% | | | Filter scenario fluff |
| **Day 10** | Dec 3 | `SB-KBA` Knowledge Badge Assessment (**Run #3 — OnVUE Rehearsal**) | Full | /90m | __% | **≥85%** | | | Strict paperless OnVUE conditions |
| **Day 11** | Dec 4 | `GH-MOCK` Practice Exam 21 or 22 *(with explanations)* | 50 | /35m | __% | **≥80%** | | | Final full stamina check |
| **Day 11** | Dec 4 | `SB-20Q` Official Practice Set (Final Retake) | 20 | /20m | __% | **≥90%** | | | Final confidence check |

---

## Domain Error Counter (Find Your Highest-ROI Gaps)

After every mock, add tally marks (`|`) under the domain where you missed or **guessed** a question. Prioritize the domain with the highest `(Missed × Weight)` score on Day 8 and Day 10.

| Domain | Exam Weight | Running Miss + Lucky-Guess Tallies | Recurring Weak Topics |
| --- | :---: | --- | --- |
| **Domain 1:** Cloud Concepts | **24%** | | *(e.g., CAF perspectives, Well-Architected pillars, 7 Rs)* |
| **Domain 2:** Security & Compliance | **30%** | | *(e.g., Shared Responsibility, GuardDuty vs Inspector vs Macie, IAM)* |
| **Domain 3:** Cloud Technology & Services | **34%** | | *(e.g., VPC/NACL/SG, S3 classes, RDS vs DynamoDB, AI/ML)* |
| **Domain 4:** Billing, Pricing & Support | **12%** | | *(e.g., 2026 Support Plans, Savings Plans vs RI, Cost Explorer vs CUR)* |

---

## The Mistake-to-Anki Protocol (From the 1000/1000 Reddit Method)

Do **not** skip this after a mock — this 15–20 minute loop is what converts 68% scores into 85%+ scores:

1. **Flag Lucky Guesses During the Mock:** On paper (Days 5–9) or in your mind/notepad (Day 10), note every question number where you were <80% sure — **even if you got it right**.
2. **Diagnose the Root Cause** for every wrong answer and lucky guess:
   - `CONCEPT` — Didn't know what the service/framework does.
   - `LOOK-ALIKE` — Confused two similar services (e.g., CloudTrail vs. Config).
   - `MISREAD` — Missed a constraint (*"lowest cost"*, *"least operational overhead"*, *"Select TWO"*).
   - `OUTDATED` — Legacy free-bank question contradicting 2026 Exam Guide v1.3 *(skip making a card; note the 2026 truth instead)*.
3. **Create a Concise Card in `CLF-C02::06_Mistakes`** (max 1–2 sentences on the back):
   - **Front:** The exact scenario trigger + why you confused it (e.g., *"Which AWS service scans Amazon S3 buckets for PII/credit cards — Macie or GuardDuty?"*).
   - **Back:** **Amazon Macie** (uses ML to discover sensitive data/PII in S3). *GuardDuty* detects malicious account/network threats via CloudTrail/VPC Flow/DNS logs.
4. **Cap Daily New Mistake Cards at 5–10:** If you missed 15 questions, pick the **top 8–10** highest-impact concepts so your Anki queue stays fast and sharp.

### Quick Mistake Log (Optional Scratchpad Before Entering Into Anki)

| Date | Mock | Root Cause | Confused Pair / Gap | Added to `06_Mistakes`? |
| --- | --- | --- | --- | :---: |
| | | | | [ ] |
| | | | | [ ] |
| | | | | [ ] |
| | | | | [ ] |
| | | | | [ ] |
| | | | | [ ] |
| | | | | [ ] |
| | | | | [ ] |
| | | | | [ ] |
| | | | | [ ] |
