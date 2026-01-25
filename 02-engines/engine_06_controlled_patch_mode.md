# 🔴 ENGINE 06 — CONTROLLED PATCH MODE (UPDATED, SURGEON MODE)

**Position**: After Cross Verification / Red Team
**Role**: Surgical Repair Engine
**Authority**: SUBORDINATE to ENGINE 05A + ENGINE 05

---

## ENGINE NAME

**ENGINE 06 — CONTROLLED PATCH MODE**

---

## MODEL

**ONLY ALLOWED MODEL**: Claude Sonnet 4.5
**Temperature**: 0.2
**Context**: Full

---

## THREAD LINK PLACEHOLDER

```
THREAD: [insert link here]
POST ID: [unique id]
RUN ID: [timestamp]
```

---

## 🎯 PURPOSE

This engine fixes **only what verification or Red Team flagged**
while preserving:

* Thesis
* Core insights
* Framework logic
* Narrative spine

This engine is a **surgeon, not an author**.

---

## ⛔ ABSOLUTE AUTHORITY RULE

This engine MUST obey:

* ENGINE 05A — Protected Insight Lock
* ENGINE 05 — Verification Report

It may:

* Replace wrong data
* Find better examples
* Update sources
* Repair broken analogies

It may NOT:

* Change thesis
* Remove protected insights
* Simplify frameworks away
* Rewrite narrative structure

---

## 🔴 PROTECTED INSIGHT RULE (CRITICAL)

This engine's job is NOT to kill or drift the thesis.

If verification flags an issue:

- **NEVER delete core thesis**
- **NEVER delete protected insights**
- **NEVER weaken the framework**

Instead:
- Replace examples with new sourced analogies
- Replace data points with verified alternatives
- Find new analogies that support the same insight
- Rewrite flow to preserve meaning

**This engine is the sole authority responsible for:**
Preserving insight while restoring factual correctness.

---

## 🔵 WHEN TO RUN

Run ONLY when:

* ENGINE 05 flags errors
  OR
* ENGINE 07 (Red Team) demands rewrite

After patch:

→ **ALWAYS route BACK to ENGINE 05 for re-verification**

---

## 📂 FILES TO ATTACH (MANDATORY)

1. **Protected Insight Lock (Engine 05A)** ← CONSTITUTIONAL
2. Cross Verification Report (Engine 05) OR Red Team Report (Engine 07)
3. Current Draft
4. `00-bible/niveshak_bible.md`

---

## 🧠 PATCH PROMPT (THREAD STARTER)

```
You are Niveshak's CONTROLLED PATCH ENGINE.

ATTACHED:
- Protected Insight Lock (CONSTITUTIONAL)
- Cross Verification / Red Team Report
- Current Draft
- niveshak_bible.md

MISSION:

Repair errors WITHOUT damaging insight.

RULES:

- Thesis and Tier 2 insights are LOCKED  
- Only fix what is explicitly flagged  
- Replace examples if they no longer match insight  
- Rebuild flow ONLY if example replacement breaks coherence  

WHAT TO DO:

STEP 1 — FIX TIER 1 ERRORS  
- Correct numbers  
- Fix quarters  
- Replace wrong filings  
- Add proper sources  

STEP 2 — DELETE TIER 3  
Remove all speculation flagged.

STEP 3 — REPAIR EXAMPLES  
If an example was killed:
- Find a NEW example that:
  - Matches the same insight  
  - Is current regime relevant  
  - Is fully sourceable  
  - Supports the locked thesis

STEP 4 — FLOW REPAIR  
If patch broke coherence:
- Repair transitions  
- Re-anchor to killer metric  
- Preserve narrative spine  
- Maintain teaching arc

STEP 5 — COHERENCE CHECK
Verify:
- Thesis unchanged
- Protected insights intact
- Framework logic preserved
- Flow still works

IMPORTANT:

- Do NOT weaken insight  
- Do NOT simplify logic  
- Do NOT rewrite whole draft  
- Do NOT add new claims

OUTPUT:

Patched Draft  
+ Patch Log (what changed and why)

After patch → Route BACK to ENGINE 05 for re-verification.
```

---

## 🔁 RESTART PROMPT (WHEN ITERATING)

```
You are continuing as Niveshak's CONTROLLED PATCH ENGINE.

PREVIOUS PATCH LOG:
[Paste previous patch log]

NEW FEEDBACK:
- Additional verification issues OR
- Red Team concerns

TASK:

- Apply additional surgical repairs
- Preserve previous successful patches
- Maintain protected insights

OUTPUT:
Updated patched draft
+ Cumulative patch log
```

---

## 🧾 OUTPUT FORMAT (NON-NEGOTIABLE)

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
CONTROLLED PATCH REPORT — ENGINE 06
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

POST ID:
DATE:
PATCH RUN:

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
REPAIRS EXECUTED
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Tier 1 Fixes:
- Issue: [what was wrong]
  Fix: [what was changed]
  New source: [if applicable]

Tier 3 Deletions:
- Removed: [speculation text]
  Reason: [why it was speculation]

Example Replacements:
- Old example: [brief description]
  Why replaced: [verification issue]
  New example: [replacement]
  Insight preserved: [YES/NO + explanation]

Flow Repairs:
- Section: [where]
  Issue: [what broke]
  Fix: [how repaired]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
PROTECTED INSIGHT VERIFICATION
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Thesis: [UNCHANGED / CHANGED - explain if changed]
Core Insights: [INTACT / MODIFIED - explain]
Killer Metric: [PRESERVED / ALTERED - explain]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
ROUTING INSTRUCTION
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

→ Route to ENGINE 05 for re-verification

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
PATCHED DRAFT ATTACHED
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

[Full patched draft below]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
END OF PATCH REPORT
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## 🔵 NEXT STEPS (AUTOMATIC ROUTING)

After patch completes:

### Always:

```
ENGINE 06 → ENGINE 05 (Re-verify patched draft)
```

Never skip re-verification.

---

## 📒 LOGS TO MAINTAIN

Mandatory:

* `run_trace`

Optional:

* `thesis_versions.md` (if thesis accidentally changed)
* `model_health_log.md` (if patch quality issues)

---

## 🗓️ WEEKLY CHECKLIST INTEGRATION

### When this engine runs

* After ENGINE 05 flags errors
* OR after ENGINE 07 requests rewrite

---

### Weekly Execution Steps

1. Receive Protected Insight Lock
2. Receive Verification/Red Team Report
3. Execute surgical repairs only
4. Verify protected insights intact
5. Route to ENGINE 05 for re-verification

---

### Weekly Quality Gate

Before marking DONE:

* All flagged issues addressed
* Protected insights verified intact
* No unauthorized edits
* Thesis unchanged
* Flow coherent

---

## 🗓️ MONTHLY CHECKLIST INTEGRATION

### Monthly Review Questions

* Is patch preserving insights?
* Are examples improving or degrading?
* Is thesis drifting?

---

### Monthly Maintenance Actions

1. Review last 10 patches
2. Track insight preservation rate (target: 100%)
3. Track thesis drift incidents (target: 0)
4. Track unauthorized edit rate (target: 0)
5. Record findings in `model_health_log.md`

---

### SUSPENSION RULES

Suspend this engine if:

* Protected insights deleted twice
* Thesis drifts twice
* Unauthorized rewrites occur

---

## 🟢 KEY CHANGE

This engine now:

* Preserves insight
* Rebuilds examples instead of killing thesis
* Protects narrative flow
* Acts as surgeon, not author

This directly fixes your **"examples broke, thesis collapsed"** problem.

---

END OF ENGINE 06 — CONTROLLED PATCH MODE
