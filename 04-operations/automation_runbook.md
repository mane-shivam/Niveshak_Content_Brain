# 🧠 NIVESHAK AUTOMATION RUNBOOK

**Version 1.0 | Human Control Manual for Engine 13**

This file defines how the Niveshak Automation System is operated, supervised, paused, resumed, audited, and recovered.

This is the **human execution layer** above all AI engines.

If automation breaks quality, this document is the first line of defense.

---

## 🎯 ROLE DEFINITION

You are operating as:

* Head of Content
* Chief Editorial Authority
* Chief Safety & Failure Officer
* Final Merge Authority

Automation exists to serve you.
You are the only entity allowed to approve, override, merge, or publish.

No engine may bypass you.

---

## 🔐 ABSOLUTE CONTROL PRINCIPLES

1. **Human approval is mandatory at every engine**
2. **No branch ever merges without manual review**
3. **No content publishes without human sanity check**
4. **No failure is auto-resolved**
5. **No core file is ever modified by automation**

Automation is a tool.
You are the institution.

---

## 🧠 RUN TRACE SYSTEM (THE EXECUTION BLACK BOX)

**Folder**: `04-operations/run_traces/`  
**Template**: `run_trace_template.md`

### What is Run Trace?

The Run Trace file is your **ground truth log** for every automation run. It contains:
- Raw engine outputs (verbatim)
- Human overrides
- Approval decisions
- Timestamps
- Failure flags
- Original + edited versions

**This is the ONLY source of truth for passing outputs between engines.**

### Before Each Workflow Run

1. Copy the template → `run_YYYY_MM_DD_HHMM_[workflow].md`
2. Fill in the PRE-RUN STATE section
3. This file is now your active trace

### During Each Engine

1. Run the engine
2. Paste raw output into the engine block
3. Fill in "Final Output Passed Forward" section
4. Mark approval status
5. Next engine reads FROM THIS SECTION (not threads)

### After the Full Run

1. Append the "RUN COMPLETE" block
2. Mark file as LOCKED
3. Archive to `archive/run_traces/`

### Run Trace Review Protocol (WEEKLY)

After each full run, you must:
- Open the run trace file
- Scroll through every engine block
- Check:
  - Prompt drift
  - Missing signals
  - Weak reasoning
  - Excess verbosity
  - Repeated errors

Weekly:
- Compare last 3 run traces
- Look for quality decay

This is how you decide:
- Model replacement
- Prompt tuning
- Engine redesign

---

## 🟢 HOW TO START A SYSTEM RUN (DAILY / WEEKLY)

### Step 1 — Pre-Run Readiness Check (5 minutes)

Before triggering any run, verify:

* You have 2–3 uninterrupted hours available
* Gmail is open and logged into `maneshivam111@gmail.com`
* GitHub repo is open in browser
* You are mentally ready to review multiple drafts

If not ready → Delay the run. Never rush.

---

### Step 2 — Trigger Automation Manually

Open Comet and type:

```
START NIVESHAK [WORKFLOW] RUN
```

Where `[WORKFLOW]` is one of:

* SUNDAY
* MONDAY_RESEARCH
* TUESDAY_AUDIT
* THURSDAY_SIGNALS
* FRIDAY_MACRO
* SATURDAY_MEMORY

Automation will:

* Create a new branch
* Send you a “RUN STARTING” email
* Wait for your on-screen confirmation

---

### Step 3 — Confirm Pre-Run Email

You must receive an email:

**Subject:**
`NIVESHAK SYSTEM RUN STARTING — READY FOR APPROVALS`

Check:

* Correct workflow
* Correct number of engines
* Correct branch name
* No unexpected engines included

Reply nothing.
Return to Comet and click **CONFIRM START**.

---

## 🔵 ENGINE-BY-ENGINE SUPERVISION FLOW

For EACH engine, the following loop repeats.

This is the heart of the system.

---

### 🟠 PERPLEXITY PRO VALIDATION (CRITICAL GATE BEFORE RESEARCH)

**AFTER Engine 02 (Signal Collector), BEFORE Engine 03 (Research Desk):**

You MUST run the Perplexity Pro validation step:

**Thread Link**: https://www.perplexity.ai/search/validate-all-financial-data-ac-QHWhLz72QE.ORX06I0upag

**Prompt**:
```
Validate all financial data, accounting claims, regulatory references.
List contradictions, missing disclosures, weak assumptions.
Cite sources where possible.

RAW SIGNALS INPUT:
[Paste raw signals data from Engine 02 here]
```

**Checklist**:
- [ ] Raw signals from E02 collected
- [ ] Perplexity Pro run in Research Mode
- [ ] Contradictions reviewed
- [ ] Weak assumptions flagged

🚫 Do NOT proceed to Deep Research (E03) until validation passes.

---

### 🟣 ENGINE 04.1: FINAL POLISHING (POST-APEX)

**AFTER Engine 04 (Apex Synthesizer), BEFORE Engine 09 (Red Team):**

You MUST run the Final Polishing step:

**Thread Link**: https://claude.ai/chat/d6d6f36b-45bc-443b-9546-c844e53ee40a

**Prompt**:
```
Rewrite ONLY for clarity, rhythm, and human voice.
Preserve all data, numbers, and structure.
Do not simplify or add claims.
Flag any sentence that sounds artificial.

INPUT (Apex Master Draft):
[Paste Engine 04 output here]
```

**Checklist**:
- [ ] Apex draft received
- [ ] Claude polishing run
- [ ] Flagged sentences reviewed
- [ ] Changes log checked

🚫 Do NOT proceed to Red Team until polishing complete.

---

### 🔹 When an Engine Finishes

You will receive:

1. An email:
   `[ENGINE XX COMPLETE] — Approval Required`

2. An on-screen popup showing:

   * Engine name
   * Summary
   * Files modified
   * Two buttons

---

### 🔹 Your Decision Options (MANDATORY)

You must choose one:

#### Option 1 — Continue with latest response

Use this ONLY when:

* Logic is correct
* Voice matches Bible
* No hallucination
* No tone drift
* Framework intact

Click → **Continue with latest response**

Automation commits and proceeds.

---

#### Option 2 — Enter custom response (MOST IMPORTANT)

Use this when:

* Framework needs tightening
* Tone is off
* Structure weak
* Data needs correction
* Metaphor wrong
* Risk unclear

Paste your edited version.

Automation will:

* Overwrite the engine output file
* Discard the AI version
* Mark internally as HUMAN_APPROVED
* Commit and proceed

This is how institutional quality is preserved.

---

## 🔴 RED TEAM CHECKPOINT (CRITICAL CONTROL POINT)

When Red Team runs:

You will receive a separate email:

**Subject:**
`🔴 HIGH CRITICAL — RED TEAM ENGINE RESULT`

This is a **hard blocker**.

Your actions:

### If Verdict = PUBLISH

→ Approve and continue

### If Verdict = REWRITE

→ Open draft
→ Fix manually
→ Re-run Red Team

### If Verdict = KILL

→ Stop this thesis
→ Log in failure_log
→ Return to Chief Strategist

🚫 Automation must NEVER proceed past Red Team without your explicit approval.

This protects Niveshak’s reputation.

---

## 🟡 FAILURE EVENTS — WHAT YOU MUST DO

Automation will stop and alert you if:

* Data verification fails
* Invalidation missing
* Contrarian unresolved
* Legal risk flagged
* Model health degrades
* Red Team blocks

When this happens:

### Step 1 — Read Failure Email Carefully

Never click continue blindly.

### Step 2 — Decide Path

Choose ONE:

* Fix manually and continue
* Kill this thesis
* Pause entire run

### Step 3 — Confirm in Popup

Automation resumes only after you approve.

All failures are logged permanently.

---

## 🟣 PAUSE, WAIT, RESUME BEHAVIOR

If you step away mid-run:

* Automation enters IDLE
* Sends reminder after 5 minutes (max 3)
* Sends one email after 15 minutes
* Keeps state safely in automation_state.json

When you return:

Automation resumes from **exact last engine**.

No restart. No duplication.

---

## 🧾 BRANCH REVIEW & MERGE PROTOCOL (MOST IMPORTANT)

After the full workflow finishes:

### Step 1 — Open the Automation Branch

Example:
`perplexity_run_20260121_0930_pm`

---

### Step 2 — Review Files Carefully

You MUST review:

* All drafts
* All logs
* changelog_automation.md
* automation_state.json
* indexes updated
* No core file touched

Look for:

* Tone drift
* Hidden predictions
* Framework violations
* Accidental core edits

---

### Step 3 — Decide

#### If Everything Clean:

→ Merge manually into `main`

#### If Problems Found:

→ Edit in branch
→ Re-commit
→ Then merge

🚫 Never let automation merge.

You are final authority.

---

## 🟤 DAILY CHECKPOINTS YOU MUST DO (10 MIN TOTAL)

### After Each Run

Verify:

* changelog_automation.md updated
* automation_state.json shows COMPLETED
* No engine skipped
* No unauthorized file changed

---

### Weekly (Saturday Memory Slot)

Review:

* framework_performance.md
* failure_log.md
* model_health_log.md
* reader-signals.md

Ask:

* Which engine degrading?
* Which framework failing?
* Which metaphors working?

Feed this into next week’s arc.

---

## 🔵 FIRST WEEK SPECIAL MODE

During Week 1 of automation:

You MUST:

* Manually inspect every engine output deeply
* Reject aggressively
* Fix tone early
* Tune prompts after runs

After Week 2:

* Trust decreases
* Edits reduce
* Speed improves

Never skip supervision early.

---

## 🚨 EMERGENCY SHUTDOWN PROTOCOL

If automation behaves dangerously:

Type immediately in Comet:

```
STOP ALL NIVESHAK AUTOMATION
```

Then:

* Close session
* Do not merge branch
* Inspect automation_state.json
* Review changelog
* Fix before next run

---

## 🧠 GOLDEN RULES

Memorize these:

1. Automation saves time, not judgment
2. Red Team is sacred
3. Branch discipline protects reputation
4. Logs protect future training
5. You are the only merge authority
6. Quality > Speed always

---

## 🏁 FINAL NOTE

If you follow this runbook:

* You will save 20–25 hours per week
* Quality will not degrade
* Framework memory will compound
* Training data will be clean
* Niveshak will behave like an institution

This system is now:

**Safer than most hedge fund research pipelines.**
**More disciplined than sell-side desks.**
**Better structured than most AI startups.**
