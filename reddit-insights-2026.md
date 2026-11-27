# Reddit Insights (`r/AWSCertifications`, Oct–Nov 2026) & 2026 Errata Filter

> **Selection Criteria:** The **5 latest substantive, live CLF-C02 passed threads** on `r/AWSCertifications` as of **November 23, 2026** (filtered to exclude empty one-liners, voucher threads, and removed posts), synthesized into concrete study & exam rules — plus the **2026 Exam Guide v1.3 Errata Filter** for free practice banks.

---

## The 5 Latest Substantive `r/AWSCertifications` CLF-C02 Threads

### Thread 1 — `'Passed' CLF-C02, Too Good to be True?`
- **Date:** November 13, 2026 · **Author:** `u/accidentalacrophobia`
- **Link:** https://www.reddit.com/r/AWSCertifications/comments/1xvn0pk/passed_clfc02_too_good_to_be_true/
- **Practice vs. Real Exam:** Scored **70s to low 80s** on full timed practice tests → **PASS** on the real exam (~60+ min total time).
- **Key Tips:**
  - **Two-Pass Strategy:** Answer questions you know with 100% confidence first, flag uncertain ones, then return and systematically cross out wrong distractors.
  - Recognizing service names in real exam context was easier than expected once distractors were eliminated.
- **OnVUE Pitfall Flagged:** Taking OnVUE on an **ultrawide monitor** or fidgeting/glancing away from center triggers high post-exam stress about proctor flags. Weekend/Friday exams frequently delay the official score report email until Monday even after seeing `PASS` on screen.

---

### Thread 2 — `Passed CLF-C02 in under 2 weeks: resources I used and what actually mattered`
- **Date:** October 30, 2026 · **Author:** `u/kanishkable`
- **Link:** https://www.reddit.com/r/AWSCertifications/comments/1xja6cg/passed_clfc02_in_under_2_weeks_resources_i_used/
- **Practice vs. Real Exam:** Completed **8 full practice exams averaging 75–80%** (specifically using the free `kananinirav/AWS-Certified-Cloud-Practitioner-Notes` GitHub exams) → **PASS** in under 2 weeks.
- **High-Yield Exam Topics Observed:**
  - **AWS CAF 6 Perspectives** (*Business, People, Governance, Platform, Security, Operations* — mnemonic: **"Big Projects Go Pretty Smoothly Overall"**) + **Well-Architected 6 Pillars & design principles** = easily **5–10 exam questions**.
  - **2026 Support Plans** appeared repeatedly: **Basic, Business Support+, Enterprise Support, Unified Operations**.
  - **Shared Responsibility nuance:** *Processes* (patch management, config management, awareness/training) are **shared**, while specific concrete tasks have **one owner** (e.g., configuring a Security Group = customer; physical data center security = AWS).
  - **Frequent look-alikes:** GuardDuty vs. Inspector vs. Macie; Cost Explorer vs. Budgets vs. Cost & Usage Report; Service Health vs. Personal Health Dashboard; Lightsail vs. Elastic Beanstalk.
- **Critical Pitfalls Flagged:**
  - **Outdated free question banks** still test discontinued Support Plan names (*Developer / Business / Enterprise On-Ramp*), pre-2019 pen-test approval myths, and obsolete Spot Instance "bidding."
  - **"Select TWO / THREE" losses:** Easy marks lost simply by misreading how many options to pick.

---

### Thread 3 — `Passed AWS Cloud Practitioner (CLF-C02)`
- **Date:** October 11, 2026 · **Author:** `u/Lucky-Champion4855`
- **Link:** https://www.reddit.com/r/AWSCertifications/comments/1x35m01/passed_aws_cloud_practitioner_clfc02/
- **Practice vs. Real Exam:** Aimed for **≥70%+** on 6 full mocks, reviewing weak topics after **every single exam** → **PASS**.
- **High-Yield Revision List:** AWS pricing models, S3 storage classes, IAM, Shared Responsibility Model, Well-Architected Framework, and differentiating similar AWS services.
- **Pitfall Flagged:** Spamming practice tests without analyzing *why* every right option works and every distractor fails. Memorizing practice questions breaks down on real AWS phrasing.

---

### Thread 4 — `Passed CLF-C02 with 1000/1000. Mechanical engineer with no IT job, 4 weeks of study`
- **Date:** October 10, 2026 · **Author:** `u/yixian0716`
- **Link:** https://www.reddit.com/r/AWSCertifications/comments/1x29dpw/passed_clfc02_with_10001000_mechanical_engineer/
- **Score & Background:** **1000/1000** (perfect score) with no IT job after 4 weeks of disciplined study outside full-time work (sat Oct 6, 2026).
- **Concrete Habits That Drove 1000/1000:**
  - Reviewed explanations for **every wrong answer AND every lucky guess** (a guess you got right is still a knowledge gap).
  - Explicitly drilled look-alike comparisons (monitoring vs. auditing, support tiers, pricing models).
  - Used the full 90 minutes wisely — didn't rush through flagged questions on exam day.
- **2025/2026 Console Note (from comments):** AWS accounts opened after July 2025 choose a "Free plan" vs. "Paid plan" at signup, and the new Free plan restricts some services — validating our exam-focused path that doesn't rely on paid personal-account labs.

---

### Thread 5 — `Finally passed CLF-C02 after putting it off for a year`
- **Date:** October 3, 2026 · **Author:** `u/ColdHeartedPencil`
- **Link:** https://www.reddit.com/r/AWSCertifications/comments/1wwh2b3/finally_passed_clfc02_after_putting_it_off_for_a/
- **Score:** **844/1000** after weekend study over ~1 month.
- **Concrete Exam Strategy & Warning:**
  - **Pacing Winner:** Finished Pass 1 in **~50 minutes**, leaving **40 minutes** to review answers carefully, which caught silly mistakes and boosted the score to 844.
  - **Pitfall of AI-only quizzes:** Real AWS exam stems inject **distracting scenario details ("fluff")** that short AI-generated quizzes omit. You must practice extracting the **1–2 operational constraints** (e.g., *"least operational overhead"*, *"audit API calls"*, *"lowest cost for unpredictable access"*) from wordy questions.

---

## Synthesized Action Rules (Baked Into This Study Plan)

| # | Consensus Finding Across the 5 Threads | How Our Study Plan Implements It |
| :-: | --- | --- |
| **1** | **75–85% on timed mocks = comfortable real-exam pass** | Pass gates in [mock-tracker.md](mock-tracker.md): ≥80% on Skill Builder Knowledge Badge + ≥80% on timed GitHub sets |
| **2** | **Review lucky guesses, not just wrong answers** | Every guessed or missed question becomes an Anki card in `CLF-C02::06_Mistakes` |
| **3** | **CAF + Well-Architected = 5–10 guaranteed questions** | Dedicated cards in `01_Domain1_CloudConcepts.tsv` + cheatsheet mnemonics |
| **4** | **Look-alikes decide close questions** | Dedicated `05_LookAlikes_2026Delta.tsv` deck + side-by-side tables in [lookalike-cheatsheet.md](lookalike-cheatsheet.md) |
| **5** | **Free banks have 2024–2025 outdated traps** | Apply the **2026 Errata Filter** below whenever taking `kananinirav` GitHub exams |
| **6** | **Two-pass 50m + 40m pacing beats rushing** | Practiced on every Week 2 mock and locked into [onvue-checklist.md](onvue-checklist.md) |
| **7** | **OnVUE discipline prevents anxiety & revocations** | Early System Test + desk audit (done!) + Thu Dec 3 paperless dress rehearsal in [onvue-checklist.md](onvue-checklist.md) |

---

## 2026 Exam Guide v1.3 Delta & Outdated-Bank Errata Filter

> **Verified Against:** Official AWS CLF-C02 Exam Guide **v1.3 (October 29, 2026)** and Official [AWS Support Plans Documentation](https://docs.aws.amazon.com/awssupport/latest/user/aws-support-plans.html).  
> **Use this table whenever grading `kananinirav` GitHub Practice Exams or older free quizzes!**

| Outdated Term / Trap in Free Banks | Verified 2026 CLF-C02 Truth (What the Real Exam Tests) | Action While Grading Free Mocks |
| --- | --- | --- |
| **Legacy Support Plans:** *Developer*, *Business*, *Enterprise On-Ramp* *(discontinued Jan 1, 2027)* | Current 4 plans: **Basic**, **AWS Business Support+** ($29/mo min, GenAI contextual support, 24x7 phone/web/chat, <30m business-critical system down, 500+ Trusted Advisor checks, Support API), **AWS Enterprise Support** ($5,000/mo min, designated TAM, ≤15m prod-critical, AWS Security Incident Response included, AWS Countdown), **AWS Unified Operations** (designated TAM + Domain Specialist Engineer, IEM, architecture guidance, Countdown Premium, personalized runbooks). | Know **both** old and new mappings so you score free mocks cleanly, but memorize the **2026 names & SLAs** for Dec 5. |
| **AWS Simple Monthly Calculator** or **TCO Calculator** | Retired! Replaced by **AWS Pricing Calculator** (and **AWS Migration Evaluator** for on-prem TCO business cases). | If a GitHub question says *Simple Monthly Calculator*, mentally map it to **AWS Pricing Calculator**. |
| **Amazon QuickSight** | Updated in CLF-C02 v1.3 in-scope list to **Amazon Quick** (BI dashboards & analytics). | Recognize **Amazon Quick** = BI / visualization dashboards (formerly QuickSight). |
| **Amazon SageMaker** | Updated in CLF-C02 v1.3 to **Amazon SageMaker AI** (build, train, deploy ML models). | Same core concept; expect **Amazon SageMaker AI** on the exam. |
| **Amazon WorkSpaces Web** | Updated in CLF-C02 v1.3 to **Amazon WorkSpaces Secure Browser** (managed browser access to internal web apps). | Distinguish from **WorkSpaces** (full virtual desktop) and **AppStream 2.0** (streaming specific desktop apps). |
| **Amazon Q** *(missing from older banks)* | Explicitly **in scope** under Machine Learning in CLF-C02 v1.3 (generative AI assistant for business & developers). | Included in `05_LookAlikes_2026Delta.tsv`. |
| **AWS Abuse Team** | Official Task 4.3 now refers to the **AWS Trust and Safety team** for reporting abuse/malicious use of AWS resources. | Treat *AWS Trust and Safety team* (and legacy *AWS Abuse team*) as the answer for abuse reporting. |
| **"Penetration testing requires prior AWS approval"** | **FALSE (outdated pre-2019 rule).** Customers **may** perform penetration testing on permitted AWS services (EC2, RDS, Aurora, CloudFront, API Gateway, Lambda, Lightsail, etc.) **without prior approval** under the AWS Customer Support Policy for Penetration Testing. Prohibited activities (DDoS simulation, DNS zone walking, port flooding) are never allowed. | Flag any old question claiming approval is required for EC2 pen-testing as **errata**. |
| **"Bid on EC2 Spot Instances"** | **FALSE (outdated pre-2017 pricing).** Spot Instances no longer use bidding; prices adjust gradually based on long-term supply & demand, with a **2-minute interruption notice** and up to **90% savings**. | Ignore "bidding" distractors; remember *stateless, fault-tolerant, interruptible, up to 90% off, 2-min notice*. |
| **AWS Personal Health Dashboard vs. Service Health Dashboard** | Consolidated into the **AWS Health Dashboard** (contains both *Your account health* [personalized events] and *Service health* [public global AWS status]). | Know both the unified **AWS Health Dashboard** name and the account-specific vs. global distinction. |
| **Retired services removed from Out-of-Scope list in v1.3** | *Elastic Transcoder, Elemental MediaStore, Lookout for Metrics, Lumberyard, Monitron, Panorama, RoboMaker, WorkDocs* were retired and removed — also note *OpsWorks, CodeCommit, CodeStar, Cloud9, Snowball/Snowmobile, QLDB* are **NOT** in the current CLF-C02 v1.3 in-scope list. | Don't waste Anki space memorizing retired services that pop up in 2021–2023 GitHub questions. |
