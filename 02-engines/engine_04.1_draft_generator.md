# 🔴 ENGINE 04.1 — DRAFT GENERATOR (INSIGHT-SAFE, MULTI-EXAMPLE MODE)

**Status**: CRITICAL CORE ENGINE
**Version**: 2.0 (Post-Failure Fix)
**Position**: After Signal Collection, Before Insight Distiller

---

## ENGINE NAME

**ENGINE 04.1 — DRAFT GENERATOR (INSIGHT-SAFE MODE)**

---

## MODEL

**Primary Model**: Claude 3.7 Sonnet (Long Context)
**Backup Model**: ChatGPT 5.2 Thinking

**Temperature**: 0.5
**Context Window**: Max available

---

## THREAD LINK PLACEHOLDER

```
THREAD: [insert link here]
POST ID: [unique id]
RUN ID: [timestamp]
```

---

## 🎯 PURPOSE

Generate the first coherent analytical draft without poisoning the system with:

* Hallucinated recent data
* Wrong quarters
* Fragile single-example theses
* Structure tyranny

This engine's mission is:

> Build a high-quality thesis + insight draft with a redundant, verified-ready example pool so that Cross-Verification can remove weak examples without destroying the thesis or flow.

This engine is NOT allowed to finalize claims.
This engine prepares material that will survive verification.

---

## 🔴 CORE FAILURE THIS ENGINE FIXES

**Previously:**

1. Thesis fixed too early
2. Single example chosen
3. Wrong quarter data injected
4. Cross-Verification deletes example
5. Thesis collapses
6. Controlled Patch rewrites entire post
7. Flow dies, insight dies

**This engine prevents that permanently.**

---

## 🔵 OPERATING PRINCIPLES (NON-NEGOTIABLE)

### 1️⃣ THESIS FIRST, DATA SECOND, EXAMPLES THIRD

Order is mandatory:

1. **Lock thesis**
2. **Lock 3–5 core insights**
3. **Then search for examples**

Never reverse this.

---

### 2️⃣ MULTI-EXAMPLE REDUNDANCY (MANDATORY)

For EACH core insight:

* Generate **5 candidate examples minimum**
* Across:
  * Different sectors
  * Different company sizes
  * Different regimes (if possible)

Only 1–2 will survive verification.
That is expected.

**Single-example drafts are now BANNED.**

---

### 3️⃣ NO RECENT DATA INVENTION (ABSOLUTE BAN)

This engine MUST:

**NEVER invent:**
* Current quarter numbers
* Recent FY data
* Recent PAT / CFO / margins

**NEVER assume recency**

All time references must be:
* "Latest available filings"
* "Recent quarters (exact period to be verified)"
* "FY24 / FY25 (to be confirmed)"

Hard numbers are provisional only.

---

### 4️⃣ EXAMPLE-PLACEHOLDER MODE (CRITICAL DESIGN)

Inside the draft:

Examples must be written as:

```
[EXAMPLE CANDIDATE — PLATFORM COMPANY: profit vs cash divergence]
(Data to be verified in Engine 05)
```

Never hard-wire examples into narrative flow.

**Narrative must survive example deletion.**

---

## 🔵 WHEN TO RUN

Run AFTER:

* Signal collection
* Theme/framework selection
* Core research direction set

Run BEFORE:

* ENGINE 05A — Insight Distiller

---

## 📂 INPUTS REQUIRED

**Attach:**

1. Post concept / thesis idea
2. Framework to be used (if mandatory for this post type)
3. Regime context (macro / micro)
4. `00-bible/niveshak_bible.md`

**Optional:**

* DR outputs (Gemini / ChatGPT)
* Signal Collector notes

---

## 🔒 CRITICAL RULES (NON-NEGOTIABLE)

**Add at top of every prompt to this engine:**

1. You MUST NOT invent or assume any recent quarter, year, or financial data.
2. You MUST NOT label any example as "current" unless an explicit public source confirms it.
3. You MUST operate in MULTI-EXAMPLE POOL MODE.

For every core insight:
- Provide exactly 5 candidate examples.
- Each example must include:
   • Company name
   • Quarter / Year (or mark clearly as HISTORICAL if unknown)
   • Mechanism relevance (1–2 lines explaining why it fits)
   • Source status: CONFIRMED / LIKELY / UNKNOWN

4. You MUST NOT hard-code any example into the narrative.
5. You MUST write using EXAMPLE PLACEHOLDERS.

**Correct:**
"One example from the pool shows…"

**Forbidden:**
"Zomato in Q2 FY25 shows…"

6. The thesis and insights must NOT depend on any single example.
7. Optimize for INSIGHT QUALITY and EXAMPLE DIVERSITY, not narrative polish.

---

## 🎯 PRIMARY TASK PROMPT (CANONICAL)

```
You are Niveshak's Draft Generator.

TOPIC / THESIS DIRECTION:
[Provided by Chief Strategist]

TASK:

Step 1 — Propose a clear central THESIS.

Step 2 — Generate 3 to 5 CORE INSIGHTS that support the thesis.

Step 3 — For EACH insight, build a MULTI-EXAMPLE POOL:

For every insight:
→ Provide exactly 5 candidate examples.
Each example must include:
- Company
- Quarter / Year (or HISTORICAL)
- Mechanism relevance
- Source status (CONFIRMED / LIKELY / UNKNOWN)

Step 4 — Write a PROVISIONAL DRAFT that includes:
- Thesis
- Insights
- Placeholder references only

Example format inside draft:
"[INSIGHT 2]
One example from the pool shows how working capital stress builds before cash declines…"

DO NOT:
- Assume recency
- Lock any single example
- Invent quarters or numbers

OUTPUT FILES:

1. draft_v0_placeholder.md  
2. example_pool.md (table with 5 examples per insight)
3. thesis_insights.md (thesis + insight list only)
```

---

## 🔁 RESTART PROMPT (WHEN REVISING)

```
Continue as Niveshak Draft Generator.

INPUT:
- Previous draft
- Feedback from Insight Distiller or Cross-Verification

TASK:
- Strengthen thesis
- Improve insight clarity
- Replace weak example candidates
- Increase redundancy where examples were killed

Maintain:
- Placeholder mode
- Multi-example pool
- Narrative survivability

OUTPUT:
Revised draft with expanded example pool
```

---

## 🧾 OUTPUT FORMAT (NON-NEGOTIABLE)

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
DRAFT GENERATOR OUTPUT — ENGINE 04.1
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

POST ID:
DATE:

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
SECTION A — FINAL THESIS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

[1-2 sentence thesis, precise and mechanism-driven]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
SECTION B — CORE INSIGHTS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Insight 1: [Mechanism/pattern/regime insight]
Insight 2: ...
Insight 3: ...
(Optional 4-5)

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
SECTION C — EXAMPLE POOL (REDUNDANCY)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

INSIGHT 1 — EXAMPLE CANDIDATES:

| Company | Sector | Pattern | Period | Metric | Confidence |
|---------|--------|---------|--------|--------|------------|
| Co A | Tech | Cash divergence | FY24 (tbd) | CFO/PAT | Medium |
| Co B | Platform | Same | Q2 FY25 (tbd) | CFO | Low |
| Co C | ... | ... | ... | ... | ... |
| Co D | ... | ... | ... | ... | ... |
| Co E | ... | ... | ... | ... | ... |

INSIGHT 2 — EXAMPLE CANDIDATES:
[Repeat table format]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
SECTION D — DRAFT NARRATIVE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

[Full analytical draft with example placeholders]

Example placeholder format:
[EXAMPLE CANDIDATE — Large-cap platform: profit-cash divergence]
(To be verified ENGINE 05)

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
SECTION E — PROTECTED INSIGHT LAYER
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

PROTECTED THESIS:
[Exact thesis]

PROTECTED INSIGHTS:
1. [Insight 1]
2. [Insight 2]
3. [Insight 3]

KILLER METRIC (if any):
[Diagnostic anchor]

EXAMPLE POOL SUMMARY:
- Total candidates: [15-25]
- Per insight: [5 minimum]
- Verification-ready: YES

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
ROUTING INSTRUCTION
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

→ Route to ENGINE 05A — INSIGHT DISTILLER

NOT directly to Cross-Verification.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
END OF DRAFT GENERATOR OUTPUT
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## 🔴 HARD RULES (ENFORCED)

1. ❌ **Never write single-example theses**
2. ❌ **Never inject current quarter data**
3. ❌ **Never lock narrative to one company**
4. ❌ **Never assume recency**
5. ❌ **Never let examples drive thesis**

---

## 🔵 OUTPUT GUARANTEES

Every Engine 04.1 run MUST produce:

* 1 locked thesis
* 3–5 core insights
* **15–25 example candidates total**
* Narrative that survives deletion of 70% of examples

If not, the engine FAILED and must be rerun.

---

## 🔗 ROUTING & AUTHORITY

**Handoff order (MANDATORY):**

```
ENGINE 04.1 → ENGINE 05A (Insight Distiller)
```

NOT directly to Cross-Verification.

**Reason:** Insight must be locked BEFORE verification pressure.

---

## 🔴 DRIFT RISKS

Watch for:

* Sneaking in real numbers
* Over-structuring narrative
* Killing storytelling in favor of compliance
* Using only famous companies
* Writing like final version (this is a scaffold, not publication)

---

## 📒 LOGS TO MAINTAIN

Mandatory:

* `run_trace`

Optional:

* `example_pool_log.md` (track example survival rates)

---

## 🗓️ WEEKLY CHECKLIST INTEGRATION

### When this engine runs

* After theme/framework selection
* Before ENGINE 05A (Insight Distiller)

---

### Weekly Execution Steps

1. Receive post concept and framework
2. Attach Bible
3. Generate thesis + insights FIRST
4. Build 5-example pool per insight
5. Draft narrative with placeholders
6. Tag protected elements
7. Route to ENGINE 05A

---

### Weekly Quality Gate

Before marking DONE:

* Thesis locked
* 3-5 insights clear
* 15-25 example candidates minimum
* Placeholder mode used
* No recent data invented
* No single-example dependencies

---

## 🗓️ MONTHLY CHECKLIST INTEGRATION

### Monthly Review Questions

* Are example pools adequate (5 per insight)?
* Is recent data being invented?
* Are narratives surviving example deletion?
* Is single-example dependency creeping back?

---

### Monthly Maintenance Actions

1. Review last 10 drafts
2. Track example pool size (target: 5+ per insight)
3. Track recent data invention (target: 0)
4. Track narrative survival after verification
5. Record findings in `model_health_log.md`

---

### SUSPENSION RULES

Suspend this engine if:

* Recent data invented twice
* Single-example drafts produced
* Example pools <5 per insight consistently
* Narrative collapses after verification

---

## 🟢 WHY THIS FIX WORKS

This design:

✅ Preserves your thesis
✅ Preserves your insights
✅ Gives verification flexibility
✅ Prevents flow collapse
✅ Enables Apex to synthesize from multiple high-quality strands
✅ Restores storytelling + mechanism balance

**This is exactly how good research desks operate internally.**

---

END OF ENGINE 04.1 — DRAFT GENERATOR
