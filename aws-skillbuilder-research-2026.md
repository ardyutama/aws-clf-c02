# Primary-Source Research: AWS Skill Builder & CLF-C02 Resources (Verified November 26, 2026)

> **Research Scope:** Strict primary-source verification of all AWS Skill Builder courses, the official CLF-C02 Exam Prep Plan, AWS Certification Exam Guide docs, AWS Support Plans docs, Tutorials Dojo Free Sampler, and `kananinirav` practice exams referenced in [study-plan.md](study-plan.md).  
> **Verification Date:** November 26, 2026 (live inspection via HTTP fetch and interactive headless browser rendering of JavaScript-rendered Skill Builder pages).

---

## Executive Summary of Key Findings

1. **`AWS Cloud Practitioner Essentials` (`SB-ESS`) WAS JUST UPDATED on November 25, 2026:**
   - Same canonical URL (`https://skillbuilder.aws/learn/94T2BEN85A/aws-cloud-practitioner-essentials/8D79F3AVR7`), carrying an **`UPDATED`** badge.
   - **Duration increased** from `12h 45m` to **`13 hours`** (`13h 0m`). *(Note: AWS's own marketing page at `https://aws.amazon.com/training/learn-about/cloud-practitioner/` still displays the stale `12 hours 45 minutes` figure, which is why [study-plan.md](study-plan.md) had `12h 45m`.)*
   - **Curriculum was substantially restructured into 13 Modules + `Next Steps: Get Started on AWS`** (replacing the older ~11-module flow that [study-plan.md](study-plan.md) splits into 4 blocks):
     - **Compute** is now split across **Module 2 (Compute in the Cloud)** and a new dedicated **Module 3 (Exploring Compute Services: Serverless/Lambda, Containers & Orchestration, Additional Compute Services)**.
     - **Module 8 (`AI ML and Data Analytics`)** is a **brand-new dedicated module** covering AI/ML on AWS, **Generative AI on AWS & AWS Generative AI Solutions**, and **Data Analytics & Data Pipelines on AWS**.
     - **Module 6 (`Storage`)** now explicitly adds **Amazon FSx**, **AWS Storage Gateway**, and **AWS Elastic Disaster Recovery**.
     - **Module 10 (`Monitoring, Compliance and Governance in the AWS Cloud`)** now consolidates CloudWatch, CloudTrail, Compliance/Auditing, AWS Organizations, Governance, AWS Health, and AWS Trusted Advisor (moving Analytics to Module 8 and Compliance/Organizations out of Security).
     - **Assessments:** Every module (Modules 1–13) ends with its own **Assessment** + **Module Summary** (there is no separate standalone final course assessment item in the outline).
     - **`Next Steps: Get Started on AWS`** now includes **Spend limits**, **Projects**, **Simplified permissions**, and **Connect your AI agent**.
2. **Official Exam Prep Plan (`SB-PLAN`) is still current (no newer replacement plan):**
   - `https://aws.amazon.com/certification/certified-cloud-practitioner/` links to the official CLF-C02 Exam Prep Category hub (`https://skillbuilder.aws/category/exam-prep/cloud-practitioner-foundational-CLF-C02`), which recommends the exact same **Exam Prep Plan: AWS Certified Cloud Practitioner (CLF-C02 - English)** (`8UUCEZGNX4`, **19 trainings**, **32h 20m**, Last Update **March 18, 2026**).
   - That plan contains **9 Free items** and **10 Subscription items**. Its item #19 already reflects the updated **13-hour** `AWS Cloud Practitioner Essentials`.
   - New Skill Builder feature on the CLF-C02 Category page: **"Build my track"** — Skill Builder's AI assistant can build a personalized track from the official exam domains.
3. **Domain 1–4 Reviews (`SB-D1`–`SB-D4`) & `SB-OVW` have NOT been updated since November 1, 2025:**
   - All 4 Domain Reviews remain **Free** and **1h 5m each** (4h 20m total), Last Update **November 1, 2025**. Because they predate the 2026 AWS Support Plans overhaul and Exam Guide v1.3 (Oct 29, 2026), learners should still patch Domain 4 (`SB-D4`) and Domain 3 (`SB-D3`) with the 2026 official docs.
4. **Other Official Resources Verified Fresh in 2026:**
   - **`SB-20Q`** (Official Practice Question Set): Free, 30m, 20 Qs, Last Update **July 18, 2026**.
   - **`SB-KBA`** (Cloud Essentials Knowledge Badge Assessment): Free, 1h 30m, randomized attempts, ≥80% earns Credly badge (5–7 business days), Last Update **April 30, 2026**.
   - **Official CLF-C02 Exam Guide:** **v1.3**, published **October 29, 2026**.
   - **Official AWS Support Plans Docs:** Active plans are **Basic**, **AWS Business Support+** ($29/mo min), **AWS Enterprise Support** ($5,000/mo min, reduced from $15,000), and **AWS Unified Operations**. Developer Support, Business Support, and Enterprise On-Ramp reach End of Support on **January 1, 2027** (remaining only in AWS GovCloud (US)).

---

## Gap / Diff Table: `study-plan.md` vs. Live Primary Sources (Nov 26, 2026)

| Resource / Area | What [study-plan.md](study-plan.md) Currently Says | What Live Primary Sources Actually Show | Status / Action Needed |
| --- | --- | --- | --- |
| **`SB-ESS` Duration** | `12h 45m (~9h @ 1.4x)` | **`13 hours`** (`13h 0m`), badge `UPDATED`, Last Update **Nov 25, 2026** | **Outdated** — update to `13h (~9.3h @ 1.4x)` |
| **`SB-ESS` Block 1** | Intro to AWS + Compute (EC2, pricing, scaling, ELB, messaging, serverless/containers) | **Module 1** (Intro to Cloud + Global Infra intro + Shared Responsibility intro), **Module 2** (Compute: EC2, provisioning, EC2 demo, pricing, Auto Scaling, ELB, Messaging & Queuing), **Module 3** (Dedicated: Exploring Compute Services — Serverless/Lambda, Containers & Orchestration, Additional Compute Services) | **Outdated structure** — split into Modules 1–3 |
| **`SB-ESS` Block 2** | Global Infra & Reliability + Networking + Storage (EBS, S3, EFS) | **Module 4** (Going Global + Infrastructure & Automation), **Module 5** (Networking + VPC Demo + Global Networking), **Module 6** (Storage: EBS + lifecycle, S3 + Demo, EFS, **Amazon FSx**, **AWS Storage Gateway**, **AWS Elastic Disaster Recovery**) | **Outdated structure** — update to Modules 4–6 and add FSx, Storage Gateway, Elastic DR |
| **`SB-ESS` Block 3** | Databases (RDS, Aurora, DynamoDB, Redshift, DMS) + Security (SRM, IAM, Organizations, KMS, Shield, WAF, Inspector, GuardDuty, Compliance/Artifact) | **Module 7** (Databases: Relational, NoSQL, Demo, In-Memory Caching, Additional DB Services — *note: DB migration moved to Module 12*), **Module 8** (**NEW: AI ML and Data Analytics** — AI/ML, **Generative AI on AWS**, Data Analytics & Data Pipelines), **Module 9** (Security: Unauthorized Access, Networks/Apps, Data, Detect & Respond, Additional Security Resources — *Organizations & Compliance moved to Module 10*) | **Majorly outdated** — missing dedicated **Module 8 (AI/ML, GenAI & Data Analytics)**; Organizations/Compliance moved to Module 10; DB Migration moved to Module 12 |
| **`SB-ESS` Block 4** | Monitoring & Analytics + Pricing & Support + Migration & Innovation (CAF, 7 Rs, AI/ML) + The Cloud Journey (Well-Architected 6 Pillars) + final course assessment | **Module 10** (Monitoring, Compliance & Governance: CloudWatch, CloudTrail, Compliance/Auditing, **AWS Organizations**, Governance, AWS Health, Trusted Advisor), **Module 11** (Pricing & Support: Pricing, Billing, Support Plans, Marketplace/Partners, Cost Optimization), **Module 12** (Migrating to AWS: CAF, 7 Rs, Migration Tools, **Database Migrations**, Online/Offline Data Transfer), **Module 13** (Well-Architected Solutions: Specialized Services + Well-Architected Framework), **`Next Steps: Get Started on AWS`** (Free Tier, Spend limits, Projects, Simplified permissions, Connect your AI agent). **No separate final exam module** — each of Modules 1–13 has its own Assessment | **Majorly outdated** — realign to Modules 10–13 + Next Steps; remove "final course assessment" wording in favor of per-module assessments |
| **`SB-PLAN` (Exam Prep Plan)** | Listed as Hub (`use free items only`), no item breakdown or update date | Still current official plan (`8UUCEZGNX4`, **19 trainings**, **32h 20m**, Last Update **Mar 18, 2026**). Contains **9 Free** items (including two unlisted free short courses: *Exam Prep Plan Overview* 15m and *Exam Prep Summary* 5m) and **10 Subscription** items | **Accurate URL**, can add the official CLF-C02 Exam Prep Category Hub (`skillbuilder.aws/category/exam-prep/cloud-practitioner-foundational-CLF-C02`) and note 9 Free vs. 10 Subscription items |
| **`SB-20Q`** | Free, 20 official Qs (~30m) | **Verified accurate** — Free, 30m, 20 Qs, Last Update **July 18, 2026** | **Current** |
| **`SB-OVW`** | Free, 20m | **Verified accurate** — Free, 20m, Last Update **Nov 1, 2025** | **Current** |
| **`SB-D1` to `SB-D4`** | Free, 1h 5m each (~45m @ 1.4x) | **Verified accurate** — Free, 1h 5m each, Last Update **Nov 1, 2025**. *(Caveat: Nov 1, 2025 predates 2026 Support Plans & Exam Guide v1.3)* | **Current**, add caveat that `SB-D4` (Nov 2025) may lag 2026 Support Plans |
| **`SB-KBA`** | Free, 1h 30m, randomized every attempt (≥80% = Credly badge) | **Verified accurate** — Free, 1h 30m, randomized attempts, ≥80% earns Credly badge (5–7 business days), Last Update **April 30, 2026** | **Current** |
| **`SB-ESC`** | Free, short interactive demo (`cpe.publicdemo.escaperoom.skillbuilder.aws`) | **Verified accurate** — Live public WebGL2 demo (*Escape Room Demo - Cloud Practitioner*). Full 5h Escape Room on Skill Builder requires Subscription | **Current** |
| **`AWS-DOC` Exam Guide** | Official CLF-C02 Exam Guide v1.3 | **Verified accurate** — **v1.3** (published **October 29, 2026**) is the latest revision. In-scope list confirms Amazon Quick, SageMaker AI, WorkSpaces Secure Browser, Amazon Q | **Current** |
| **`AWS-DOC` Support Plans** | 2026 Support Plans Docs (Business Support+, Enterprise Support, Unified Operations) | **Verified accurate** — Active plans: Basic, Business Support+ ($29/mo min), Enterprise Support ($5,000/mo min), Unified Operations. Developer, Business, and Enterprise On-Ramp end **Jan 1, 2027** | **Current** |
| **`TD-FREE`** | Free, 30 Qs (15 Timed + 15 Review) | **Verified accurate** — Free, 30 Qs (15 Timed + 15 Review) + bonus **CLF-C02 Flash Cards – Part 1**. *(Note: TD's description text still has a legacy `CLF-C01` typo)* | **Current** |
| **`GH-MOCK`** | `kananinirav`, 23 sets × 50 Qs | **Verified active** — 23 practice exam sets (`practice-exam-1.html` through `practice-exam-23.html`) | **Current** |

---

## Detailed Primary-Source Findings

### 1. `SB-ESS` — AWS Cloud Practitioner Essentials (Primary Target)

- **Primary Source URL:** `https://skillbuilder.aws/learn/94T2BEN85A/aws-cloud-practitioner-essentials/8D79F3AVR7`
- **Official AWS Training Redirect Check:** `https://aws.amazon.com/training/digital/aws-cloud-practitioner-essentials/` redirects to `https://aws.amazon.com/training/learn-about/cloud-practitioner/`, which links directly to `https://skillbuilder.aws/learn/94T2BEN85A/aws-cloud-practitioner-essentials/8D79F3AVR7` (though that marketing page still prints stale duration text `12 hours 45 minutes`).
- **Course Metadata (Live Skill Builder Page):**
  - **Exact Title:** `AWS Cloud Practitioner Essentials`
  - **Status Badge:** `UPDATED`
  - **Product Type:** `Digital course`
  - **Course Duration:** **`13 hours`** (`13h` / `13h 0m`)
  - **Access / Tier:** **`Free`**
  - **Domain:** `Cloud Essentials`
  - **Level:** `Fundamental`
  - **Last Update:** **`November 25, 2026`**
  - **Languages:** `English` + 19 more
  - **Ratings:** `4.7 / 5` (88,923–88,925 reviews)
  - **Achievement:** PDF Certificate of Completion upon finishing the course

#### Official Course Objectives (Verbatim from `Details` Tab)
- Describe fundamental functions and benefits of the AWS Cloud.
- Explain how virtual compute resources are provisioned and managed in the AWS Cloud.
- Explain how AWS compute services support scalable, serverless application environments.
- Describe fundamental components and benefits of the AWS Global Infrastructure.
- Describe AWS networking components and services.
- Describe AWS storage services, storage tiers, and data lifecycle policies.
- Describe AWS database services and migration tools.
- Describe the benefits and purpose of AWS AI/ML services, AWS generative AI services, and AWS ETL data pipelines.
- Explain how AWS security services protect against network attacks, safeguard data, and help you detect and respond to security incidents.
- Describe AWS monitoring, compliance, and governance services.
- Describe fundamental concepts, services, and features of AWS Pricing and AWS Support.
- Describe AWS migration strategies and services.
- Describe specialized AWS services and the six pillars of the AWS Well-Architected Framework.

#### Exact Live Module-by-Module Syllabus (Extracted from `Outline` Tab)

1. **Module 1 - Introduction to the Cloud**
   - *MODULE 1 INTRODUCTION:* Welcome to AWS Cloud Practitioner Essentials
   - *THE AWS CLOUD:* What is Cloud Computing? · Benefits of the AWS Cloud · Introduction to AWS Global Infrastructure · The AWS Shared Responsibility Model
   - *CLOUD IN REAL LIFE:* Applying Cloud Concepts to Real Life Use Cases
   - *MODULE 1 CONCLUSION:* Assessment · Module Summary
2. **Module 2 - Compute in the Cloud**
   - *MODULE 2 INTRODUCTION:* Introduction to Amazon EC2
   - *COMPUTE IN THE CLOUD:* Amazon EC2 Instance Types · How to Provision AWS Resources · Demo: Launching an Amazon EC2 Instance · Amazon EC2 Pricing
   - *AUTO SCALING AND LOAD BALANCING:* Scaling Amazon EC2 · Directing Traffic with Elastic Load Balancing · Messaging and Queuing
   - *MODULE 2 CONCLUSION:* Assessment · Module Summary
3. **Module 3 - Exploring Compute Services**
   - *MODULE 3 INTRODUCTION:* Introduction to Serverless Computing
   - *AWS SERVERLESS, CONTAINERS, AND SOLUTIONS OVERVIEW:* AWS Lambda · Containers and Orchestration on AWS · Additional Compute Services
   - *MODULE 3 CONCLUSION:* Assessment · Module Summary
4. **Module 4 - Going Global**
   - *MODULE 4 INTRODUCTION:* Introduction to Going Global
   - *AWS GLOBAL INFRASTRUCTURE:* Choosing AWS Regions · Diving Deeper into AWS Global Infrastructure · Infrastructure and Automation
   - *MODULE 4 CONCLUSION:* Assessment · Module Summary
5. **Module 5 - Networking**
   - *MODULE 5 INTRODUCTION:* Introduction to Networking
   - *NETWORK COMPONENTS IN THE AWS CLOUD:* Organizing AWS Cloud Resources · More Ways to Connect to the AWS Cloud · Subnets, Security Groups, and Network Access Control Lists · Amazon VPC Demo · Global Networking
   - *CLOUD IN REAL LIFE:* Global Architectures
   - *MODULE 5 CONCLUSION:* Assessment · Module Summary
6. **Module 6 - Storage**
   - *MODULE 6 INTRODUCTION:* Introduction to Storage
   - *BLOCK STORAGE:* EC2 Instance Store and Amazon Elastic Block Store (Amazon EBS) · Amazon Elastic Block Store (Amazon EBS) Data Lifecycle
   - *OBJECT STORAGE:* Amazon Simple Storage Service (Amazon S3) · Amazon S3 Storage Classes and S3 Lifecycle · Amazon S3 Demonstration
   - *FILE STORAGE:* Amazon Elastic File System (Amazon EFS) · Amazon FSx
   - *ADDITIONAL STORAGE SOLUTIONS:* AWS Storage Gateway · AWS Elastic Disaster Recovery
   - *CLOUD IN REAL LIFE:* Comparing Storage Services
   - *MODULE 6 CONCLUSION:* Assessment · Module Summary
7. **Module 7 - Databases**
   - *MODULE 7 INTRODUCTION:* Introduction to Databases
   - *AWS DATABASE SERVICES:* Relational Database Services · NoSQL Database Services · AWS Databases Demonstration · In-Memory Caching Services · Additional Database Services
   - *MODULE 7 CONCLUSION:* Assessment · Module Summary
8. **Module 8 - AI ML and Data Analytics**
   - *MODULE 8 INTRODUCTION:* Introduction to AI and Machine Learning
   - *AI/ML ON AWS:* AI/ML on AWS · AWS AI/ML Solutions · Introduction to Generative AI on AWS · AWS Generative AI Solutions
   - *DATA ANALYTICS ON AWS:* Introduction to Data Analytics · Data Pipelines on AWS
   - *CLOUD IN REAL LIFE:* Data Analytics and AI/ML
   - *MODULE 8 CONCLUSION:* Assessment · Module Summary
9. **Module 9 - Security**
   - *MODULE 9 INTRODUCTION:* Introduction to Security on AWS
   - *AWS SECURITY CONTROLS:* Preventing Unauthorized Access · Protecting Networks and Applications · Protecting Data · Detecting and Responding to Security Incidents · Additional Security Resources
   - *MODULE 9 CONCLUSION:* Assessment · Module Summary
10. **Module 10 - Monitoring, Compliance and Governance in the AWS Cloud**
    - *MODULE 10 INTRODUCTION:* Introduction to Monitoring, Compliance, and Governance in the AWS Cloud
    - *MONITORING AND COMPLIANCE SERVICES:* Introduction to Monitoring · Amazon CloudWatch · AWS CloudTrail · Compliance · Auditing AWS Resources for Compliance · AWS Organizations · Governance · AWS Health · AWS Trusted Advisor
    - *MODULE 10 CONCLUSION:* Assessment · Module Summary
11. **Module 11 - Pricing and Support**
    - *MODULE 11 INTRODUCTION:* Introduction to Pricing and Support
    - *AWS PRICING:* AWS Pricing Concepts · AWS Pricing and Billing Services
    - *AWS SUPPORT:* AWS Support Plans · AWS Marketplace and AWS Partners
    - *CLOUD IN REAL LIFE:* Cost Optimization
    - *MODULE 11 CONCLUSION:* Assessment · Module Summary
12. **Module 12 - Migrating to the AWS Cloud**
    - *MODULE 12 INTRODUCTION:* Introduction to Migration
    - *MIGRATION FRAMEWORKS AND STRATEGIES:* AWS Cloud Adoption Framework · Seven Migration Strategies
    - *MIGRATION SERVICES AND TOOLS:* Migration Services and Tools
    - *MIGRATING DATABASES TO THE AWS CLOUD:* Database Migrations
    - *MIGRATING DATA TO THE AWS CLOUD:* Transferring Data Online · Transferring Data Offline
    - *MODULE 12 CONCLUSION:* Assessment · Module Summary
13. **Module 13 - Well-Architected Solutions**
    - *MODULE 13 INTRODUCTION:* Introduction to Well-Architected Solutions
    - *AWS SPECIALIZED SERVICES AND SOLUTIONS:* AWS Specialized Services · AWS Well-Architected Framework
    - *CLOUD IN REAL LIFE:* Specialized Use Cases
    - *MODULE 13 CONCLUSION:* Assessment · Module Summary · Contact Us
14. **Next Steps: Get Started on AWS**
    - *INTRODUCTION:* Getting started on AWS · Create a new AWS account · AWS Free Tier · Spend limits · Projects · Simplified permissions · Invite team members to your project · Connect your AI agent · AWS advanced features · Closing your AWS Account · Summary
15. **Feedback** & **Achievements** (PDF Certificate of completion)

---

### 2. Official CLF-C02 Exam Prep Hub & `SB-PLAN` (All 19 Trainings)

- **Official Certification Page:** `https://aws.amazon.com/certification/certified-cloud-practitioner/`
  - Links to the official Exam Guide (`https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02.html`) and the **4-step plan** at `https://skillbuilder.aws/category/exam-prep/cloud-practitioner-foundational-CLF-C02`.
- **Official Skill Builder CLF-C02 Exam Prep Category Hub:** `https://skillbuilder.aws/category/exam-prep/cloud-practitioner-foundational-CLF-C02`
  - **Option 1 (Recommended):** `Exam Prep Plan: AWS Certified Cloud Practitioner (CLF-C02 - English)` (`SB-PLAN`) — confirms this is the **sole current official Exam Prep Plan** for CLF-C02.
  - **Option 2:** Build Your Own Plan across Steps 1–4.
  - **AI Feature:** *"Already know some of this? Get a plan aimed at your gaps. Skill Builder's AI assistant builds a track from the official exam domains, personalized to where you are."* (`Build my track`).
- **Legacy Learning Plan Note:** The legacy `Cloud Essentials Learning Plan` link on `https://aws.amazon.com/training/learn-about/cloud-practitioner/` (`https://explore.skillbuilder.aws/learn/public/learning_plan/view/82/cloud-foundations-learning-plan`) is **no longer active** and redirects to Skill Builder search with banner *"This link is no longer active, but we've found similar courses based on your search."*
- **`SB-PLAN` Metadata:**
  - **URL:** `https://skillbuilder.aws/learning-plan/8UUCEZGNX4/exam-prep-plan-aws-certified-cloud-practitioner-clfc02--english/1J2VTQSGU2`
  - **Total Duration:** `32 hours 20 minutes` (`32h 20m`)
  - **Trainings Count:** `19` (**9 Free** + **10 Subscription**)
  - **Last Update:** `March 18, 2026`

#### Complete 19-Item Inventory of `SB-PLAN` (Extracted from Live `Outline` Tab)

| # | Training Title | Type | Access | Duration | Direct URL |
| :---: | --- | --- | :---: | :---: | --- |
| 1 | Exam Prep Plan Overview: AWS Certified Cloud Practitioner (CLF-C02 - English) | Certification Exam Preparation | **Free** | 15 minutes | `https://skillbuilder.aws/learn/93WN9GJ1PK/exam-prep-plan-overview-aws-certified-cloud-practitioner-clfc02--english/88Y7YE3JPK` |
| 2 | Official Practice Question Set: AWS Certified Cloud Practitioner (CLF-C02 - English) (`SB-20Q`) | Certification Exam Preparation | **Free** | 30 minutes | `https://skillbuilder.aws/learn/E4W52ZKK6P/official-practice-question-set-aws-certified-cloud-practitioner-clfc02--english/RJSZKD3MG3` |
| 3 | Official Pretest: AWS Certified Cloud Practitioner (CLF-C02 - English) | Certification Exam Preparation | Subscription | 1 hour 30 minutes | `https://skillbuilder.aws/learn/X19D6YZ5HY/official-pretest-aws-certified-cloud-practitioner-clfc02--english/GAGEDKHMET` |
| 4 | Exam Prep Overview: AWS Certified Cloud Practitioner (CLF-C02 - English) (`SB-OVW`) | Certification Exam Preparation | **Free** | 20 minutes | `https://skillbuilder.aws/learn/N7R36JEFT4/exam-prep-overview-aws-certified-cloud-practitioner-clfc02--english/D4Z29YNQVU` |
| 5 | Domain 1 Review: AWS Certified Cloud Practitioner (CLF-C02 - English) (`SB-D1`) | Certification Exam Preparation | **Free** | 1 hour 5 minutes | `https://skillbuilder.aws/learn/QQG3HTG5X9/domain-1-review-aws-certified-cloud-practitioner-clfc02--english/XN4NSNUEKK` |
| 6 | Domain 1 Practice: AWS Certified Cloud Practitioner (CLF-C02 - English) | Certification Exam Preparation | Subscription | 40 minutes | `https://skillbuilder.aws/learn/9UCEYJPBW7/domain-1-practice-aws-certified-cloud-practitioner-clfc02--english/7NT7FS1CJJ` |
| 7 | Domain 1 Practice: AWS SimuLearn - AWS Certified Cloud Practitioner (CLF-C02 - English) | AWS SimuLearn | Subscription | 1 hour | `https://skillbuilder.aws/learn/JXUDPD4QEN/domain-1-practice-aws-simulearn--aws-certified-cloud-practitioner-clfc02--english/468KTGPWDG` |
| 8 | Domain 2 Review: AWS Certified Cloud Practitioner (CLF-C02 - English) (`SB-D2`) | Certification Exam Preparation | **Free** | 1 hour 5 minutes | `https://skillbuilder.aws/learn/C2QPSGKG9W/domain-2-review-aws-certified-cloud-practitioner-clfc02--english/TB2UW9ZDZ6` |
| 9 | Domain 2 Practice: AWS Certified Cloud Practitioner (CLF-C02 - English) | Certification Exam Preparation | Subscription | 40 minutes | `https://skillbuilder.aws/learn/FBB2WCCDAA/domain-2-practice-aws-certified-cloud-practitioner-clfc02--english/1K655CMA8X` |
| 10 | Domain 2 Practice: AWS SimuLearn - AWS Certified Cloud Practitioner (CLF-C02 - English) | AWS SimuLearn | Subscription | 1 hour | `https://skillbuilder.aws/learn/TNND6DFC4K/domain-2-practice-aws-simulearn--aws-certified-cloud-practitioner-clfc02--english/P6QE5NPKTH` |
| 11 | Domain 3 Review: AWS Certified Cloud Practitioner (CLF-C02 - English) (`SB-D3`) | Certification Exam Preparation | **Free** | 1 hour 5 minutes | `https://skillbuilder.aws/learn/D42FCU5QXG/domain-3-review-aws-certified-cloud-practitioner-clfc02--english/4AWWM46ESM` |
| 12 | Domain 3 Practice: AWS Certified Cloud Practitioner (CLF-C02 - English) | Certification Exam Preparation | Subscription | 1 hour | `https://skillbuilder.aws/learn/KK7SC1E2SA/domain-3-practice-aws-certified-cloud-practitioner-clfc02--english/A7JW4ZST3G` |
| 13 | Domain 3 Practice: AWS SimuLearn - AWS Certified Cloud Practitioner (CLF-C02 - English) | AWS SimuLearn | Subscription | 1 hour | `https://skillbuilder.aws/learn/ZUY4FZ65HH/domain-3-practice-aws-simulearn--aws-certified-cloud-practitioner-clfc02--english/TTFBKXY3XJ` |
| 14 | Domain 4 Review: AWS Certified Cloud Practitioner (CLF-C02 - English) (`SB-D4`) | Certification Exam Preparation | **Free** | 1 hour 5 minutes | `https://skillbuilder.aws/learn/SZH438F6RP/domain-4-review-aws-certified-cloud-practitioner-clfc02--english/9UBJWU2Z43` |
| 15 | Domain 4 Practice: AWS Certified Cloud Practitioner (CLF-C02 - English) | Certification Exam Preparation | Subscription | 45 minutes | `https://skillbuilder.aws/learn/753JXFHECD/domain-4-practice-aws-certified-cloud-practitioner-clfc02--english/KNPUKZEF5Y` |
| 16 | AWS Escape Room: Exam Prep for AWS Certified Cloud Practitioner (CLF-C02) with Free Demo | AWS Escape Room | Subscription *(public demo free)* | 5 hours | `https://skillbuilder.aws/learn/5GRU5D1264/aws-escape-room-exam-prep-for-aws-certified-cloud-practitioner-clfc02-with-free-demo/GR8M397UAU` |
| 17 | Official Practice Exam: AWS Certified Cloud Practitioner (CLF-C02 - English) | Certification Exam Preparation | Subscription | 1 hour 30 minutes | `https://skillbuilder.aws/learn/JSJ5VBDBRG/official-practice-exam-aws-certified-cloud-practitioner-clfc02--english/FHCY1FNYXJ` |
| 18 | Exam Prep Summary: AWS Certified Cloud Practitioner (CLF-C02 - English) | Certification Exam Preparation | **Free** | 5 minutes | `https://skillbuilder.aws/learn/8VKB8VX8TH/exam-prep-summary-aws-certified-cloud-practitioner-clfc02--english/32SUM5PQR9` |
| 19 | AWS Cloud Practitioner Essentials (`SB-ESS`) | Digital course | **Free** | **13 hours** | `https://skillbuilder.aws/learn/94T2BEN85A/aws-cloud-practitioner-essentials/8D79F3AVR7` |

---

### 3. Individual Skill Builder Resources Verified

| Code | Title | Access | Duration | Last Update | Notes |
| --- | --- | :---: | :---: | :---: | --- |
| **`SB-20Q`** | Official Practice Question Set: AWS Certified Cloud Practitioner (CLF-C02 - English) | Free | 30 minutes | **July 18, 2026** | 20 official CLF-C02 questions with detailed answer-choice feedback; repeatable (same questions in different order). Source: `https://skillbuilder.aws/learn/E4W52ZKK6P/official-practice-question-set-aws-certified-cloud-practitioner-clfc02--english/RJSZKD3MG3` |
| **`SB-OVW`** | Exam Prep Overview: AWS Certified Cloud Practitioner (CLF-C02 - English) | Free | 20 minutes | **November 1, 2025** | Covers exam scope, intended audience, and topics. Source: `https://skillbuilder.aws/learn/N7R36JEFT4/exam-prep-overview-aws-certified-cloud-practitioner-clfc02--english/D4Z29YNQVU` |
| **`SB-D1`** | Domain 1 Review: AWS Certified Cloud Practitioner (CLF-C02 - English) | Free | 1 hour 5 minutes | **November 1, 2025** | Expert instructor videos covering Domain 1: Cloud Concepts. Source: `https://skillbuilder.aws/learn/QQG3HTG5X9/domain-1-review-aws-certified-cloud-practitioner-clfc02--english/XN4NSNUEKK` |
| **`SB-D2`** | Domain 2 Review: AWS Certified Cloud Practitioner (CLF-C02 - English) | Free | 1 hour 5 minutes | **November 1, 2025** | Expert instructor videos covering Domain 2: Security and Compliance. Source: `https://skillbuilder.aws/learn/C2QPSGKG9W/domain-2-review-aws-certified-cloud-practitioner-clfc02--english/TB2UW9ZDZ6` |
| **`SB-D3`** | Domain 3 Review: AWS Certified Cloud Practitioner (CLF-C02 - English) | Free | 1 hour 5 minutes | **November 1, 2025** | Expert instructor videos covering Domain 3: Cloud Technology and Services. Source: `https://skillbuilder.aws/learn/D42FCU5QXG/domain-3-review-aws-certified-cloud-practitioner-clfc02--english/4AWWM46ESM` |
| **`SB-D4`** | Domain 4 Review: AWS Certified Cloud Practitioner (CLF-C02 - English) | Free | 1 hour 5 minutes | **November 1, 2025** | Expert instructor videos covering Domain 4: Billing, Pricing, and Support. *(Updated prior to 2026 Support Plan changes.)* Source: `https://skillbuilder.aws/learn/SZH438F6RP/domain-4-review-aws-certified-cloud-practitioner-clfc02--english/9UBJWU2Z43` |
| **`SB-KBA`** | Cloud Essentials Knowledge Badge Assessment | Free | 1 hour 30 minutes | **April 30, 2026** | Digital course assessment; score ≥80% earns AWS Cloud Essentials Knowledge Badge (issued by Credly within 5–7 business days); questions are randomized on each attempt. Source: `https://skillbuilder.aws/learn/63URRERNTS/cloud-essentials-knowledge-badge-assessment/VYB4663QV9` |
| **`SB-ESC`** | Escape Room Demo - Cloud Practitioner | Free | Short demo | Live (no date shown) | Public WebGL2 browser game at `https://cpe.publicdemo.escaperoom.skillbuilder.aws/`. Full 5h version on Skill Builder requires Subscription. |

---

### 4. Official AWS Docs & Free External Resources Verified

#### A. Official CLF-C02 Exam Guide
- **Primary Source URLs:**
  - Main guide: `https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02.html`
  - Revisions: `https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/clf-02-revisions.html`
  - In-Scope Services: `https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/clf-02-in-scope-services.html`
- **Verified Revision History:**
  - `1.0` — June 24, 2026
  - `1.1` — August 28, 2026
  - `1.2` — September 24, 2026
  - **`1.3` — October 29, 2026** *(latest)*
- **Exam Format & Weightings (Unchanged):**
  - 65 questions total (**50 scored** + **15 unscored**), scaled score 100–1,000, minimum passing score **700** (compensatory scoring; no guessing penalty).
  - Domain 1: Cloud Concepts (**24%**) · Domain 2: Security and Compliance (**30%**) · Domain 3: Cloud Technology and Services (**34%**) · Domain 4: Billing, Pricing, and Support (**12%**).
- **Notable In-Scope Services Verified in v1.3:**
  - Analytics: **Amazon Quick**, Amazon Athena, Amazon EMR, AWS Glue, Amazon Kinesis, Amazon OpenSearch Service, Amazon Redshift.
  - End User Computing: Amazon AppStream 2.0, Amazon WorkSpaces, **Amazon WorkSpaces Secure Browser**.
  - Machine Learning: Amazon Comprehend, Amazon Lex, Amazon Polly, **Amazon Q**, Amazon Rekognition, **Amazon SageMaker AI**, Amazon Textract, Amazon Transcribe, Amazon Translate. *(Note: Amazon Bedrock is NOT listed in the v1.3 In-Scope Services page, even though `SB-ESS` Module 8 introduces Generative AI on AWS.)*
  - Customer Enablement: **AWS Support**.

#### B. Official AWS Support Plans Documentation (2026)
- **Primary Source URL:** `https://docs.aws.amazon.com/awssupport/latest/user/aws-support-plans.html`
- **Active Support Plans (4 Tiers):**
  1. **Basic** — 24x7 account/billing questions, support forums, service health checks, docs/best practice guides.
  2. **AWS Business Support+** — **$29/month minimum per account**; real-time contextual generative AI assistance, 24x7 phone/web/chat with Cloud Support Engineers, **<30 minutes** human engagement for business-critical system-down cases, **500+ AWS Trusted Advisor checks**, AWS Support API, third-party software support, unlimited cases.
  3. **AWS Enterprise Support** — **$5,000/month minimum** *(reduced from $15,000)*; all Business Support+ benefits plus designated Technical Account Manager (TAM), **up to 15-minute** production-critical response, **AWS Security Incident Response** at no additional cost, strategic business reviews, **AWS Countdown** event management.
  4. **AWS Unified Operations** — Application architecture guidance, infrastructure event management, designated TAM + **Domain Specialist Engineer (DSE)**, recurring subscription to **AWS Countdown Premium**, critical workload reviews, and personalized runbooks/operational procedures.
- **End of Support Notices (Effective January 1, 2027):**
  - **Developer Support**, **Business Support**, and **Enterprise On-Ramp** will be discontinued on **January 1, 2027** (Enterprise On-Ramp customers are automatically upgraded to AWS Enterprise Support throughout 2026). All three legacy plans remain available only in the **AWS GovCloud (US)** Region.

#### C. Free External Practice Resources
- **Tutorials Dojo Free CLF-C02 Sampler (`TD-FREE`):**
  - **Primary Source URL:** `https://portal.tutorialsdojo.com/courses/free-aws-certified-cloud-practitioner-practice-exams-sampler/`
  - **Verified Details:** **FREE**, instructor Jon-Bonso, **30 questions** (15 Timed Mode + 15 Review Mode), plus bonus lesson **`AWS Certified Cloud Practitioner (CLF-C02) Flash Cards – Part 1`**. *(Minor note: the top Course Description paragraph still contains a legacy `CLF-C01` typo, while the flashcards and course content target CLF-C02.)*
- **`kananinirav` Free Practice Exams (`GH-MOCK`):**
  - **Primary Source URL:** `https://kananinirav.com/practice-exam/exams.html`
  - **Verified Details:** **FREE**, lists **23 practice exams** (`Practice Exam - 1` through `Practice Exam - 23`, `practice-exam-1.html` – `practice-exam-23.html`) with answers, explanations, and reference links.

---

## Items Behind Login Wall / Not Directly Observed

To prevent any guessing or fabrication, the following internal details could **not** be directly observed without signing in / enrolling:

1. **Per-module durations & exact media format inside `SB-ESS`:** The public Skill Builder `Outline` tab exposes all 13 module titles, subsection headings, and lesson titles, plus the total duration (`13 hours`), but does **not** expose per-module durations or the exact video vs. interactive text/quiz runtime split.
2. **Exact internal lesson content of `SB-ESS` Module 11 (`Pricing and Support`):** Because `SB-ESS` was updated on **November 25, 2026**, Module 11 very likely reflects the 2026 Support Plans (`Business Support+`, `Enterprise Support`, `Unified Operations`), but the actual lesson slides are behind the Skill Builder enrollment login wall.
3. **Exact internal video content of `SB-D1`–`SB-D4`:** All four Domain Reviews show `Last Update: November 1, 2025`. Their actual video transcripts are behind login, so it is inferred (not directly viewed) that `SB-D4` may still discuss legacy Developer/Business/Enterprise On-Ramp support tiers.
4. **Exact question count & live question bank inside `SB-KBA` and `TD-FREE`:** Both require account sign-in/enrollment to launch the quiz player; only the public course descriptions and outlines were directly verified.
