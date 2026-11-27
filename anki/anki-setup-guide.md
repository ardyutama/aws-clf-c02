# Anki 8-Day Recovery Sprint Setup Guide (Nov 27 – Dec 5, 2026)

> **Why tightened sprint settings matter:** With **8 days left** before your **December 5, 2026** exam and **130/150 starter cards remaining** (20 already completed), default Anki intervals push cards past Exam Day. These tightened settings unlock **100% of your 150 starter cards by Tuesday, Dec 1**, cap intervals at **3 days** so even the last batch resurfaces **3–4 times** before Saturday, and keep **Sunday, Nov 29 strictly to ~30 minutes of due reviews only**.

---

## Step 1 — Deck Hierarchy (Already Imported)

Your 5 starter `.tsv` decks in this `anki/` folder total **150 cards** (plus your custom mistakes subdeck):
- [01_Domain1_CloudConcepts.tsv](01_Domain1_CloudConcepts.tsv) — **28 cards** → `CLF-C02::01_Domain1_CloudConcepts`
- [02_Domain2_Security.tsv](02_Domain2_Security.tsv) — **35 cards** → `CLF-C02::02_Domain2_Security`
- [03_Domain3_TechServices.tsv](03_Domain3_TechServices.tsv) — **45 cards** → `CLF-C02::03_Domain3_TechServices`
- [04_Domain4_BillingSupport.tsv](04_Domain4_BillingSupport.tsv) — **22 cards** → `CLF-C02::04_Domain4_BillingSupport`
- [05_LookAlikes_2026Delta.tsv](05_LookAlikes_2026Delta.tsv) — **20 cards** → `CLF-C02::05_LookAlikes_2026Delta`
- `CLF-C02::06_Mistakes` — manual subdeck for mock errors & lucky guesses (5–8/day in Week 2)

```text
CLF-C02
├── 01_Domain1_CloudConcepts   (28 starter cards)
├── 02_Domain2_Security        (35 starter cards)
├── 03_Domain3_TechServices    (45 starter cards)
├── 04_Domain4_BillingSupport  (22 starter cards)
├── 05_LookAlikes_2026Delta    (20 starter cards)
└── 06_Mistakes                (5–8 custom cards/day from mocks!)
```

---

## Step 2 — Retune Options Preset for 8-Day Recovery Sprint (Do Today · Fri, Nov 27)

Click the gear icon next to the parent **`CLF-C02`** deck → **Options** → update your sprint preset (`CLF-C02 8-Day Recovery`), apply these exact values, and click **Save to All Subdecks**:

### Daily Limits
- **New cards/day:** `35` *(Fri Nov 27 – Tue Dec 1: pulls 30–35 new/day from the scheduled subdecks in [../study-plan.md](../study-plan.md); after Tue Dec 1, all 150/150 starter cards are active and only `06_Mistakes` adds new cards!)*
- **Maximum reviews/day:** `9999` *(never cap reviews during the final 8 days — clear every due card daily).*
- **New/review order:** `Show after reviews` *(ALWAYS clear due reviews first).*

### Scheduling — Pick Option A (Recommended: FSRS) OR Option B (Classic SM-2)

| Setting | Option A: **FSRS (Anki 23.10+ Recommended)** | Option B: **Classic SM-2** |
| --- | --- | --- |
| **Enable FSRS** | **ON** | OFF |
| **Desired retention** | **`0.94`** *(tightened for an 8-day final sprint)* | N/A |
| **Learning steps** | `10m 1h` | `10m 1h 6h` |
| **Relearning steps** | `10m` | `10m 1h` |
| **Graduating interval** | *(handled by FSRS)* | `1` day |
| **Easy interval** | *(handled by FSRS)* | **`2`** days |
| **Maximum interval** | **`3` days** *(CRITICAL — guarantees 3–4 passes before Dec 5!)* | **`3` days** |
| **Bury related siblings** | OFF | OFF |

> **Why `Maximum interval = 3 days`?** In an 8-day recovery sprint, capping the max interval at **3 days** guarantees cards unlocked today (Nov 27) resurface on Nov 28 → Dec 1 → Dec 4, and even your final batch on **Tuesday, Dec 1** resurfaces on Dec 2 → Dec 3/4 Cram Deck → Dec 4/5 — zero cards go cold before Saturday morning.

---

## Step 3 — Restructured Daily Pacing (Starting From 20/150 Done)

> **Deck assumption:** Assumes your first 20 cards are in `01_Domain1_CloudConcepts`. If they were spread across other decks, simply unlock **30–35 new cards/day** in order (`01 → 03 → 02 → 04 → 05`) so your cumulative total hits **150/150 on Tuesday, Dec 1**.

| Day | New Starter Quota | Cumulative Active | Subdeck Focus (Synced to `SB-ESS` & Mocks) |
| --- | :---: | :---: | --- |
| **Completed (Nov 23–26)** | 20 done | `20 / 150` | `01_Domain1_CloudConcepts` (first 20) |
| **Day 1 (Fri Nov 27)** | **+30 new** | `50 / 150` | Remaining **8** of `01_Domain1` + first **22** of `03_Domain3` *(matches M3–M6)* |
| **Day 2 (Sat Nov 28)** | **+35 new** | `85 / 150` | Remaining **23** of `03_Domain3` *(done!)* + first **12** of `02_Domain2` *(matches M7–M11)* |
| **REST (Sun Nov 29)** | **+0 new** | `85 / 150` | **Due reviews ONLY (~25–30m)** — zero new cards, zero courses/mocks |
| **Day 3 (Mon Nov 30)** | **+35 new** | `120 / 150` | Remaining **23** of `02_Domain2` *(done!)* + first **12** of `04_Domain4` *(matches M12–M13 + Docs Patch)* |
| **Day 4 (Tue Dec 1)** | **+30 new** | **`150 / 150`** | Remaining **10** of `04_Domain4` + all **20** of `05_LookAlikes_2026Delta` → **100% ACTIVE!** |
| **Day 5 (Wed Dec 2)** | `06_Mistakes` only | `150 + Mistakes` | Clear all due reviews + 5–8 Mistake Cards from `SB-KBA` & `GH-MOCK` |
| **Day 6 (Thu Dec 3)** | Cram Mode #1 | `150 + Mistakes` | Clear due reviews + **Filtered Cram Deck Pass #1** |
| **Day 7 (Fri Dec 4)** | Cram Mode #2 | `150 + Mistakes` | Clear due reviews + **Filtered Cram Deck Pass #2** *(stop by 8 PM)* |
| **Exam Morning (Dec 5)** | Warm-up only | Warm-up | Quick **20-min** pass on `06_Mistakes` + `05_LookAlikes_2026Delta` only |

### Strict Honest Grading Rule
- Press **`Again` (1)** if you hesitated >5 seconds, confused two services, or only "kind of" recognized the answer after flipping.
- Press **`Hard` (2)** if you got it right with noticeable effort.
- Press **`Good` (3)** if you recalled it accurately within ~3–5 seconds.
- **Avoid `Easy` (4)** during Days 1–6 unless a concept is 100% trivial (e.g., S3 = object storage).

---

## Step 4 — Handling Sunday, Nov 29 (Active Rest: Reviews ONLY ~30m)

To keep Sunday restful while preventing a 100-card Monday queue:
1. Open Anki **Options** on `CLF-C02` → under **This deck / Today only**, temporarily set **New cards/day = `0`** (so Anki does NOT show new starter cards on Sunday).
2. Clear every due review card (~65–75 cards, taking **~25–30 minutes**).
3. Close Anki immediately and enjoy the rest of Sunday 100% study-free. *(The `Today only` override resets automatically on Monday morning back to `35`!)*

---

## Step 5 — Thu Dec 3 & Fri Dec 4 Filtered Cram Deck (Final Lock-In)

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
