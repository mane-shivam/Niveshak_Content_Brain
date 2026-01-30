# 🧠 NIVESHAK CORE PIPELINE — AUTHORITATIVE FLOW & AUTHORITY DIAGRAM

**Version:** 2.3 (Insight-Protected Architecture)
**Date:** 25 January 2026
**Status:** Production Canonical

This document defines the **complete routing, authority chain, loop rules, and quality governance** for the Niveshak Content Brain.

---

## 🔵 PLANNING LAYER (UPSTREAM OF PRODUCTION)

```
ENGINE 19 — MONTHLY ARC PLANNER (Season Theme)
        ↓
ENGINE 18 — WEEKLY ARC PLANNER (Episode Design) [CAN OVERRIDE 19]
        ↓
ENGINE 17 — TUESDAY STOCK AUDIT GENERATOR (Pick Selection)
        ↓
ENGINE 05 — CROSS VERIFICATION (Stock Pick Validation)
        ↓
        → FEEDS INTO PRODUCTION PIPELINE
```

**Planning Layer Rules:**
- ENGINE 19 runs monthly → sets season curriculum
- ENGINE 18 runs weekly → designs Sun/Tue/Fri episodes
- ENGINE 18 may override 19 for urgent topics (max 2/month)
- ENGINE 17 generates Tuesday stock picks from weekly brief
- ENGINE 17 picks MUST pass ENGINE 05 before production

---

## 🔴 CANONICAL PIPELINE FLOW

```
ENGINE 01 — SIGNAL COLLECTOR
        ↓
ENGINE 02 — SIGNAL VALIDATOR
        ↓
ENGINE 03 — GEMINI DEEP RESEARCH
        ↓
ENGINE 04 — CHATGPT DEEP RESEARCH
        ↓
🔴 ENGINE 04A — DRAFT GENERATOR (MULTI-EXAMPLE MODE)
        ↓
🔴 ENGINE 04B — INSIGHT DISTILLER (LOCK THESIS + INSIGHTS)
        ↓
ENGINE 05 — CROSS VERIFICATION (JUDGE)
        ↓
    ┌──────────── FAIL ─────────────┐
    ↓                                │
ENGINE 06 — CONTROLLED PATCH MODE    │
    ↓                                │
ENGINE 05 — RE-VERIFY ───────────────┘
        ↓
ENGINE 07 — RED TEAM (CYNIC / SHORT SELLER)
        ↓
    ┌────────── REWRITE ──────────┐
    ↓                              │
ENGINE 06 — PATCH (RED TEAM FIX)   │
    ↓                              │
ENGINE 05 — RE-VERIFY ─────────────┘
        ↓
🔴 ENGINE 08 — APEX SYNTHESIZER (FINAL AUTHOR)
        ↓
★ ENGINE 13.A CHECKPOINT 1 (POST-APEX INTEGRITY) ★
        ↓
🔴 ENGINE 09 — FINAL WRITING POLISH
        ↓
ENGINE 10 / 11 / 12 — PLATFORM ADAPTORS
        ↓
ENGINE 13 — VISUAL INTELLIGENCE
        ↓
★ ENGINE 13.A CHECKPOINT 2 (PRE-PUBLISH) ★ — MANDATORY
        ↓
PUBLISH
        ↓
ENGINE 14 — COMMENT ENGINE
        ↓
★ ENGINE 13.A CHECKPOINT 3 (48HR POST-PUBLISH) ★
        ↓
INTELLIGENCE → ENGINE 01 (LOOP)
```

---

## 🔒 AUTHORITY CHAIN (PREVENTS DRIFT & CHAOS)

### 🔹 ENGINE 04A — DRAFT GENERATOR

**Authority:** LOW

**Can:**
- Generate thesis proposals
- Generate insights
- Build 5-example pools per insight

**Cannot:**
- Lock anything
- Finalize claims
- Skip multi-example pools

**Status:** Can be overwritten freely

---

### 🔹 ENGINE 04B — INSIGHT DISTILLER

**Authority:** VERY HIGH (CONSTITUTIONAL)

**Locks permanently:**
- Thesis
- 3-5 core insights
- Killer metric
- Falsification logic

**Creates files:**
- `protected_insights.md` (SACRED)
- `example_selection.md` (control sheet)
- `draft_v1_curated.md

`

**After this stage:**
❌ No engine may delete insights
❌ No engine may rewrite thesis

**This is your INTELLECTUAL CORE LAYER.**

---

### 🔹 ENGINE 05 — CROSS VERIFICATION

**Authority:** HIGH but LIMITED (Judge not Author)

**Can:**
- Kill examples
- Kill numbers
- Kill hallucinated data
- Verify Tier 1 facts
- Delete Tier 3 speculation

**Cannot:**
- Touch thesis
- Touch insights (Tier 2)
- Touch frameworks
- Touch narrative

**Routing:**
- On FAIL → ONLY to ENGINE 06
- On PASS → ONLY to ENGINE 07
- Never to Apex directly

**Creates files:**
- `verification_report.md`
- `defect_list.md`

---

### 🔹 ENGINE 06 — CONTROLLED PATCH MODE

**Authority:** SURGICAL ONLY (Surgeon not Author)

**Can:**
- Replace examples with Tier-2 backups
- Replace numbers
- Fix sourcing

**Cannot:**
- Rewrite logic
- Change insights
- Simplify frameworks
- Alter story

**Routing:**
- Always routes back to ENGINE 05 for re-verification

**Creates files:**
- `patch_log.md`
- Updated `example_selection.md`
- `draft_v2_patched.md`

---

### 🔹 ENGINE 07 — RED TEAM

**Authority:** VERY HIGH (VETO POWER)

**Can:**
- Kill draft
- Force rewrite
- Force thesis revision
- Veto publication

**Cannot:**
- Patch
- Verify
- Rewrite directly

**Routing:**
- On REWRITE / KILL → ENGINE 06
- On PASS → ENGINE 08

**Red Team veto CANNOT be bypassed.**

---

### 🔹 ENGINE 08 — APEX SYNTHESIZER

**Authority:** FINAL AUTHOR (Narrative omnipotence, ZERO data authority)

**Core Mode:** WRITE FROM SCRATCH (not merge, not patch)

**Can:**
- Write a brand new post from scratch
- Ignore all existing structure
- Merge best insights, analogies, mechanisms from all drafts
- Architect final narrative and teaching arc
- Select best examples from verified pool

**Cannot:**
- Invent data
- Change thesis (wording must be identical)
- Change protected insights
- Change killer metric
- Remove falsification logic
- Fix verification issues

**🔴 INPUT SANITATION RULE (CRITICAL):**

Must receive ONLY clean inputs:
- `protected_insights.md` (from ENGINE 04B)
- Final Verified Draft (from ENGINE 05)
- Red Team PASS verdict (summary only, NO commentary)
- Clean alternative drafts (Gemini, ChatGPT, Patch)
- `niveshak_bible.md`

Must NOT receive:
- Red Team commentary blocks
- Patch notes
- Instructional notes
- Meta-analysis
- Internal flags

**If meta or scaffolding text present → ABORT RUN**

**Voice Target:** Bloomberg Intelligence primary, Business Standard clarity, Groww smoothness. Personality: 7/10.

**Creates files:**
- `master_draft_vfinal.md`
- Internal Synthesis Note (NOT published)

---

### 🔹 ENGINE 09 — FINAL POLISH

**Authority:** LOWEST (Polish only)

**Can only:**
- Improve flow
- Improve readability
- Improve rhythm
- Fix transitions

**Cannot change:**
- Anything substantive
- Any claims
- Any data
- Any insights

**Creates files:**
- `final_publish_draft.md`

---

## 🔄 CRITICAL LOOP RULES (ANTI-VALUE DESTRUCTION)

### 🔹 MULTI-EXAMPLE SAFETY LOOP

**Because of ENGINE 04A + 04B:**

Each insight always has:
- 2 Tier-1 examples
- 1-2 Tier-2 backups

**When verification kills one example:**

```
ENGINE 05 → ENGINE 06 → swap example → ENGINE 05
```

**Thesis and insight NEVER touched.**

---

### 🔹 RED TEAM LOOP

**When Red Team rejects:**

```
ENGINE 07 FAIL
      ↓
ENGINE 06 PATCH
      ↓
ENGINE 05 REVERIFY
      ↓
ENGINE 07 AGAIN
```

**No draft reaches Apex unless:**
- Verified
- Patched
- Red-Team approved

---

### 🔹 VERIFICATION-PATCH LOOP

**When verification finds errors:**

```
ENGINE 05 FAIL
      ↓
ENGINE 06 PATCH (replace examples/numbers)
      ↓
ENGINE 05 RE-VERIFY
      ↓
(If PASS) → ENGINE 07
(If FAIL again) → ENGINE 06 (new examples)
```

**Max iterations:** 3
**After 3 failures:** Route to human review

---

## 📋 FILE HANDOFF MAP

### ENGINE 04A → 04B:
- `draft_v0_placeholder.md`
- `engine 04A output `
- `engine 04A output `

### ENGINE 04B → 05:
- `protected_insights.md` ⭐ CONSTITUTIONAL
- `example_selection.md` ⭐ CONTROL SHEET
- `draft_v1_curated.md`

### ENGINE 05 → 06:
- `verification_report.md`
- `defect_list.md`

### ENGINE 06 → 05:
- `draft_v2_patched.md`
- Updated `example_selection.md`
- `patch_log.md`

### ENGINE 07 → 08:
- Red Team PASS verdict
- All verified materials

### ENGINE 08 → 09:
- `master_draft_vfinal.md`
- Internal Synthesis Note (not published)

### ENGINE 09 → 10-12:
- `final_publish_draft.md`

---

## 🔴 DRIFT / QUALITY GOVERNANCE

### 🔹 WEEKLY QUALITY CHECK (MANDATORY)

**Add to `weekly_checklist.md`:**

```markdown
## WEEKLY PIPELINE HEALTH CHECK

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
```

---

### 🔹 MONTHLY SYSTEM AUDIT

**Add to `monthly_drift_check.md`:**

```markdown
## MONTHLY ENGINE AUDIT

### ENGINE 04A — Draft Generator
- [ ] % examples rejected by verification: ____
- [ ] Hallucination rate: ____
- [ ] Target: <20% example rejection, 0% hallucination

### ENGINE 04B — Insight Distiller
- [ ] Are insights surviving verification? ____%
- [ ] Any forced thesis rewrites? ____
- [ ] Target: >80% insight survival, 0 thesis rewrites

### ENGINE 06 — Controlled Patch
- [ ] Patch success rate: ____%
- [ ] Avg number of example swaps per post: ____
- [ ] Target: >90% patch success, <3 swaps per post

### ENGINE 07 — Red Team
- [ ] Kill rate: ____%
- [ ] Common logic failures: ____
- [ ] Target: 10-25% veto rate (not >80% or <5%)

### ENGINE 08 — Apex Synthesizer
- [ ] Reader engagement vs depth balance: ____
- [ ] Narrative quality score (manual): ____
- [ ] Protected insight preservation: ____%
- [ ] Target: 100% insight preservation

### ENGINE 09 — Final Polish
- [ ] Any meaning drift detected? ____
- [ ] Voice quality consistent? ____
- [ ] Target: 0 claim changes, consistent 7/10 personality

## SYSTEM KPIs

- [ ] Insight survival rate: ____% (target: >80%)
- [ ] Red Team veto rate: ____% (target: 10-25%)
- [ ] Reader "framework reuse" signals: ____
- [ ] Hallucination incidents: ____ (target: 0)
- [ ] Thesis drift incidents: ____ (target: 0)
```

---

## 🟢 WHAT THIS ARCHITECTURE GUARANTEES

With this complete system:

✅ **Protected insight layer** (04B constitutional authority)
✅ **Multi-example safety net** (04A + 04B redundancy)
✅ **Verification that cannot kill thesis** (judge not author)
✅ **Patch engine that preserves essence** (surgeon not rewriter)
✅ **Apex that becomes real editor + storyteller** (write-from-scratch synthesis)
✅ **Single final polish layer** (ENGINE 09, story-preserving)
✅ **Clean authority and routing** (no ambiguity)
✅ **Drift prevention** (weekly + monthly governance)

---

## 🎯 SYSTEM GRADE

**This is now:**

- Hedge-fund-grade research pipeline
- Editorial-grade storytelling system
- Automation-safe architecture
- Bloomberg × Business Standard × Groww voice (personality 7/10)
- FT Alphaville / Odd Lots operational standard

---

**Last Updated:** 25 January 2026
**Version:** 2.3 (Complete Authority Chain)
**Status:** Production Canonical

END OF PIPELINE MAP
