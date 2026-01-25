# 🧠 NIVESHAK CONTENT BRAIN

**Version 2.0** | **Status**: Production | **Last Updated**: 25 January 2026

**Institutional Research Operating System — Buy-Side Grade**

---

## 🎯 WHAT THIS IS

This is not a content repository.  
This is not a documentation library.  
This is **a deterministic, audit-safe institutional research operating system** for producing elite equity intelligence.

**Niveshak** is India's most disciplined equity research platform. We publish forensic, regime-aware analysis for serious retail investors, professionals, and institutions who reject hype and demand intellectual rigor.

This repository encodes:
- **16 coordinated AI engines** with complete separation of concerns
- **3 production streams** (Core Content, Real-Time Obs, Strategy Desk)
- **4-layer signal intelligence** feeding all engines
- **Daily/weekly/monthly orchestration** with closed feedback loops
- **Multi-gate quality control** (Cross-Verification + Red Team + Editorial)
- **Complete governance and drift control** preventing system degradation
- **Institutional memory systems** ensuring frameworks compound over time

---

## ⚡ QUICK START

**If you're new to this system, read these files in order:**

### 1. **[`00-bible/niveshak_bible.md`](00-bible/niveshak_bible.md)** — The Constitution
Mission, voice rules, writing bans, edge dimensions, core philosophy

### 2. **[`01-master/master_orchestration.md`](01-master/master_orchestration.md)** — The Orchestration Layer
Daily/weekly/monthly execution logic, signal bindings, feedback loops

### 3. **[`04-operations/daily_checklist.md`](04-operations/daily_checklist.md)** — The Execution Authority
Day-by-day operational guide with exact protocols

**That's it. Those 3 files contain the complete system.**

---

## 🏗️ SYSTEM ARCHITECTURE

### THREE PRODUCTION STREAMS

**STREAM A — CORE CONTENT PIPELINE**
Scheduled institutional blogs (Sunday / Tuesday / Friday)
- Full research pipeline: Signal → Research → Verification → Red Team → Synthesis → Polish → Distribution

**STREAM B — REAL-TIME OBSERVATION**
Market Correspondent (max 3/week, breaking signals only)
- Dual-stage: Grok Pro (X-native) → ChatGPT 5.2 (institutional refinement)
- Insight > Trend supreme rule

**STREAM C — STRATEGY DESK**
Weekly Market Intelligence (independent weekly memo)
- 6-dimension mandatory scan (narratives, sentiment, rotation, earnings, policy, risks)
- Internal memo + public X/Reddit versions

---

## 🔵 SIGNAL LAYER (Foundation)

Located in `/05-signals/` — **Single source of truth**

### 1. `earnings_calendar.md`
Drives Tuesday Audit scheduling, triggers research engines

### 2. `weekly_market_signals.md`
Real-time market memory updated by ENGINE 01, 14, 15

### 3. `regulatory_watch.md`
Legal + governance spine updated by ENGINE 01, 15

### 4. `reader-signals.md`
Crowd-sourced alpha feed updated by ENGINE 14, 15

**All 3 production streams consume these 4 signal files.**

---

## 🤖 THE 16 ENGINES

### CORE PRODUCTION (01-09)

| ID | Engine | Model | Authority |
|----|--------|-------|-----------|
| 01 | **Signal Collector** | Grok + Perplexity | Signal intake authority |
| 02 | **Signal Validator** | Perplexity Pro | Mandatory gate before research |
| 03 | **Gemini Deep Research** | Gemini 2.0 Flash Thinking | Primary research desk |
| 04 | **ChatGPT Deep Research** | ChatGPT 5.2 Deep Research | Context + history desk |
| 05 | **Cross-Verification** | Claude Sonnet 4.5 | **BLOCKING** data quality gate |
| 06 | **Controlled Patch Mode** | Claude Sonnet 4.5 | Surgical repair (no rewrite) |
| 07 | **Red Team** | Claude Sonnet 4.5 | **ABSOLUTE VETO** intellectual gate |
| 08 | **Apex Synthesizer** | Claude Sonnet 3.7 | Chief Strategist / Final Author |
| 09 | **Final Editorial Polish** | Claude Sonnet 4.5 | Publication gate (editing only) |

### DISTRIBUTION (10-13)

| ID | Engine | Platform | Authority |
|----|--------|----------|-----------|
| 10 | **Twitter Adapter** | Claude Sonnet 4.5 | 1-3 Premium tweets, 80% value on X |
| 11 | **LinkedIn Adapter** | Claude Sonnet 4.5 | Single 400-900 word teaching post |
| 12 | **Reddit Adapter** | Claude Sonnet 4.5 | 600-1200 word discussion post |
| 13 | **Visual Intelligence** | Claude Opus 4.5 Thinking | Institutional charts (runs LAST) |

### ENGAGEMENT & INTELLIGENCE (14-16)

| ID | Engine | Model | Authority |
|----|--------|-------|-----------|
| 14 | **Comment & Community Intelligence** | ChatGPT 5.2 | Post-publication engagement |
| 15 | **Market Correspondent** | Grok Pro → ChatGPT 5.2 | Real-time observation (max 3/week) |
| 16 | **Weekly Market Intelligence** | ChatGPT 5.2 | Independent weekly regime pulse |

**Full specifications**: See [`02-engines/`](02-engines/) folder

---

## 🔒 CANONICAL PIPELINE FLOW

```
CORE PRODUCTION:
01 Signal Collector
02 Signal Validator
03 Gemini Deep Research
04 ChatGPT Deep Research
05 Cross-Verification ━━━┓
     ┃                     ┃
     ┃ (APPROVE)      (FAIL)
     ┃                     ┃
     ┃                06 Controlled Patch
     ┃                     ┃ (ALWAYS re-verify)
     ┃ ◄━━━━━━━━━━━━━━━━━━┛
     V
07 Red Team ━━━━━━━━━━━━┓
     ┃                   ┃
     ┃ (APPROVE)    (REJECT)
     ┃                   ┃
     ┃         ┏━━━━━━━━━━━━━━━┓
     ┃         ┃                ┃
     ┃    Data issues?   Structural?
     ┃         ┃                ┃
     ┃    ENGINE 06        ENGINE 08
     ┃         ┃           (rewrite)
     ┃    ENGINE 05 ━┓        ┃
     ┃         ┃      ┃        ┃
     ┃    ENGINE 07 ━┛  ━━━━━━┛
     V
08 Apex Synthesizer
09 Final Editorial Polish
10-12 Platform Adapters
13 Visual Intelligence ← RUNS LAST
→ PUBLISH
14 Comment Engine (ongoing)
```

---

## 📅 ORCHESTRATION CADENCE

### DAILY CONTROL LAYER

**Morning Block (9-10am):**
- ENGINE 01 collects signals
- Updates `weekly_market_signals.md`, `regulatory_watch.md`

**Midday Block (11am-5pm):**
- Check `earnings_calendar.md`
- If match → trigger full pipeline (03→04→05→06→07→08→09→10-13)

**Real-Time Block (ongoing):**
- ENGINE 15 Market Correspondent (conditional, max 3/week)

**End-of-Day (6-6:30pm):**
- Quality sweep (hallucinations, governance errors, reader insights)

### WEEKLY CONTROL LAYER

**Saturday:**
- System 1: Core content close (Sun/Tue/Fri blog logging)
- System 2: MC synthesis (extract regime/governance/flow patterns)
- System 3: ENGINE 16 Weekly Intelligence (independent memo)

**Sunday:**
- Audit 1: Signal quality
- Audit 2: Model health
- Audit 3: Content integrity

### MONTHLY CONTROL LAYER

**First Sunday:**
- Monthly signal audit (4-week review)
- Engine drift audit (all 16 engines)
- Content quality audit (frameworks, kill rate, bias)
- Feedback loop audit (all 4 loops)

---

## 📁 REPOSITORY STRUCTURE

```
Niveshak_Content_Brain/
│
├── 00-bible/                    # Constitutional Foundation
│   ├── niveshak_bible.md        # Mission, voice, edge dimensions
│   ├── frameworks_index.md      # Framework tracking + reinforcement
│   ├── post_index.md            # Complete post log
│   └── killed_ideas.md          # Rejected ideas + lessons
│
├── 01-master/                   # System Architecture
│   ├── niveshak_operating_system_v1.md  # Legacy OS overview
│   └── master_orchestration.md  # ⭐ ORCHESTRATION AUTHORITY
│
├── 02-engines/                  # 16 Engine Specifications
│   ├── engine_01_signal_collector.md
│   ├── engine_02_signal_validator.md
│   ├── engine_03_gemini_deep_research.md
│   ├── engine_04_chatgpt_deep_research.md
│   ├── engine_05_cross_verification.md
│   ├── engine_06_controlled_patch_mode.md
│   ├── engine_07_red_team.md
│   ├── engine_08_apex_synthesizer.md
│   ├── engine_09_writing_polish.md
│   ├── engine_10_platform_adapter_twitter.md
│   ├── engine_11_platform_adapter_linkedin.md
│   ├── engine_12_platform_adapter_reddit.md
│   ├── engine_13_visual_intelligence.md
│   ├── engine_14_comment_engine.md
│   ├── engine_15_market_correspondent.md
│   └── engine_16_weekly_market_intelligence.md
│
├── 04-operations/               # Operational Control
│   ├── daily_checklist.md       # ⭐ DAILY EXECUTION AUTHORITY
│   ├── weekly_checklist.md      # 3-system weekly control
│   ├── monthly_drift_check.md   # System-level integrity audits
│   ├── quality_gate.md          # Pre-publication gates
│   ├── failure_log.md           # Error tracking + learning
│   ├── high_signal_readers.md   # Community intelligence
│   ├── model_health_log.md      # AI performance monitoring
│   ├── market_correspondent_log.md  # MC tracking + synthesis
│   ├── framework_performance.md # Framework win/loss
│   ├── idea_backlog.md          # Content pipeline
│   └── thesis_versions.md       # Intellectual evolution
│
└── 05-signals/                  # ⭐ SIGNAL LAYER (Foundation)
    ├── earnings_calendar.md     # Tuesday Audit scheduler
    ├── weekly_market_signals.md # Real-time market memory
    ├── regulatory_watch.md      # Governance + policy spine
    └── reader-signals.md        # Crowd-sourced alpha
```

---

## 🔐 CORE PRINCIPLES

### 1. Diagnosis > Prediction
- **80%** What happened and why (diagnosis)
- **20%** If X then Y (scenarios)
- **0%** What will happen (predictions)

### 2. Teaching Before Reacting
Frameworks compound over time. We educate, not react.

### 3. Institutional Voice, Zero Hype
Sharp, calm, forensic, anti-fluff. Credibility over clicks.

### 4. Multi-Gate Quality Control
- **ENGINE 05** — Data quality gate (2-source verification)
- **ENGINE 07** — Intellectual quality gate (thesis + voice)
- **ENGINE 09** — Publication gate (editorial polish)

### 5. Governance & Legal Discipline
Question incentives with data, never sensationally. Use "raises questions" not "alleges wrongdoing."

### 6. Separation of Concerns
- **Judge** (05) → **Surgeon** (06) → **Cynic** (07) → **Author** (08) → **Editor** (09)
- No engine performs multiple roles

### 7. Closed Feedback Loops
- LOOP 1: Signal → Content → Reader-Signals
- LOOP 2: Content → Crowd → Signal
- LOOP 3: Real-Time → Strategy (MC → blogs <2 weeks)
- LOOP 4: Quality Control → Engine Tightening

---

## 🛡️ QUALITY SYSTEMS

### Pre-Publication Gates (ALL must pass)

1. **Signature Metric** — One killer number anchors the post
2. **2+ Edge Dimensions** — Novel metric / Regime / Governance / Teaching / Cross-sector / Product
3. **Invalidation Metric** — Specific data point proving analysis wrong
4. **Framework Application** — At least ONE explicitly applied
5. **Voice Check** — Zero banned AI tells
6. **Red Team Approval** — Adversarial challenge passed
7. **Data Verification** — All numbers from 2+ independent sources
8. **Prediction Leakage Scan** — Zero price targets or directional claims
9. **Uncertainty Admission** — Explicit limits stated
10. **"What We're Watching"** — Forward mechanics, not predictions

### Drift Prevention

**Daily:**
- Hallucination check → `model_health_log.md`
- Governance error check → `failure_log.md`

**Weekly:**
- Signal quality audit
- Model health audit
- Content integrity audit

**Monthly:**
- Engine drift audit (all 16 engines)
- Narrative bias check (sector/thesis balance)
- Feedback loop verification

### Failure Recovery

1. **Acknowledge** within 24 hours (public correction)
2. **Investigate** within 48 hours
3. **Correct** within 72 hours
4. **Extract learning** and update engines
5. **Log everything** in `failure_log.md`

---

## 📊 SUCCESS METRICS

### Content Quality
- 90%+ posts hit 2+ Edge dimensions
- 100% analytical posts have invalidation metrics
- Zero banned AI tells in published content
- Zero prediction language

### Cadence Adherence
- 90%+ on-time publications (Sunday/Tuesday/Friday)
- ENGINE 15 Market Correspondent ≤3 posts/week
- ENGINE 16 Weekly Intelligence every Saturday

### Framework Health
- No framework >40% monthly usage (prevents monoculture)
- Framework reinforcement > framework introduction
- Kill rate 10-20% (quality threshold)

### Model Health
- Zero hallucinations passing ENGINE 05
- <2 voice drift incidents per week
- Immediate suspension if prediction language escapes

---

## 🚨 WHAT NIVESHAK NEVER DOES

1. Predict stock prices or returns
2. Promise guaranteed outcomes
3. Hype companies for engagement
4. Copy consensus research
5. Use AI content unedited
6. Ignore governance red flags
7. Sacrifice honesty for clicks
8. Publish without multi-gate validation
9. Soften governance criticism for access
10. Mix analytical roles (judge ≠ surgeon ≠ author)

---

## ✅ WHAT NIVESHAK ALWAYS DOES

1. Teach frameworks that compound
2. Show our work and reasoning
3. Acknowledge what we don't know
4. Update publicly when wrong
5. Question incentives when data warrants
6. Maintain calm institutional voice
7. Reference specific companies and metrics
8. Apply frameworks explicitly
9. Preserve 2-Edge minimum
10. Reinforce frameworks over time

---

## 👥 FOR NEW TEAM MEMBERS

**Day 1:**
- Read `00-bible/niveshak_bible.md`
- Read `01-master/master_orchestration.md`
- Read `04-operations/daily_checklist.md`

**Week 1:**
- Shadow one full week using daily checklist
- Observe all 3 production streams

**Week 2:**
- Produce content under Chief Editor supervision
- All publications require approval

**Week 3:**
- Independent production with spot-checks
- Begin participating in weekly audits

**Month 1:**
- First monthly drift audit participation
- Full system authority granted

**Rule:** If anything is unclear, the documentation is wrong—not you. Update the docs.

---

## 🔄 MAINTENANCE

### Daily
- Update signal files after ENGINE 01
- Log MC posts after ENGINE 15
- Update reader-signals after ENGINE 14

### Weekly
- Log all 3 posts in `post_index.md`
- Update `frameworks_index.md`
- Run 3 mandatory audits (signal/model/content)

### Monthly
- Complete drift audit (all 16 engines)
- Review `failure_log.md` for patterns
- Update engine prompts if systemic issues
- Verify all 4 feedback loops functioning

### Quarterly
- Comprehensive system review
- Model stack reevaluation
- Bible updates (voice/framework evolution)

---

## 🎯 REPOSITORY PHILOSOPHY

This repository is designed so that:

✅ A new operator can run the system without questions  
✅ Quality never degrades over time  
✅ Framework memory compounds  
✅ Institutional voice never drifts  
✅ Every post is auditable  
✅ Every failure becomes a lesson  
✅ Every engine has clear boundaries  
✅ Every decision is traceable  
✅ Models are replaceable without system failure  

**This is a research institution in Git form.**

---

## 📜 VERSION HISTORY

**v2.0** (25 Jan 2026): Orchestration Layer Complete
- 16 engines (up from 12)
- 3 production streams formalized
- 4-layer signal intelligence
- Master orchestration with feedback loops
- Complete daily/weekly/monthly control

**v1.0** (21 Jan 2026): Initial production release
- 12 engines specified
- Basic operational system

---

## 🔒 INSTITUTIONAL MEMORY

This repository contains Niveshak's complete intellectual operating system:

- **16 coordinated AI engines** with complete separation of concerns
- **4 closed feedback loops** preventing drift and compounding intelligence
- **Multi-gate quality control** (Cross-Verification + Red Team + Editorial)
- **Signal layer architecture** feeding all production streams
- **Daily/weekly/monthly orchestration** with deterministic execution
- **Complete governance protocols** preventing legal/reputation risk
- **Framework compounding mechanics** building intellectual moats

**Treat this repository as institutional knowledge—preserve it, update it, never let it drift.**

---

**Built with discipline. Maintained with rigor. Executed with institutional precision.**

**Last Updated:** 25 January 2026  
**Version:** 2.0 (Orchestration Complete)  
**Status:** Production  
**Grade:** Institutional Buy-Side Research OS
