# Anki 11-Day Sprint Setup Guide (CLF-C02 Cram Mode)

> **Why custom settings matter:** Default Anki scheduling optimizes for multi-year retention — pressing `Good` twice pushes a card out past your **December 5, 2026** exam date! These sprint settings force every card to resurface **at least 3–4 times** before Exam Day while honoring **Sunday, November 29 strictly OFF**.

---

## Step 1 — Install & Create Deck Hierarchy (5 Minutes on Day 1)

1. Install **Anki Desktop** (Windows/macOS/Linux) from https://apps.ankiweb.net/ and create a free **AnkiWeb** account if you want optional sync to AnkiDroid (free) or AnkiMobile.
2. Import all **5 starter `.tsv` files** from this `anki/` folder (`File → Import...` one file at a time):
   - [01_Domain1_CloudConcepts.tsv](01_Domain1_CloudConcepts.tsv) — **28 cards** → `CLF-C02::01_Domain1_CloudConcepts`
   - [02_Domain2_Security.tsv](02_Domain2_Security.tsv) — **35 cards** → `CLF-C02::02_Domain2_Security`
   - [03_Domain3_TechServices.tsv](03_Domain3_TechServices.tsv) — **45 cards** → `CLF-C02::03_Domain3_TechServices`
   - [04_Domain4_BillingSupport.tsv](04_Domain4_BillingSupport.tsv) — **22 cards** → `CLF-C02::04_Domain4_BillingSupport`
   - [05_LookAlikes_2026Delta.tsv](05_LookAlikes_2026Delta.tsv) — **20 cards** → `CLF-C02::05_LookAlikes_2026Delta`
   - *(Each file contains built-in Anki headers `#separator:tab`, `#html:true`, `#notetype:Basic`, `#deck:...`, `#tags column:3` — Anki auto-detects everything on import! Verify preview shows `Front`, `Back`, `Tags`, then click **Import**.)*
3. Manually create one empty subdeck for your mock errors:
   - Click **Create Deck** → name it exactly: `CLF-C02::06_Mistakes`

Your final deck tree will look like:
```text
CLF-C02
├── 01_Domain1_CloudConcepts   (28 starter cards)
├── 02_Domain2_Security        (35 starter cards)
├── 03_Domain3_TechServices    (45 starter cards)
├── 04_Domain4_BillingSupport  (22 starter cards)
├── 05_LookAlikes_2026Delta    (20 starter cards)
└── 06_Mistakes                (5–10 custom cards/day from mocks!)
```

---

## Step 2 — Configure 11-Day Sprint Options Preset

Click the gear icon next to the parent **`CLF-C02`** deck → **Options** → top-right dropdown → **Add Preset** → name it **`CLF-C02 11-Day Sprint`**, apply these exact settings, and click **Save to All Subdecks**:

### Daily Limits
- **New cards/day:** `25` *(Days 1–6: study from the specific subdeck scheduled in [../study-plan.md](../study-plan.md); after Day 6, all 150 starter cards are unlocked and only `06_Mistakes` adds new cards!)*
- **Maximum reviews/day:** `9999` *(never cap reviews during an 11-day sprint — you want to see every due card).*
- **New/review order:** `Show after reviews` *(ALWAYS clear reviews first).*

### Scheduling — Pick Option A (Recommended: FSRS) OR Option B (Classic SM-2)

| Setting | Option A: **FSRS (Anki 23.10+ Recommended)** | Option B: **Classic SM-2** |
| --- | --- | --- |
| **Enable FSRS** | **ON** | OFF |
| **Desired retention** | **`0.93`** *(tighter intervals suited to a 11-day exam)* | N/A |
| **Learning steps** | `10m 1h` | `10m 1h 6h` |
| **Relearning steps** | `10m` | `10m 1h` |
| **Graduating interval** | *(handled by FSRS)* | `1` day |
| **Easy interval** | *(handled by FSRS)* | `3` days |
| **Maximum interval** | **`4` days** *(CRITICAL — guarantees every card returns before Dec 5!)* | **`4` days** |
| **Bury related siblings** | OFF | OFF |

> **Why `Maximum interval = 4 days`?** In an 11-day sprint, capping the max interval at **4 days** ensures even cards you learn on Day 1 resurface on Days 2, 5, 8/9, and 11 — zero cards go stale before Saturday, Dec 5.

---

## Step 3 — Daily Pacing & Grading Rules

| Day | New Starter Quota | Subdeck Focus |
| --- | :---: | --- |
| **Day 1 (Mon Nov 23)** | 25 new | `01_Domain1_CloudConcepts` |
| **Day 2 (Tue Nov 24)** | 25 new | `03_Domain3_TechServices` (first 25) |
| **Day 3 (Wed Nov 25)** | 25 new | `02_Domain2_Security` (first 25) |
| **Day 4 (Thu Nov 26)** | 25 new | `04_Domain4_BillingSupport` (22) + 3 from `01_Domain1` |
| **Day 5 (Fri Nov 27)** | 25 new | `05_LookAlikes_2026Delta` (20) + 5 from `02_Domain2` |
| **Day 6 (Sat Nov 28)** | 25 new | Remaining 5 from `02_Domain2` + remaining 20 from `03_Domain3` → **150/150 active!** |
| **OFF (Sun Nov 29)** | **0** | **DO NOT OPEN ANKI.** |
| **Day 7 (Mon Nov 30)** | `06_Mistakes` only | Clear 2-day backlog (35–40 min buffer already scheduled!) |
| **Days 8–9 (Dec 1–2)** | `06_Mistakes` only | Clear all reviews daily + 5–10 Mistake Cards from mocks |
| **Days 10–11 (Dec 3–4)** | Cram Mode | Clear due reviews + run **Filtered Cram Deck** (below) |
| **Exam Morning (Dec 5)** | Warm-up only | Quick 20-min pass on `06_Mistakes` + Look-Alikes only |

### Strict Honest Grading Rule
- Press **`Again` (1)** if you hesitated >5 seconds, confused two services, or only "kind of" recognized the answer after flipping.
- Press **`Hard` (2)** if you got it right with noticeable effort.
- Press **`Good` (3)** if you recalled it accurately within ~3–5 seconds.
- **Avoid `Easy` (4)** during Days 1–9 unless a concept is 100% trivial (e.g., S3 = object storage).

---

## Step 4 — Handling Sunday, Nov 29 Strictly OFF

You do **not** need any Anki add-on for a single rest day:
1. Finish Saturday, Nov 28 reviews normally.
2. Do **not** open Anki at all on Sunday, Nov 29.
3. On **Monday, Nov 30**, Anki's queue will contain Sunday + Monday due cards (~70–100 cards, taking ~30–40 minutes). Clear it first thing in the **0:00–0:40** catch-up block in [../study-plan.md](../study-plan.md) before starting Mock #2.

---

## Step 5 — Days 10–11 Filtered Cram Deck (Final Lock-In)

On **Thursday, Dec 3** and **Friday, Dec 4**, after finishing normal due reviews, create a temporary Filtered Deck to hammer your highest-risk cards:

1. Press **`F`** in Anki Desktop (or `Tools → Create Filtered Deck`).
2. Name it: **`CLF-C02 Final Cram`**
3. **Search query** (paste verbatim):
   ```text
   (deck:"CLF-C02::06_Mistakes" OR deck:"CLF-C02::05_LookAlikes_2026Delta" OR prop:lapses>=1) -is:suspended
   ```
4. **Limit:** `100` cards · **Order:** `Most lapses` (or `Random`).
5. **Reschedule cards based on my answers in this deck:** **UNCHECKED** *(so cramming doesn't corrupt your regular review intervals)*.
6. Click **Build**, drill through once on Thursday and once on Friday, then click **Empty** (never delete the underlying cards) after Exam Day.

---

## Step 6 — Writing Great `06_Mistakes` Cards (Template)

Keep Mistake Cards **atomic (one concept per card)** and contrast the distractor you fell for:

- **Bad Card:** *Front: Tell me everything about AWS Security services.* *(Too broad — causes review fatigue.)*
- **Good Card:**
  - **Front:** *Mock Trap: Which service checks EC2 & ECR container images for software CVEs (GuardDuty vs. Inspector)?*
  - **Back:** *<b>Amazon Inspector</b> = automated vulnerability scanning (CVEs, network exposure) on EC2, ECR, Lambda.<br><i>Why not GuardDuty?</i> GuardDuty detects active malicious threats from CloudTrail/DNS/VPC Flow logs.*
