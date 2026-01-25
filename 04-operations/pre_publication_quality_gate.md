# 🔒 NIVESHAK PRE-PUBLICATION MASTER QUALITY GATE (v1.0)

**Run time**: 5 minutes  
**Mandatory before**: Platform Adaptors (ENGINES 10-12)  
**Authority**: Must pass all 10 gates before publication

---

## 🔵 GATE 1 — DATA INTEGRITY

**Already implemented. Verify:**

- [ ] All numbers sourced to filing / headline / transcript
- [ ] Periods consistent (no mixed FY / quarterly / half-year)
- [ ] No invented recency (e.g., "latest data" when 2 years old)
- [ ] Numbers match source ±0.1%

**Owner**: ENGINE 05 (Cross Verification)  
**If fails**: Route back to ENGINE 06 (Patch)

---

## 🔵 GATE 2 — LOGIC & FALSIFIABILITY

**Already implemented. Verify:**

- [ ] Core thesis stated clearly in opening
- [ ] At least 1 explicit invalidation metric stated
- [ ] Reasoning chain logically complete (A→B→C, not gaps)
- [ ] Claims testable by reader

**Owner**: ENGINE 07 (Red Team)  
**If fails**: RED TEAM VETO, force rewrite

---

## 🔵 GATE 3 — RED TEAM CLEARANCE

**Already implemented. Verify:**

- [ ] Red Team has signed off: YES / NO
- [ ] No unresolved critical issues
- [ ] Minor issues documented and accepted

**Owner**: ENGINE 07 (Red Team)  
**If fails**: BLOCK PUBLICATION

---

## 🔴 GATE 4 — SIGNATURE METRIC CHECK [NEW]

**Purpose**: Every serious post must have ONE diagnostic metric that lives beyond the post.

**Test:**

- [ ] One explicit metric named and defined
- [ ] Metric explained mechanistically (WHY it matters, not just WHAT it is)
- [ ] Metric is reusable by reader (they can check it themselves)
- [ ] Metric is novel OR used in novel way

**Examples (what passes):**

- "Flow Divergence Ratio: FII sells exceed DII buys by 2.3:1 (regime shift indicator)"
- "Governance Lag Index: Days between announcement and implementation averaging 47 (highest in 18 months)"
- "Credit Cost Compression: NIM spread narrowing by 45bps YoY (unsustainable signal)"

**Examples (what fails):**

- "Flows are weak" (no metric)
- "Valuation is high" (no specific metric)
- "Management is cautious" (not quantified)

**Action if fails:**

→ Route to ENGINE 08 (Apex): Add one signature metric OR REWRITE

---

## 🔴 GATE 5 — EDGE DIMENSION CHECK [NEW]

**Purpose**: Content must hit at least 2 of these 5+1 dimensions to avoid bland analysis.

**Test:**

Post hits at least **2 of these 6 edges**:

1. **Novel Metric** — Introduces a new way to measure something
2. **Regime Diagnosis** — Identifies structural shift in market behavior
3. **Governance Lens** — Interprets incentives through policy/disclosure rules
4. **Teaching While Analyzing** — Teaches a concept IN the analysis (not separate)
5. **Cross-Sector Pattern** — Spots pattern across industries (not single company)
6. **Product/Tool Reference** — References specific capability/limitation that matters

**Mark which edges hit:**

- [ ] Novel Metric
- [ ] Regime Diagnosis
- [ ] Governance Lens
- [ ] Teaching While Analyzing
- [ ] Cross-Sector Pattern
- [ ] Product/Tool Reference

**Count**: _____ (must be ≥2)

**Action if <2:**

→ REWRITE to add edge dimensions OR KILL post

---

## 🔴 GATE 6 — FRAMEWORK APPLICATION CHECK [NEW]

**Purpose**: Ensure frameworks are not forced or misapplied.

**Test by post type:**

### Sunday Brief:

- [ ] At least 1 framework explicitly taught
- [ ] Framework shapes the thesis (not decoration)
- [ ] Framework applied correctly to data

**If framework missing**: ADD one before publish

### Tuesday Audit / Friday Macro / Newsletter:

- [ ] Framework optional (not required)
- [ ] If framework used: Applied correctly to case?
- [ ] If framework forced/misapplied: REWRITE

**Check:**

- [ ] Any framework feel forced? (Yes/No)
- [ ] Any framework misapplied to data? (Yes/No)

**Action if forced/misapplied:**

→ Remove framework OR rewrite to apply correctly

---

## 🔴 GATE 7 — UNCERTAINTY & LIMITATION CHECK [NEW]

**Purpose**: Institutional credibility requires admitting what you don't know.

**Test:** Post includes at least ONE of:

- [ ] "What we don't know yet" section (explicit unknowns)
- [ ] Regime uncertainty admitted (e.g., "This assumes policy stability; if that breaks...")
- [ ] Model limitation admitted (e.g., "This analysis excludes FPI flows; they could shift outcomes")
- [ ] Data quality caveat (e.g., "Bulk deal data has 2-week reporting lag")

**Action if none present:**

→ ADD admission of uncertainty OR rewrite to include one

---

## 🔴 GATE 8 — FORWARD SCAN CHECK [NEW]

**Purpose**: Post should signal what to watch next, not just analyze past.

**Test:** Post includes at least ONE of:

- [ ] "What we're watching" or "Next trigger" section
- [ ] Transmission checkpoint stated (e.g., "This thesis breaks if FII flows return")
- [ ] Early warning indicator named (e.g., "Watch for credit cost stabilization")
- [ ] Timeline given (e.g., "This plays out over next 4-6 weeks")

**Action if none present:**

→ ADD forward signal OR remove from publication

---

## 🔴 GATE 9 — VOICE & READABILITY CHECK [NEW]

**Purpose**: Ensure prose quality and institutional voice consistency.

**Test:**

- [ ] No banned AI tells (see Bible for list)
- [ ] No em-dashes (use colons or full stops instead)
- [ ] Sentence rhythm varied (not all similar length)
- [ ] Not over-dense (avg <20 words per sentence)
- [ ] Passes Coffee Test (readable at 6am with coffee)

**Action if any fail:**

→ Route to ENGINE 09 (Polish) for rhythm fix

---

## 🔴 GATE 10 — LEGAL & GOVERNANCE SAFETY [NEW]

**Purpose**: Protect against defamation, motive attribution, fraud implication.

**Test:**

- [ ] No motive attribution without explicit filing evidence
  - ❌ "Management is hiding losses" (bad)
  - ✔ "Filing delay extends ±X days vs historical average" (good)
- [ ] No fraud association without regulatory citation
- [ ] All governance framed as data-based, not accusatory
- [ ] No defamation risk (no unsubstantiated negative claims)
- [ ] Any criticism supported by specific disclosure or action

**Action if any fail:**

→ Route to ENGINE 06 (Patch) for rewording

---

## 🟢 FINAL DECISION LOGIC

```
RUN ALL 10 GATES

IF (Gate 1 = PASS) AND (Gate 2 = PASS) AND ... (Gate 10 = PASS):
  → PUBLISH
  
ELSE:
  → DO NOT PUBLISH
  → Route to appropriate engine for fix
  → Re-run gates after fix
```

---

## 🟢 PRE-PUBLICATION CHECKLIST (USE THIS)

Copy and paste before every main post:

```
POST: ________________________  DATE: ________

□ GATE 1 (Data Integrity) .............. PASS / FAIL
□ GATE 2 (Logic & Falsifiability) ...... PASS / FAIL
□ GATE 3 (Red Team Clearance) .......... PASS / FAIL
□ GATE 4 (Signature Metric) ............ PASS / FAIL
□ GATE 5 (Edge Dimensions) ............ PASS / FAIL [___ / 6 edges hit]
□ GATE 6 (Framework Application) ....... PASS / FAIL
□ GATE 7 (Uncertainty Admitted) ........ PASS / FAIL
□ GATE 8 (Forward Scan) ............... PASS / FAIL
□ GATE 9 (Voice & Readability) ........ PASS / FAIL
□ GATE 10 (Legal & Safety) ............ PASS / FAIL

DECISION: PUBLISH / REWORK / KILL

Route to: _____________________
```

---

## 📊 TRACKING

Log each use in `framework_performance.md`:

- Date
- Post title
- Gates passed / failed
- Fixes applied
- Final decision

This creates a 10-gate quality history that surfaces patterns in what fails most.

---

**Version**: 1.0  
**Last Updated**: 26 January 2026  
**Authority**: Mandatory before ENGINE 10 (Platform Adapter Twitter)
