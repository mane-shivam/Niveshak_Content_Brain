# NIVESHAK DAILY CHECKLIST

**Reference:** `01-master/master_orchestration.md`
**Version:** 2.0 (Orchestration-Integrated)

---

## 🔵 MORNING BLOCK — SIGNAL INTAKE

**Time:** 9:00 AM - 10:00 AM (Every Working Day)
**Mandatory:** Yes

### ENGINE 01 — SIGNAL COLLECTOR

**Run Daily:**

- [ ] Scan BSE/NSE filings (yesterday + overnight)
- [ ] Scan SEBI circulars and regulatory updates
- [ ] Scan X (Twitter) for structural signals
- [ ] Scan business news (ET, Mint, BL) for non-noise
- [ ] Scan earnings calendar for upcoming releases

**Update Files:**

- [ ] Append structural signals to `05-signals/weekly_market_signals.md`
- [ ] Append governance/policy to `05-signals/regulatory_watch.md`
- [ ] Update `05-signals/earnings_calendar.md` if new earnings announced

**Quality Check:**

- [ ] All signals structural (not daily noise)
- [ ] All signals sourced (filing/disclosure/official)
- [ ] No predictions or hype language

---

## 🔵 MIDDAY BLOCK — RESEARCH TRIGGERS

**Time:** 11:00 AM - 5:00 PM (Conditional)
**Trigger:** Earnings match in `earnings_calendar.md` OR scheduled post day

### If Today = Tuesday (Earnings Audit)

**Stock Selection (from Planning Layer):**

- [ ] **ENGINE 17** — Verify Tuesday stock pick from `stock_picks_verified_ENGINE17.md`
  - [ ] Pick was generated from weekly brief (ENGINE 18)
  - [ ] Pick was verified by ENGINE 05
  - [ ] If pick failed verification → use BACKUP from ENGINE 17 pool

**Run Full Pipeline:**

- [ ] **ENGINE 03** — Gemini Deep Research (attach Bible + earnings calendar)
- [ ] **ENGINE 04** — ChatGPT Deep Research (attach Bible + signals)
- [ ] **ENGINE 05** — Cross-Verification (attach both packs)
  - [ ] If FAIL → **ENGINE 06** Controlled Patch → Re-verify with 05
  - [ ] Loop until PASS
- [ ] **ENGINE 07** — Red Team (attach verified pack)
  - [ ] If REJECT (data) → **ENGINE 06** → **ENGINE 05** → **ENGINE 07**
  - [ ] If REJECT (structural) → **ENGINE 08** rewrite → **ENGINE 07**
  - [ ] Loop until APPROVE
- [ ] **ENGINE 08** — Apex Synthesizer (attach ONLY: protected_insights.md, verified draft, Red Team PASS summary, clean drafts, Bible — NO meta, NO commentary)
- [ ] **ENGINE 09** — Final Editorial Polish
- [ ] **ENGINE 10** — Platform Adapter: Twitter
- [ ] **ENGINE 11** — Platform Adapter: LinkedIn
- [ ] **ENGINE 12** — Platform Adapter: Reddit
- [ ] **ENGINE 13** — Visual Intelligence (attach ALL platform versions)

**Log Everything:**

- [ ] Update `04-operations/weekly_execution_log_template.md`
- [ ] If any failures → log in `failure_log.md`
- [ ] If Red Team kills → log in `killed_ideas.md`

### If Today = Sunday or Friday (Macro/Brief)

**Same pipeline as Tuesday, but:**

- [ ] Sunday: Signal-driven topic from `weekly_market_signals.md`
- [ ] Friday: Macro regime topic from `regulatory_watch.md` + signals

---

## 🔵 REAL-TIME BLOCK — MARKET CORRESPONDENT (CONDITIONAL)

**Time:** Ongoing (as events break)
**Trigger:** Breaking event + Insight > Trend test

### Before Posting:

- [ ] **Energy Governor Check:**
  - [ ] Am I reacting emotionally? (If YES → STOP)
  - [ ] Am I tired or rushing? (If YES → STOP)
  - [ ] Am I posting to feel relevant? (If YES → STOP)

- [ ] **Insight > Trend Test:**
  - [ ] Do I add structural angle others miss? (If NO → STOP)
  - [ ] Does this change how readers interpret the event? (If NO → STOP)

- [ ] **Frequency Check:**
  - [ ] Have I posted 3 times this week already? (If YES → STOP)

### If All Checks Pass:

- [ ] **Stage 1:** Run Grok Pro (X-native sentiment capture)
- [ ] **Stage 2:** Run ChatGPT 5.2 (institutional refinement)
- [ ] **Verification Gate:**
  - [ ] Event confirmed via primary source
  - [ ] Company/quarter/numbers verified
  - [ ] Regulatory wording checked
- [ ] **Legal Safety Check:**
  - [ ] No intent language
  - [ ] Governance claims cite filings
  - [ ] Use "raises questions" not "wrongdoing"

### After Posting (ENGINE 15):

- [ ] Update `market_correspondent_log.md`
- [ ] Append to `05-signals/weekly_market_signals.md`
- [ ] If reactions seen → append to `05-signals/reader-signals.md`

---

## 🔵 POST-PUBLICATION BLOCK — COMMENT ENGINE

**Time:** Ongoing after any publication
**Priority:** First 24-48 hours

### ENGINE 14 — COMMENT & COMMUNITY INTELLIGENCE

**For Each Platform:**

Twitter:
- [ ] Monitor replies (short, precise responses)
- [ ] Max 2 replies deep per thread
- [ ] Flag high-signal readers

LinkedIn:
- [ ] Monitor comments (teaching tone, warmer)
- [ ] Extra caution on governance accusations
- [ ] Flag Tier-1 commenters

Reddit:
- [ ] Monitor threads (peer-to-peer tone)
- [ ] Strong uncertainty admissions
- [ ] Never assert authority

**Categorize Each Comment:**

- [ ] Praise → Brief acknowledgment
- [ ] Criticism → Thank, acknowledge, cite filings if governance
- [ ] Question → Direct answer with teaching
- [ ] Discussion → Deep engagement, flag Tier-1
- [ ] Troll → Ignore or one polite redirect
- [ ] **ERROR** → 24hr public reply, verify, correct, log

**Update Files:**

- [ ] If Tier-1 reader → log in `04-operations/high_signal_readers.md`
- [ ] If error found → log in `failure_log.md` + notify Chief Editor
- [ ] If insight surfaces → log in `05-signals/reader-signals.md`

---

## 🔵 END-OF-DAY QUALITY SWEEP

**Time:** 6:00 PM - 6:30 PM
**Mandatory:** Yes

### Quality Checks:

- [ ] Any hallucination today? → Log in `model_health_log.md`
- [ ] Any governance errors flagged? → Log in `failure_log.md`
- [ ] Any high-signal reader insight? → Update `reader-signals.md`
- [ ] Any prediction language slipped through? → Escalate immediately

**INSIGHT PRESERVATION CHECK:**
- [ ] Did any protected insight get deleted during verification?
- [ ] Did thesis drift after patch?
- [ ] Did patch preserve meaning and examples?
- [ ] If YES to any → FLAG SYSTEM DRIFT in `model_health_log.md`

**PIPELINE HEALTH CHECK:**
- [ ] Any insight deleted by verification this week?  
      → If yes, log in `insight_loss_log.md`  
- [ ] Any post rewritten around surviving data instead of original thesis?  
      → If yes, FLAG STRUCTURE TYRANNY  
- [ ] Any Apex draft rejected by Red Team?  
      → Track in `red_team_kill_log.md`  
- [ ] Any hallucinated data caught after Engine 05?  
      → Log in `model_health_log.md`  
- [ ] Did at least one post introduce a reusable framework or metric?
- [ ] Example survival rate this week: ____%
      → Target: >60% of Tier-1 examples survive verification

### Daily Close:

- [ ] Review `run_trace` for today
- [ ] Flag any engine showing drift signs
- [ ] Prepare tomorrow's priorities

---

## 🔴 EMERGENCY PROTOCOLS

### If Wrong Data Published:

1. **Immediate** public correction on all platforms (<24hr)
2. Log in `failure_log.md`
3. Notify Chief Editor
4. Review which engine failed
5. Suspend engine if systemic

### If Prediction Language Published:

1. Identify which engine allowed it
2. Log in `model_health_log.md`
3. Tighten prompts immediately
4. Consider suspension if repeat

### If Legal/Defamation Risk:

1. Consult legal immediately
2. Do NOT delete (creates Streisand effect)
3. Issue clarification if needed
4. Log in `failure_log.md`
5. Review governance safety rules

---

END OF DAILY CHECKLIST
