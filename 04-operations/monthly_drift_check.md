# NIVESHAK MONTHLY DRIFT CHECK

**Reference:** `01-master/master_orchestration.md`
**Version:** 2.0 (System-Level Integrity Audits)
**Runs:** First Sunday of every month

---

## 🔵 MONTHLY SIGNAL AUDIT

**Purpose:** Ensure signal layer coverage and quality

### Review Last 4 Weeks:

**From `05-signals/weekly_market_signals.md`:**

- [ ] Total signals logged: ____
- [ ] Structural signals: ____ (target >80%)
- [ ] Noise signals: ____ (target <20%)
- [ ] Prediction creep incidents: ____ (target: 0)

**Sector Coverage Analysis:**

- [ ] Are we over-focusing on one sector? (Max 30% concentration)
- [ ] Are we missing obvious regimes? (Cross-check with actual market)
- [ ] Governance coverage adequate? (Min 20% of signals)
- [ ] Flow signals balanced? (FII/DII/retail/bulk deals)

**From `05-signals/regulatory_watch.md`:**

- [ ] Total governance signals: ____
- [ ] SEBI circulars covered: ____
- [ ] Company disclosures tracked: ____
- [ ] Any major regulatory shift missed?

**From `05-signals/reader-signals.md`:**

- [ ] High-signal reader contributions: ____
- [ ] Content ideas generated from comments: ____
- [ ] Framework weaknesses surfaced: ____
- [ ] Conversion rate (reader signals → published posts): ____%

**From `05-signals/earnings_calendar.md`:**

- [ ] Earnings tracked: ____
- [ ] Tuesday Audits completed: ____
- [ ] Missed earnings (should have covered): ____

### Action Items:

- [ ] Update `framework_performance.md` with monthly signal audit
- [ ] If sector concentration >30% → Diversify next month's focus
- [ ] If governance <20% → Increase regulatory monitoring
- [ ] If conversion rate <10% → Review audience quality

---

## 🔵 MONTHLY ENGINE DRIFT AUDIT

**Purpose:** System-level engine health monitoring

### For EACH Engine (01-16):

Review from `model_health_log.md` + individual engine outputs:

#### ENGINE 01 — SIGNAL COLLECTOR

- [ ] Signal quality score: ____ (target >80%)
- [ ] Noise ratio: ____ (target <20%)
- [ ] Structural focus maintained? (Yes/No)
- [ ] Action: _____________________

#### ENGINE 03 — GEMINI DEEP RESEARCH

- [ ] Hallucination incidents: ____ (target: 0)
- [ ] Data depth score: ____
- [ ] Thesis coherence: ____
- [ ] Action: _____________________

#### ENGINE 04 — CHATGPT DEEP RESEARCH

- [ ] Context quality: ____
- [ ] Historical accuracy: ____
- [ ] Peer analysis depth: ____
- [ ] Action: _____________________

#### ENGINE 05 — CROSS-VERIFICATION

- [ ] Wrong data passed: ____ (target: 0)
- [ ] FAIL rate: ____ (target: 30-50%, shows rigor)
- [ ] 2-source compliance: ____%
- [ ] Action: _____________________

#### ENGINE 06 — CONTROLLED PATCH MODE

- [ ] Patches executed: ____
- [ ] Patch success rate: ____%
- [ ] Unauthorized edits: ____ (target: 0)
- [ ] **Insight preservation rate: ____% (target: 100%)**
- [ ] **Thesis drift incidents: ____ (target: 0)**
- [ ] Action: _____________________

### Monthly Engine Performance Audit

#### ENGINE 04.1 — Draft Generator
- [ ] % examples rejected by verification: ____
- [ ] Hallucination rate: ____
- [ ] Target: <20% example rejection, 0% hallucination
- [ ] Action: _____________________

#### ENGINE 05A — Insight Distiller
- [ ] Are insights surviving verification? ____%
- [ ] Any forced thesis rewrites? ____
- [ ] Target: >80% insight survival, 0 thesis rewrites
- [ ] Action: _____________________

#### ENGINE 07 — RED TEAM

- [ ] Approval rate: ____% (target: 50-70%, not >80%)
- [ ] Rejection reasons logged? (Yes/No)
- [ ] Prediction creep caught: ____
- [ ] Voice drift caught: ____
- [ ] Action: _____________________

#### ENGINE 08 — APEX SYNTHESIZER

- [ ] New data introduced: ____ (target: 0)
- [ ] Framework quality: ____
- [ ] Thesis durability: ____
- [ ] Invalidation logic present: ____%
- [ ] Action: _____________________

#### ENGINE 09 — FINAL EDITORIAL POLISH

- [ ] AI-tells escaped: ____ (target: 0)
- [ ] Claim drift incidents: ____ (target: 0)
- [ ] Tone consistency: ____
- [ ] Action: _____________________

#### ENGINE 10-12 — PLATFORM ADAPTERS

- [ ] Voice maintained across platforms? (Yes/No)
- [ ] Redirect abuse detected? (Yes/No)
- [ ] Platform-specific tone respected? (Yes/No)
- [ ] Action: _____________________

#### ENGINE 13 — VISUAL INTELLIGENCE

- [ ] Visual errors published: ____ (target: 0)
- [ ] Killer visual success rate: ____%
- [ ] Decorative visuals: ____ (target: 0)
- [ ] Action: _____________________

#### ENGINE 14 — COMMENT ENGINE

- [ ] High-signal readers identified: ____
- [ ] Error corrections issued: ____ (<24hr?)
- [ ] Tier-1 reader growth: ____
- [ ] Action: _____________________

#### ENGINE 15 — MARKET CORRESPONDENT

- [ ] Posts per week avg: ____ (target ≤3)
- [ ] Insight > Trend compliance: ____%
- [ ] Prediction language: ____ (target: 0)
- [ ] Intelligence conversion: ____%
- [ ] Action: _____________________

#### ENGINE 16 — WEEKLY MARKET INTELLIGENCE

- [ ] Weekly memos completed: ____ (target: 4)
- [ ] 6-dimension scan compliance: ____%
- [ ] Regime shifts captured: ____
- [ ] Action: _____________________

### Engine Suspension Decisions:

- [ ] Any engine flagged for suspension? Which: __________
- [ ] Suspension rationale: _____________________
- [ ] Replacement model identified: _____________________

---

## 🔵 MONTHLY CONTENT QUALITY AUDIT

**Purpose:** Strategic content performance review

### From `post_index.md` (Last 30 Days):

**Publication Stats:**

- [ ] Total posts published: ____ (target: 12-15)
- [ ] Sunday Briefs: ____
- [ ] Tuesday Audits: ____
- [ ] Friday Macros: ____
- [ ] Market Correspondent: ____
- [ ] Weekly Intelligence: ____

**Framework Analysis:**

From `frameworks_index.md`:

- [ ] Total frameworks used: ____
- [ ] Most used framework: __________ (usage: ___%)
- [ ] Least used framework: __________ (usage: ___%)
- [ ] Framework balance healthy? (No single >40%)

**Signature Metrics:**

- [ ] Posts with signature metric: ____%
- [ ] Posts with invalidation metric: ____%
- [ ] Posts with "What We're Watching": ____%
- [ ] Compliance rate: ____%

**Quality Metrics:**

From `failure_log.md` + Red Team verdicts:

- [ ] Wrong facts published: ____ (target: 0)
- [ ] Corrections issued: ____
- [ ] Red Team kills: ____
- [ ] Kill rate: ____% (healthy: 10-20%)

### Kill Rate Analysis:

From `killed_ideas.md`:

- [ ] Total ideas killed: ____
- [ ] Kill reasons:
  - [ ] Data issues: ____
  - [ ] Weak thesis: ____
  - [ ] Voice drift: ____
  - [ ] Prediction creep: ____

**Healthy Range:** 10-20% kill rate
- If <10% → Standards may be slipping
- If >30% → Research quality needs improvement

### Reader Engagement:

From `high_signal_readers.md` + engagement metrics:

- [ ] Tier-1 readers: ____ (growth: ____)
- [ ] Comment quality improving? (Yes/No)
- [ ] Reader signals → content conversion: ____%

---

## 🔵 MONTHLY NARRATIVE BIAS CHECK

**Purpose:** Prevent institutional bias formation

### Sector Exposure Review:

- [ ] IT: ____%
- [ ] BFSI: ____%
- [ ] Pharma: ____%
- [ ] Auto: ____%
- [ ] Infra: ____%
- [ ] Consumer: ____%
- [ ] Other: ____%

**Warning:** If any sector >40% → Deliberate diversification required

### Thesis Bias Check:

- [ ] Bullish theses: ____%
- [ ] Bearish theses: ____%
- [ ] Neutral/diagnostic: ____%

**Target:** Neutral/diagnostic should be >50%

### Governance Coverage:

- [ ] Posts with governance angle: ____%
- [ ] Posts with regime analysis: ____%

**Target:** Governance >30%, Regime >40%

---

## 🔵 MONTHLY FEEDBACK LOOP AUDIT

**Purpose:** Verify all 4 loops functioning

### LOOP 1 — SIGNAL → CONTENT

- [ ] Signals from `weekly_market_signals.md` → Research → Blogs
- [ ] Conversion rate: ____%
- [ ] Loop functioning? (Yes/No)

### LOOP 2 — CONTENT → CROWD → SIGNAL

- [ ] Comments → `reader-signals.md` → New ideas
- [ ] Conversion rate: ____%
- [ ] Loop functioning? (Yes/No)

### LOOP 3 — REAL-TIME → STRATEGY

- [ ] MC insights → Reinforced in blogs <2 weeks
- [ ] Compliance rate: ____%
- [ ] Loop functioning? (Yes/No)

### LOOP 2.5 — MISSED SIGNAL CORRECTIVE ACTION (NEW, MANDATORY)

**Purpose:** System self-correction when market signals are missed.

Once per month, identify missed signals:

- [ ] Review market events from past month
- [ ] Cross-check against `weekly_market_signals.md`
- [ ] Identify 3-5 major signals that were NOT written about

For each missed signal, classify failure:

- [ ] Blind spot (sector we don't monitor)
- [ ] Speed failure (signal was logged but not researched)
- [ ] Data failure (wrong data in signal file)
- [ ] Framework failure (we saw it but framework didn't trigger analysis)

**Corrective Actions:**

If BLIND SPOT:
- [ ] Add sector to permanent watchlist
- [ ] Update `frameworks_index.md` to include sector
- [ ] Log in `failure_log.md`

If SPEED FAILURE:
- [ ] Check `signal_action_log.md` — why wasn't research triggered?
- [ ] Adjust ENGINE 15 monitoring rules if needed
- [ ] Identify content pipeline bottleneck

If FRAMEWORK FAILURE:
- [ ] Update framework in `frameworks_index.md`
- [ ] Add failure note to `niveshak_bible.md`
- [ ] Schedule framework teaching post

If DATA FAILURE:
- [ ] Correct `weekly_market_signals.md` entry
- [ ] Add note: "Corrected [date] — impact on [posts]"
- [ ] Log in `model_health_log.md`

**Record:**
- [ ] Missed signals identified: ____
- [ ] Root causes: ____
- [ ] Corrections implemented: ____
- [ ] Future prevention: ____

---

### LOOP 4 — QUALITY CONTROL

- [ ] Red Team failures → Engine tightening → Bible updates
- [ ] Actions taken this month: ____
- [ ] Loop functioning? (Yes/No)

---

## 🔵 FRAMEWORK PERFORMANCE AUDIT (NEW - MANDATORY)

**Purpose:** Track framework effectiveness and retirement candidates

Review `framework_performance.md`:

- [ ] Update framework usage counts from past month's posts
- [ ] Calculate win/loss rates for each framework used
- [ ] Identify frameworks with <50% win rate (retirement candidates)
- [ ] Identify frameworks unused for 6+ months
- [ ] Update framework status (STRONG/WEAK/FAILED/RETIRED)

**Framework Win Rate Check:**
- [ ] Frameworks with 80%+ win rate: ____
- [ ] Frameworks with <50% win rate: ____
- [ ] Frameworks to retire this month: ____

**Action Items:**
- [ ] Frameworks to reinforce in content: ____
- [ ] Frameworks to teach (low familiarity): ____
- [ ] Framework gaps identified: ____
- [ ] Retirement notes documented: ____

---

## 🔴 MONTHLY ACTION ITEMS

Based on audits above:

### Immediate Actions (This Week):

1. _____________________________________
2. _____________________________________
3. _____________________________________

### Strategic Actions (This Month):

1. _____________________________________
2. _____________________________________
3. _____________________________________

### Engine Updates Required:

- [ ] Tighten prompts for: __________
- [ ] Replace model for: __________
- [ ] Suspend: __________

### Bible Updates Required:

- [ ] Add framework guidance: __________
- [ ] Update voice rules: __________
- [ ] Add safety rule: __________

---

## 🟢 MONTHLY SIGN-OFF

**System Health Score:** ____ / 100

**Chief Editor Approval:** ___________
**Date:** ___________

**Major Concerns:** _____________________

**Next Month Focus:** _____________________

---

END OF MONTHLY DRIFT CHECK

---

## 🔴 MONTHLY ACTION ITEMS

Based on audits above:

### Immediate Actions (This Week):

1. _____________________________________
2. _____________________________________
3. _____________________________________

### Strategic Actions (This Month):

1. _____________________________________
2. _____________________________________
3. _____________________________________

### Engine Updates Required:

- [ ] Tighten prompts for: __________
- [ ] Replace model for: __________
- [ ] Suspend: __________

### Bible Updates Required:

- [ ] Add framework guidance: __________
- [ ] Update voice rules: __________
- [ ] Add safety rule: __________

---

## 🟢 MONTHLY SIGN-OFF

**System Health Score:** ____ / 100

**Chief Editor Approval:** ___________
**Date:** ___________

**Major Concerns:** _____________________

**Next Month Focus:** _____________________

---

END OF MONTHLY DRIFT CHECK
