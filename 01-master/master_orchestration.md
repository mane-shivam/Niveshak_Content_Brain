# Niveshak Content Brain — Master Orchestration v2.3

**Version**: 2.3 FINAL
**Last Updated**: 25 January 2026
**Status**: Production-Ready Institutional Research OS

---

## System Philosophy

This system produces **institutional-grade equity research** with:
- Bloomberg-level factual rigor
- Michael Lewis-level narrative readability
- Hedge fund-level governance thinking
- Complete insight protection from verification pressure

**Core Doctrine**: Insight is sacred. Structure, examples, and data serve insight — never the reverse.

---

## Complete Production Pipeline

```
ENGINE 01-02: Signal Collection & Validation
    ↓
ENGINE 03: Primary Research Desk (Gemini)
    → Forensic fact extraction
    → 5 hallucination control rules
    → 3 input modes (Company/Event/Macro)
    → Output: research_pack_engine03.md
    ↓
ENGINE 04: ChatGPT Deep Research Desk
    → Mechanism mapping
    → Multi-example pools (5-8 per branch)
    → Insight candidates (5-8)
    → Output: insight_pack_engine04.md
    ↓
ENGINE 04.1: Draft Generator (Placeholder Mode)
    → 5 examples per insight
    → Anti-hallucination rules
    → Placeholder narrative
    → Output: draft_v0_placeholder.md, example_pool.md
    ↓
ENGINE 05A: Insight Distiller ⭐ CONSTITUTIONAL AUTHORITY
    → Locks thesis + 3-5 insights + killer metric
    → Creates protected_insights.md (SACRED)
    → Tier 1/2/3 classification
    → Output: protected_insights.md
    ↓
ENGINE 05: Cross-Verification (Judge Mode)
    → Verifies Tier 1 facts only
    → CANNOT touch Tier 2 reasoning (protected)
    → Output: verification_report.md, defect_list.md
    → If FAIL → ENGINE 06
    → If PASS → ENGINE 07
    ↓
ENGINE 06: Controlled Patch (Surgeon Mode)
    → Replaces failed examples from Tier-2 pool
    → CANNOT change thesis/insights
    → Output: patched_draft.md, patch_log.md
    → Always routes back to ENGINE 05 for re-verification
    ↓
[LOOP until verification PASS]
    ↓
ENGINE 07: Red Team
    → Hostile short-seller mode
    → Veto power (can kill draft)
    → Cannot directly edit
    → Routes fixes through ENGINE 06
    → Output: red_team_verdict.md
    ↓
ENGINE 08: Apex Synthesizer (Final Author)
    → Multi-draft synthesis
    → Story-building + teaching arc
    → Zero data authority
    → Must preserve protected insights
    → Output: master_draft_vfinal.md
    ↓
ENGINE 09: Writing Polish (Final Gate)
    → Bloomberg + Michael Lewis voice
    → Rhythm, flow, transitions only
    → CANNOT change claims/data/insights
    → Output: final_publish_draft.md
    ↓
ENGINE 10-12: Platform Adapters (Twitter/LinkedIn/Reddit)
    ↓
ENGINE 13: Visual Intelligence
    ↓
ENGINE 14: Comment Engine
```

---

## Authority Hierarchy (Non-Negotiable)

**CONSTITUTIONAL (Highest):**
- ENGINE 05A — Locks insights before verification

**JUDICIAL:**
- ENGINE 05 — Verifies facts, cannot delete insights

**SURGICAL:**
- ENGINE 06 — Repairs examples, preserves insights

**VETO:**
- ENGINE 07 — Can kill draft, cannot rewrite

**AUTHORIAL:**
- ENGINE 08 — Controls narrative, zero data authority

**POLISH:**
- ENGINE 09 — Lowest authority, language only

**Critical Rule**: No downstream engine may contradict protected_insights.md without human override.

---

## Critical Mechanisms

### 1. Multi-Example Safety Net
- ENGINE 03-04: Build 3-8 examples per thesis branch
- ENGINE 04.1: Generate 5 examples per insight
- ENGINE 05A: Select Tier-1 (2) + Tier-2 backups (1-2)
- ENGINE 05: Can delete 3 examples without thesis collapse
- ENGINE 06: Swaps from Tier-2 pool

### 2. Protected Insight Layer (3 Defenses)
- ENGINE 05A locks insights BEFORE verification
- ENGINE 05 cannot delete Tier 2 reasoning
- ENGINE 06 must preserve insights while patching

### 3. Hallucination Prevention (Source Control)
- ENGINE 03 banned from inventing periods
- ENGINE 04.1 uses placeholder mode
- Source status tracking throughout
- Tier 1 facts require verification

---

## Key File Handoffs

| From | To | Critical Files |
|------|----|----|
| ENGINE 03 | ENGINE 04 | research_pack_engine03.md |
| ENGINE 04 | ENGINE 04.1 | insight_pack_engine04.md |
| ENGINE 04.1 | ENGINE 05A | draft_v0_placeholder.md, example_pool.md |
| ENGINE 05A | ENGINE 05 | **protected_insights.md** ⭐ |
| ENGINE 05 | ENGINE 06 | verification_report.md, defect_list.md |
| ENGINE 06 | ENGINE 05 | patched_draft.md (re-verify) |
| ENGINE 07 | ENGINE 08 | red_team_verdict.md |
| ENGINE 08 | ENGINE 09 | master_draft_vfinal.md |

**Sacred File**: `protected_insights.md` — Created by ENGINE 05A, obeyed by all downstream engines.

---

## Routing Rules

### Standard Flow:
03 → 04 → 04.1 → 05A → 05 → 07 → 08 → 09 → Platforms

### Verification Loop:
05 (FAIL) → 06 → 05 (re-verify) → [loop until PASS]

### Red Team Loop:
07 (concerns) → 06 (fix) → 05 (verify fix) → 07 (re-check)

### Never Allowed:
- 04.1 → 05 (must go through 05A first)
- 08 → 05 (Apex cannot fix verification issues)
- 09 → data changes (Polish is language only)

---

## Weekly Production Cycle

**Sunday Brief**: Macro/sector framework (mandatory structure)
**Tuesday Audit**: Company/governance deep dive (optional structure)
**Friday**: Market Correspondent micro-intelligence

**Process for each post:**
1. Signal validation (ENGINE 01-02)
2. Deep research (ENGINE 03-04)
3. Draft generation (ENGINE 04.1)
4. Insight lock (ENGINE 05A)
5. Verification + patch loop (ENGINE 05-06)
6. Red Team approval (ENGINE 07)
7. Narrative synthesis (ENGINE 08)
8. Final polish (ENGINE 09)
9. Platform distribution (ENGINE 10-14)

---

## Monthly Governance

**Track in `model_health_log.md`:**
- Hallucination incidents (target: 0)
- Thesis survival rate after verification
- Example pool survival rate
- Insight density scores
- Voice drift indicators
- Framework performance
- Red Team veto rate

**Suspend engine if:**
- Hallucination twice (ENGINE 03)
- Thesis collapse twice (ENGINE 04.1/05A)
- Insight deletion (ENGINE 05)
- Data changes (ENGINE 09)

---

## Integration Points

**Daily Checklist**: `04-operations/daily_checklist.md`
- Signal discipline
- Market Correspondent cap (300 words)
- Insight protection verification

**Weekly Checklist**: `04-operations/weekly_checklist.md`
- Insight survival scoring
- Framework performance
- Voice audit

**Monthly Drift Check**: `04-operations/monthly_drift_check.md`
- Hallucination audit
- Insight destruction check
- Voice + readability scoring
- Framework retirement triggers

---

## Core Reference Documents

**Constitutional:**
- `00-bible/niveshak_bible.md` — Philosophical charter (v2.0)
- `01-master/master_orchestration.md` — This file (system architecture)
- `01-master/final_system_verification.md` — Completion audit

**Operational:**
- `04-operations/pipeline_map.md` — Visual routing diagram
- `04-operations/model_health_log.md` — Engine performance tracking

**Engines** (all in `02-engines/`):
- engine_03_gemini_deep_research.md
- engine_04_chatgpt_deep_research.md
- engine_04.1_draft_generator.md
- engine_05A_insight_distiller.md
- engine_05_cross_verification.md
- engine_06_controlled_patch_mode.md
- engine_07_red_team.md
- engine_08_apex_synthesizer.md
- engine_09_writing_polish.md
- engine_10-14 (platform/distribution)

---

## System Grade

**Operational Standard**: Hedge fund research desk / Bloomberg intelligence level

**Voice Achievement**: Bloomberg clarity + Michael Lewis narrative + Institutional forensic

**Hallucination Risk**: ELIMINATED AT SOURCE (ENGINE 03 controls)

**Insight Protection**: 3-layer constitutional defense

**Status**: Production-ready institutional research OS

---

## What This System Guarantees

1. **Insight cannot be destroyed** — ENGINE 05A locks before verification runs
2. **Thesis cannot collapse** — Multi-example pools provide redundancy
3. **Hallucination eliminated** — ENGINE 03 bans recent data invention
4. **Authority is clean** — Each engine knows its limits
5. **Story capability enabled** — ENGINE 08 builds narrative while preserving rigor
6. **Voice is readable** — ENGINE 09 polishes to 7/10 personality
7. **Drift is monitored** — Weekly/monthly governance catches regression

---

**Last Updated**: 25 January 2026
**Canonical Version**: v2.3 FINAL
**Next Review**: Monthly drift check cycle
