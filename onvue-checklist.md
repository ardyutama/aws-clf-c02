# Pearson VUE OnVUE Online Proctoring Checklist & Exam-Day Pacing Guide (2026)

> **Verified Against:** Official [Pearson VUE OnVUE Requirements for AWS (2026)](https://www.pearsonvue.com/us/en/aws/onvue.html) + Nov 2026 `r/AWSCertifications` OnVUE pass reports.  
> **Critical Warning:** Failing OnVUE technical, room, or ID rules on exam day can result in **immediate cancellation and forfeiture of your $100 exam fee**. Run Stage 1 on **Day 2 (Nov 24)** so you have 11 days to fix any issue.

---

## Verified 2026 OnVUE Requirements (Quick Reference)

| Category | Mandatory Rule |
| --- | --- |
| **OS & Hardware** | Personal **Windows 10+** or **macOS 14+** laptop/desktop; working **webcam, microphone, and built-in/external speakers** (NO virtual machines, NO beta OS) |
| **Monitor Rule** | **ONE display screen ONLY.** Unplug all secondary monitors (and turn/cover them if physically mounted on desk). Disable/avoid touchscreen secondary displays. |
| **Ultrawide Caution** *(Nov 2026 Reddit)* | If using an ultrawide monitor, center the OnVUE window or use a standard laptop screen so you aren't turning your head left/right (proctors flag repeated off-center eye movement). |
| **Network** | Stable **private** wired/Wi-Fi network with **≥ 6 Mbps down / ≥ 2 Mbps up**. **NO VPNs**, corporate firewalls, or public/shared networks. Ask household members not to stream/download during your slot. |
| **Prohibited Items** | Headphones, earbuds, smartwatches, regular watches, phones (must be out of arm's reach after check-in photos), tablets, styluses, smart speakers (Alexa/Google Home), smart glasses, physical scratch paper, pens, books, sticky notes. |
| **Scratch Work** | **NO physical paper or whiteboard.** Use the built-in **OnVUE on-screen digital whiteboard** only (click the whiteboard icon at the top bar). |
| **Behavior on Cam** | Keep your face and shoulders inside the webcam frame at all times. **Do NOT read questions aloud or move your lips** (proctors warn/revoke for mouthing words). Do NOT leave webcam view. |
| **Government ID** | Original, unexpired, physical government-issued photo ID (Passport, Driver's License, or National ID). First & Last name **must match your AWS CertMetrics profile character-for-character**. |

---

## Stage 1 — Early Technical & Room Audit (Do on Day 2 · Tue, Nov 24)

- [ ] **Check AWS CertMetrics Profile Name:** Log in to [AWS Certification Portal (CertMetrics)](https://cp.certmetrics.com/amazon/en/login) and confirm your **exact legal name** matches your physical government ID (no nicknames or missing middle-name mismatches).
- [ ] **Run Official OnVUE System Test:** Run [Pearson VUE AWS OnVUE System Test](https://system-test.onvue.com/system_test?customer=pearson_vue&clientcode=AWS&locale=en_US) on the **exact computer and exact Wi-Fi/Ethernet network** you will use on Dec 5.
  - [ ] Webcam check passed
  - [ ] Microphone & speaker check passed (without headphones!)
  - [ ] Network speed check passed (≥6 Mbps down / ≥2 Mbps up, VPN OFF)
  - [ ] Sample OnVUE exam screen launched cleanly
- [ ] **Audit Your Testing Room:**
  - [ ] Private, quiet, well-lit room with a **closable door** (nobody can walk in during the 90 minutes).
  - [ ] Plan where your unplugged second monitor, papers, books, and smart speakers will go.
  - [ ] Confirm you have an Ethernet cable (or strong router signal) and laptop power adapter ready.
- [ ] **Check Exam Appointment Details:** Confirm exact start time & timezone for **Saturday, Dec 5, 2026** in CertMetrics.

---

## Stage 2 — Full Paperless Dress Rehearsal (Do on Day 10 · Thu, Dec 3)

- [ ] Clear your desk **100% identically** to exam day (single screen, power cord, mouse/keyboard only).
- [ ] Re-run the [Pearson VUE OnVUE System Test](https://system-test.onvue.com/system_test?customer=pearson_vue&clientcode=AWS&locale=en_US) to verify no OS update broke OnVUE.
- [ ] Take **Skill Builder Knowledge Badge Assessment Run #3** silently (no muttering, no physical notes, eyes centered on screen, phone in another corner) to verify 90-minute focus comfort.

---

## Night Before — Friday, Dec 4 (10 Minutes Before 8:00 PM)

- [ ] Clear your entire desk surface and everything within arm's reach (clear transparent water glass only if allowed — safest option: keep desk completely empty).
- [ ] Unplug any external/secondary monitors, docking-station extra displays, headphones, and USB drives.
- [ ] Pause Windows Updates (`Settings → Windows Update → Pause for 1 week`) so Windows cannot force a reboot or popup tomorrow morning.
- [ ] Restart your computer cleanly and verify audio works through **speakers** (not headset).
- [ ] Place your **physical Government ID** next to your laptop and charge your **smartphone** (needed strictly for taking the 4 check-in room photos + ID photo via QR/SMS link).
- [ ] Put a **"DO NOT ENTER — ONLINE EXAM IN PROGRESS"** sign on your door.

---

## Exam Morning — Saturday, Dec 5 (Timeline)

- [ ] **T-90 min (20m max):** Light warm-up on `CLF-C02::06_Mistakes` + 2026 Support Plans table. Eat a light breakfast; use the restroom **before** check-in.
- [ ] **T-45 min:**
  - [ ] Restart PC once cleanly.
  - [ ] Close **all** background apps (VS Code, browsers except launch tab, Slack, Teams, Discord, Steam, VPN, Grammarly, screen recorders, clipboard managers, tray updaters — check Task Manager!).
  - [ ] Mute your phone's notifications (keep volume on **only** if proctor calls during check-in; after check-in, silence and place **out of arm's reach** behind/across the room).
  - [ ] Remove watch, headphones, earbuds, hoodie/hat.
- [ ] **T-30 min (Check-In Window Opens):**
  - [ ] Log in to [CertMetrics](https://cp.certmetrics.com/amazon/en/login) → *Manage Pearson VUE Exams* → click your CLF-C02 appointment → **Begin Exam**.
  - [ ] Download/run the OnVUE client, enter access code, complete **headshot + ID front/back + 4 room photos (front, back, left, right)** on your phone.
  - [ ] Put phone **out of arm's reach** (visible/away from desk). Wait calmly in the webcam queue until the proctor releases the exam (usually 5–15 min; do not walk away!).

---

## 90-Minute Exam Execution: The Two-Pass Strategy

> **Exam Structure:** **65 questions** (50 scored + 15 unscored) in **90 minutes** = **~83 seconds/question**. No penalty for guessing; unanswered = wrong.

### Pass 1 — Fast Certainty Sweep (`0:00 → 0:50` · ~45 sec/question)
1. **Read the LAST sentence first** (the actual question + whether it asks for **ONE**, **TWO**, or **THREE** answers), then scan the scenario for the **1–2 real constraints** — ignore distracting fluff.
2. **Instant Know (>85% sure):** Select the answer(s) and move immediately.
3. **Uncertain / Wordy / Close Pair:** Pick your best provisional guess (never leave blank!), click **Flag for Review**, and move on within 60 seconds. Do not burn 4 minutes fighting Question #7 (it might even be one of the 15 unscored pretest questions!).

### Pass 2 — Rational Elimination (`0:50 → 1:25` · ~35 minutes)
1. Open the **Review Screen** and work through **Flagged Questions** one by one.
2. Use the on-screen strikethrough / elimination mental model:
   - Eliminate out-of-category services first (e.g., question asks for *auditing API calls* → immediately drop CloudWatch/GuardDuty).
   - Check key constraints: *"least operational overhead"* → **managed/serverless**; *"lowest cost"* → **Spot / Glacier Deep Archive / S3 Intelligent-Tiering / Savings Plans**; *"no single point of failure"* → **Multi-AZ**.
   - Don't change a Pass-1 answer unless you find a **clear, factual reason** you misread a constraint.

### Final Sweep (`1:25 → 1:30` · Last 5 minutes)
1. Confirm **65/65 answered** (`0 incomplete`).
2. Double-check every **"Choose TWO / Choose THREE"** question has the exact required number of selections.
3. Submit, complete the short end-of-exam survey, and note your **on-screen `PASS` confirmation**.

---

## Post-Exam Notes
- Save/screenshot (on your phone *only after* OnVUE fully closes!) or bookmark your confirmation email/receipt.
- Because your exam is on **Saturday**, your official score report (100–1,000), domain breakdown, **50% off next exam voucher**, and **Credly digital badge** may take **1–5 business days** (often arriving Sunday evening or Monday).
