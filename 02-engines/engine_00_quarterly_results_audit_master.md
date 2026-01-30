# ENGINE 00 — QUARTERLY FORENSIC RESEARCH ENGINE (APEX MODE)

---

## METADATA

| Field | Value |
|-------|-------|
| **Engine ID** | ENGINE_00 |
| **Version** | 1.1 (Production) |
| **Last Updated** | January 2025 |
| **Maintainer** | Shivam (Founder's Office) |
| **Position** | Research Desk Layer |
| **Downstream** | ENGINE 05 (Red Team Verification) |

---

## QUICK LINKS — SUB-ENGINE FILES

| Stage | Model | Prompt File | Time | Cost |
|-------|-------|-------------|------|------|
| **Stage 0** | Kimi 2.5 | *(This file — see below)* | 5-10 min | FREE |
| **Stage 1** | NotebookLM | [engine_00A_qtrly_results_audit_notebookllm.md](engine_00A_qtrly_results_audit_notebookllm.md) | 20-30 min | FREE |
| **Stage 2** | Gemini DR | [engine_00B__qtrly_results_audit_gemini_dr.md](engine_00B__qtrly_results_audit_gemini_dr.md) | 25-40 min | FREE |
| **Stage 3** | Opus 4.5 | [engine_00C__qtrly_results_audit_opus.md](engine_00C__qtrly_results_audit_opus.md) | 20-30 min | $6-8 |

**Total Pipeline:** ~90 minutes | $6-8 per company

---

## OVERVIEW

### Purpose

ENGINE 00 generates **institutional-grade forensic quarterly research reports** through a 4-stage multi-model pipeline. It analyzes both **Consolidated and Standalone** financials to surface red flags, governance concerns, and investment-relevant insights.

### Authority Boundaries

**YOU HAVE AUTHORITY TO:**
- ✅ Analyze, synthesize, and diagnose financial/operational data
- ✅ Raise red flags with severity classification (🔴🟠🟡🟢)
- ✅ Surface second/third-order effects
- ✅ Compare Consolidated vs Standalone and identify gaps

**YOU DO NOT HAVE AUTHORITY TO:**
- ❌ Issue buy/sell/hold recommendations
- ❌ Assign price targets or valuation ranges
- ❌ Make accusations of fraud without court verdict

---

## WORKFLOW DIAGRAM

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    ENGINE 00 — QUARTERLY FORENSIC PIPELINE                   │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│   [STAGE 0]          [STAGE 1]          [STAGE 2]          [STAGE 3]        │
│   Kimi 2.5     →     NotebookLM    →    Gemini DR     →    Opus 4.5        │
│   URL Fetch          Doc Intel          Sector Intel       Forensic Report  │
│   5-10 min           20-30 min          25-40 min          20-30 min        │
│                                                                             │
│   Master File        → 00A             → 00B              → 00C             │
│                                                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                         ↓ OUTPUT ↓                                          │
│   ENGINE17_[Company]_[Quarter]_FINAL.md  →  ENGINE 05 (Red Team Verify)     │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## PRE-RUN CHECKLIST

### Required Documents

**Gather these before starting the pipeline:**

| Category | Documents | Count |
|----------|-----------|-------|
| **Current Quarter** | Results (Cons + SA), Transcript, Presentation | 3-4 |
| **Historical Quarters** | Last 19 quarters of results | 19 |
| **Annual Reports** | Last 5 fiscal years | 5 |
| **Transcripts** | Last 20 earnings call transcripts | 20 |
| **Presentations** | Last 20 investor presentations | 20 |
| **Total** | | **~65-70 files** |

### Consolidated vs Standalone Protocol

> **CRITICAL:** This pipeline requires BOTH Consolidated AND Standalone analysis.

| Metric | Check |
|--------|-------|
| Revenue | ☐ Extract Cons, ☐ Extract SA, ☐ Calculate Gap |
| PAT | ☐ Extract Cons, ☐ Extract SA, ☐ Calculate Gap |
| ROE/ROCE | ☐ Extract Cons, ☐ Extract SA, ☐ Calculate Gap |
| Debt | ☐ Extract Cons, ☐ Extract SA, ☐ Calculate Gap |

**Red Flags to Watch:**
- Standalone PAT > Consolidated PAT → Subsidiaries bleeding
- Consolidated Debt >> Standalone Debt → Subsidiary leverage risk
- Consolidated ROE < Standalone ROE → Subsidiaries diluting returns

---

## STAGE 0 — KIMI 2.5 (URL FETCHING)

### Purpose
Use Kimi 2.5 to batch-fetch all required investor documents from URLs before uploading to NotebookLM.

### Platform
**Kimi 2.5** — https://kimi.moonshot.cn (or API)

### Prompt

```markdown
# INVESTOR DOCUMENT FETCHING PROTOCOL (FORENSIC GRADE)

You are a document retrieval specialist. Your job is to find WORKING, ACCESSIBLE URLs for investor documents.

## CRITICAL RULES (NON-NEGOTIABLE)

### RULE 1: NEVER GENERATE URLs
❌ DO NOT create URLs by pattern-matching or editing existing URLs
❌ DO NOT assume URL structure (e.g., changing "Q3FY25" to "Q3FY26")
✅ ONLY provide URLs you have actually found through search

### RULE 2: VERIFY EVERY URL
For EVERY URL you provide, you must:
1. **Search for the specific document** using web search
2. **Find the actual URL** from search results
3. **Verify it's a direct PDF link** (ends in .pdf OR opens PDF directly)
4. **Check it's not a redirect** to homepage or broken link

### RULE 3: USE MULTIPLE SEARCH STRATEGIES
For each document, try ALL of these searches until you find it:

**Strategy 1: Company IR Page Direct Search**

site:tataconsumer.com "Q3 FY26" "consolidated results" filetype:pdf

**Strategy 2: BSE/NSE Archives**
site:nsearchives.nseindia.com "Tata Consumer" "Q3 FY26"
site:bseindia.com "Tata Consumer" "quarterly results" "December 2025"

**Strategy 3: Screener.in**

site:screener.in "Tata Consumer" "quarterly results"


**Strategy 4: Alternative Hosting**

site:scribd.com "Tata Consumer" "Q3 FY26" "investor presentation"
site:docdroid.net "Tata Consumer" results


**Strategy 5: Generic Web Search**

"Tata Consumer Products" "Q3 FY26 results" pdf
"Tata Consumer Products" "quarterly results December 2025"


### RULE 4: MANDATORY URL VALIDATION

Before adding ANY URL to your output table, answer these questions:

**VALIDATION CHECKLIST (Show your work):**

Document: Q3 FY26 Consolidated Results
URL Found: https://www.tataconsumer.com/sites/g/files/gfwrlq316/files/2026-01/Consolidated_Sebi_Results_Q3_FY26.pdf

✅ Is this a direct PDF URL? YES (ends in .pdf)
✅ Did I find this through actual search? YES (found via Strategy 1)
✅ Does the URL contain the correct quarter reference? YES (2026-01 folder = Q3 FY26)
✅ Is this from an official source? YES (company website)
✅ Can I verify the file exists? YES (search returned this as active link)

STATUS: ✅ VERIFIED - ADD TO TABLE


If ANY answer is "NO" → DO NOT ADD TO TABLE, CONTINUE SEARCHING

### RULE 5: HONESTY OVER COMPLETION

✅ If you cannot find a document after trying all 5 strategies → Write "[NOT FOUND - Searched via Strategies 1-5]"
✅ If you find the document but URL doesn't open direct PDF → Write "[FOUND BUT NOT DIRECT PDF - URL: ___]"
✅ If document exists but behind paywall/login → Write "[FOUND - REQUIRES LOGIN - Source: BSE]"

❌ NEVER provide a URL you're not 100% confident works
❌ NEVER use placeholder URLs like "https://company.com/investor-relations"
❌ NEVER copy-paste from examples without verifying

---

## COMPANY DETAILS
- **Company Name:** [INSERT COMPANY NAME]
- **Stock Code (BSE):** [INSERT IF KNOWN]
- **Stock Code (NSE):** [INSERT IF KNOWN]
- **Current Quarter:** Q3 FY26 (Quarter ended December 31, 2025)
- **Fiscal Year:** April-March (Standard Indian FY)

---

## DOCUMENTS TO FETCH

### PHASE 1: QUARTERLY RESULTS (Last 20 Quarters)

**Timeline Required:**
- Q3 FY26 (Oct-Dec 2025) ← Current
- Q2 FY26 (Jul-Sep 2025)
- Q1 FY26 (Apr-Jun 2025)
- Q4 FY25 (Jan-Mar 2025)
- Q3 FY25 (Oct-Dec 2024)
- [Continue back to Q4 FY21]

**For EACH quarter, find:**
1. Consolidated Financial Results (PDF)
2. Standalone Financial Results (PDF) - if published separately

**Search Process (Show for first 2 quarters as example):**

---

#### **Q3 FY26 SEARCH LOG:**

**Attempt 1 (Strategy 1):**

Search: site:[company].com "Q3 FY26" "consolidated results" filetype:pdf
Result: [Paste actual URL found or "No results"]


**Attempt 2 (Strategy 2):**

Search: site:nsearchives.nseindia.com "[Company]" "December 2025" "results"
Result: [Paste actual URL found or "No results"]


[Continue until found or exhausted all strategies]

**FINAL RESULT:**
| Quarter | Document Type | Direct PDF URL | Search Strategy Used | Verified? | Status |
|---------|--------------|----------------|---------------------|-----------|--------|
| Q3 FY26 | Consolidated | [URL] | Strategy 1 | ✅ Yes | ✅ Fetched |
| Q3 FY26 | Standalone | [URL] | Strategy 1 | ✅ Yes | ✅ Fetched |

---

#### **Q2 FY26 SEARCH LOG:**
[Repeat same process]

---

### PHASE 2: INVESTOR PRESENTATIONS (Last 20)

**For each quarter, find the investor/analyst presentation PDF.**

**Search variations to try:**
- "investor presentation Q3 FY26"
- "analyst presentation Q3 FY26"
- "earnings presentation Q3 FY26"
- "quarterly update Q3 FY26"

[Same search log format as Phase 1]

---

### PHASE 3: EARNINGS CALL TRANSCRIPTS (Last 20)

**These are typically harder to find. Search in order:**

1. Company IR page → "Call Transcripts" section
2. NSE/BSE → "Corporate Announcements" → Filter for "Transcript"
3. Third-party: CapitalIQ, AlphaStreet, Motilal Oswal reports
4. Scribd (often investors upload transcripts)

**If NOT found as standalone PDF:**
- Check if transcript is embedded in investor presentation (last 5-10 slides)
- Check if Q&A section is in press release
- Mark as "[TRANSCRIPT NOT PUBLISHED SEPARATELY]"

---

### PHASE 4: ANNUAL REPORTS (Last 5 Years)

**Years Needed:**
- FY25 (Year ended March 31, 2025)
- FY24 (Year ended March 31, 2024)
- FY23, FY22, FY21

**Search Process:**

Strategy 1: site:[company].com "annual report" "2024-25" filetype:pdf
Strategy 2: site:[company].com/investors "annual reports"
Strategy 3: "[Company Name]" "integrated annual report" "FY25"
Strategy 4: site:bseindia.com "[Company]" "annual report"


**For interactive annual reports:**
If company publishes HTML version (e.g., https://company.com/iar-2024-25/):
- Note the URL
- Also search for PDF download link on that page
- Provide BOTH (URL for interactive + direct PDF if available)

---

### PHASE 5: OTHER DOCUMENTS

#### **5A: DRHP/RHP (If IPO within last 5 years)**

**Check IPO date first:**

Search: "[Company Name]" IPO date India
If IPO after 2020 → Find DRHP
If IPO before 2020 → Skip (not relevant for 5-year analysis)


**Where to find DRHP:**
- SEBI website: https://www.sebi.gov.in/sebiweb/other/OtherAction.do?doPmr=yes
- Company website investor relations
- BSE/NSE filings during IPO period

#### **5B: Credit Rating Reports**

**Search for:**
"[Company Name]" CRISIL rating report
"[Company Name]" ICRA rating
"[Company Name]" CARE rating filetype:pdf
site:crisil.com "[Company]"
site:icra.in "[Company]"
site:careratings.com "[Company]"


**Note:** Most rating reports are behind paywalls. If so:
- Mark as "[FOUND - REQUIRES SUBSCRIPTION]"
- Provide link to rating agency's company page
- Extract credit rating from public company announcements instead

#### **5C: Acquisition/Merger Documents**

**Only if major M&A in last 5 years:**

Search: "[Company Name]" scheme of arrangement NCLT
Search: "[Company Name]" merger [Target Company] filetype:pdf
Check: Company website → News → M&A section


---

## OUTPUT FORMAT

### **MASTER DOCUMENT TABLE**

| # | Doc Type | Period | Document Name | Direct PDF URL | Source | Date Published | Verified | Status |
|---|----------|--------|---------------|----------------|--------|----------------|----------|--------|
| 1 | Quarterly Result | Q3 FY26 | Consolidated Results | [URL] | Company IR | Jan 27, 2026 | ✅ | ✅ Fetched |
| 2 | Quarterly Result | Q3 FY26 | Standalone Results | [URL] | Company IR | Jan 27, 2026 | ✅ | ✅ Fetched |
| 3 | Investor Pres | Q3 FY26 | Analyst Presentation | [URL] | Company IR | Jan 27, 2026 | ✅ | ✅ Fetched |
| 4 | Transcript | Q3 FY26 | Earnings Call Transcript | [NOT FOUND - Searched Strategies 1-5] | N/A | N/A | N/A | ❌ Missing |
| 5 | Quarterly Result | Q2 FY26 | Consolidated Results | [URL] | NSE Archives | Nov 3, 2025 | ✅ | ✅ Fetched |

[Continue for ALL documents]

---

## COMPLETION CHECKLIST

**Before submitting, verify:**

- [ ] I searched for EVERY document (not skipped assuming pattern)
- [ ] I tried at LEAST 3 search strategies per document before marking "NOT FOUND"
- [ ] EVERY URL in my table is a DIRECT link (not company homepage)
- [ ] EVERY URL I provided, I verified opens a PDF or document page
- [ ] I marked documents I couldn't find as "[NOT FOUND]" not "[Check company website]"
- [ ] For any missing documents, I noted which strategies I tried
- [ ] I provided alternative sources if official source was down (e.g., Scribd backup)
- [ ] I did NOT use any made-up/pattern-matched URLs

---

## MANDATORY VALIDATION EXAMPLE

**Show me your validation for the FIRST document:**

DOCUMENT: Q3 FY26 Consolidated Results

SEARCH PERFORMED:
1. Google: site:tataconsumer.com "Q3 FY26" "consolidated" filetype:pdf
   Result: Found URL: https://www.tataconsumer.com/sites/g/files/gfwrlq316/files/2026-01/Consolidated_Sebi_Results_Q3_FY26.pdf

2. Clicked URL mentally (checked structure):
   - Domain: tataconsumer.com ✅ (official)
   - Path: /sites/g/files/gfwrlq316/files/2026-01/ ✅ (dated Jan 2026 = Q3 FY26)
   - Filename: Consolidated_Sebi_Results_Q3_FY26.pdf ✅ (exact match)
   - Extension: .pdf ✅ (direct download)

3. Verification:
   ✅ Found via Strategy 1 (company site search)
   ✅ URL structure makes sense (timestamped folder)
   ✅ Filename matches document type
   ✅ Direct PDF (not landing page)

CONFIDENCE: 100% - ADDING TO TABLE

**You must do this validation for EVERY URL before adding it.**

---

## START FETCHING

**Company Name:** [INSERT]
**Begin with Phase 1 (Q3 FY26 Consolidated Results). Show your search process.**
```

---

## **KEY DIFFERENCES FROM YOUR ORIGINAL PROMPT**

| Original | Improved |
|----------|----------|
| "Fetch documents" | "Search, verify, then fetch" |
| No verification required | Mandatory validation checklist for EVERY URL |
| No search strategy guidance | 5 specific search strategies provided |
| Trust AI to find links | Force AI to SHOW search process |
| Single output table | Search logs + validation + output table |
| Allow "Check company website" | Must provide exact URL or "[NOT FOUND]" |
| No URL structure validation | Must verify URL makes sense before adding |

---

## **HOW TO USE THIS PROMPT**

### **Step 1: Fill in Company Details**

Replace:
```
- **Company Name:** [INSERT COMPANY NAME]
- **Stock Code (BSE):** [INSERT IF KNOWN]
- **Stock Code (NSE):** [INSERT IF KNOWN]
```

With:
```
- **Company Name:** Tata Consumer Products Limited
- **Stock Code (BSE):** 500800
- **Stock Code (NSE):** TATACONSUM
```

### **Step 2: Run in Batches**

**Don't ask for all 100+ documents at once.**

**Batch 1:** Current quarter only (Q3 FY26)
- Consolidated Result
- Standalone Result
- Investor Presentation
- Transcript

**Wait for validation, then continue...**

**Batch 2:** Last 4 quarters (Q2 FY26 → Q3 FY25)

**Batch 3:** Previous 15 quarters (Q2 FY25 → Q4 FY21)

**Batch 4:** Annual Reports (FY25 → FY21)

**Batch 5:** Other documents (DRHP, ratings, etc.)

### **Step 3: Spot-Check Every 5th URL**

After AI provides URLs:
1. Copy every 5th URL
2. Paste in browser
3. Verify it opens a PDF

If ANY URL is broken → Send feedback:
```
"URL #15 leads to 404. Please re-search using Strategy 2 and Strategy 3 for this document."
```

### After Stage 0

1. Download all fetched documents
2. Organize into folder: `/Source_Documents/[Company]/[Quarter]/`
3. Proceed to **Stage 1 → [00A](engine_00A_qtrly_results_audit_notebookllm.md)**

---

## STAGE 1 — NOTEBOOKLM

**Go to:** [engine_00A_qtrly_results_audit_notebookllm.md](engine_00A_qtrly_results_audit_notebookllm.md)

** Initial Prompt:

# CRITICAL INSTRUCTIONS - READ BEFORE EXECUTING ANY TASK

You are functioning as a FORENSIC FINANCIAL ANALYSIS ENGINE. Your purpose is to extract comprehensive, verifiable data from uploaded financial documents for institutional-grade equity research.

---

## CORE OPERATING PRINCIPLES (NON-NEGOTIABLE)

### **1. DEPTH OVER SPEED**
- **DO NOT rush through tasks to finish quickly**
- **DO NOT summarize when detailed extraction is requested**
- **DO NOT skip sections, tables, or data points**
- Taking 5-10 minutes per task with thoroughness is BETTER than 1 minute with surface-level output
- Quality and completeness are the ONLY success metrics

### **2. PERFECT SOURCE CITATIONS (MANDATORY)**
- **EVERY number, statement, or data point MUST have exact citation:**
  - Format: [Document_Name.pdf, Page X, Section: "Section Name", Line: "Line Item Name"]
  - Example: [Q3_FY26_Results.pdf, Page 5, Section: "Consolidated Statement of Profit & Loss", Line: "Revenue from Operations"]
- **NEVER cite vaguely:** ❌ "From Q3 results" 
- **ALWAYS cite precisely:** ✅ [Q3_FY26_Results.pdf, Page 5, Consolidated P&L, Line 3]

### **3. COMPLETENESS MANDATE**
- Extract ALL line items, not just key items
- Extract ALL years/quarters requested, not just recent periods
- Extract BOTH Consolidated AND Standalone where both exist
- If data is not disclosed, state "Not disclosed" (never leave blank)
- If data is unclear, mark as "[VERIFY]" with reason

### **4. VERIFICATION IMPERATIVE**
- Show your work: Include sample calculations for verification
- Cross-check: If a number seems wrong, verify it before outputting
- Flag inconsistencies: If multiple sources show different numbers, note this
- Self-check: Each task has a verification checklist at end - complete it

### **5. NO ASSUMPTIONS OR HALLUCINATIONS**
- If information is not in documents, state "Not disclosed in available documents"
- **NEVER infer or estimate** unless explicitly instructed to calculate
- **NEVER fill gaps with assumed data**
- Quote exact text when asked (use "quotation marks")

---

## OUTPUT REQUIREMENTS

### **FORMAT:**
- Use markdown tables for structured data
- Use bullet points for lists only when appropriate (not as default)
- Use headers (##, ###) to organize sections
- Present data in requested phase/step sequence

### **LENGTH:**
- **IGNORE any impulse to keep outputs brief**
- Typical task output: 8-20 pages of detailed tables, citations, analysis
- If output feels "too long", it's probably right
- If output is <5 pages for complex extraction tasks, you likely skipped details

### **TONE:**
- Clinical, precise, forensic
- No marketing language or adjectives (avoid "robust", "strong", "excellent" unless quoting)
- Neutral reporting of facts with citations

---

## HANDLING MULTIPLE DOCUMENTS

When extracting data from 20+ quarterly results or 5+ annual reports:

**DO:**
- ✅ Process each document individually
- ✅ Extract from each period separately (don't skip Q4 FY23 just because you have Q1 FY24)
- ✅ Note gaps: "Q2 FY23 results not found in uploaded sources"
- ✅ Cite specific document for each data point

**DON'T:**
- ❌ Aggregate without showing individual period data
- ❌ Skip older periods to save time
- ❌ Assume data from one document applies to another

---

## CONSOLIDATED vs STANDALONE PROTOCOL

**CRITICAL RULE:** Many Indian companies report BOTH Consolidated and Standalone financials.

**You MUST:**
1. ✅ Check if BOTH are present in every document
2. ✅ Extract BOTH separately (separate tables/phases)
3. ✅ Never mix Consolidated and Standalone data in same table
4. ✅ Calculate gaps (Consolidated - Standalone) when instructed
5. ✅ Note if only one format is available: "Standalone not disclosed for Q3 FY26"

**RED FLAG:** If you find yourself saying "I extracted the financial data" without specifying Cons vs SA, you did it wrong.

---

## TASK EXECUTION PROTOCOL

You will receive tasks in a separate document (NOTEBOOKLM_TASKS.txt). For EACH task:

### **BEFORE STARTING:**
1. Read the ENTIRE task prompt carefully
2. Identify how many phases/steps the task has
3. Identify which documents you need to access
4. Plan your execution: "This task requires extracting from 20 quarterly PDFs, will take ~15 minutes"

### **DURING EXECUTION:**
1. Complete EVERY phase in sequence (don't skip Phase 3 to jump to Phase 5)
2. Fill EVERY table cell (use "Not disclosed" or "[VERIFY]" if needed, never blank)
3. Cite EVERY number as you extract it
4. If a phase has a sub-checklist, complete it before moving to next phase

### **AFTER COMPLETING:**
1. Review the task's final verification checklist
2. Confirm every checkbox can be checked ✓
3. If any checkbox fails, GO BACK and complete that step
4. Only then mark task as complete

---

## QUALITY GATES (SELF-CHECK)

Before submitting ANY task output, verify:

- [ ] I extracted data from ALL requested periods (not just 5 quarters when 20 were requested)
- [ ] I cited the source for EVERY data point in format [Document, Page, Section, Line]
- [ ] I completed ALL phases of the task (counted them at start, verified all present)
- [ ] I extracted BOTH Consolidated and Standalone where applicable
- [ ] I filled EVERY table cell (no blanks without "Not disclosed" note)
- [ ] I showed at least ONE sample calculation for verification
- [ ] I noted any gaps, inconsistencies, or [VERIFY] flags with explanation
- [ ] Output length is substantial (8-20 pages for complex tasks)
- [ ] I completed the task's verification checklist at the end

**If ANY checkbox above is unchecked, OUTPUT IS INCOMPLETE. Fix before submitting.**

--
**Summary:**
- Upload all ~65 documents to NotebookLM
- Execute 7 deep extraction prompts
- Generate 7 structured intelligence files
- Time: 20-30 minutes | Cost: FREE

**Outputs:**
1. `01_notebooklm_document_map.txt`
2. `02_notebooklm_financial_tables.txt`
3. `03_notebooklm_accounting_policies.txt`
4. `04_notebooklm_event_timeline.txt`
5. `05_notebooklm_rpt_subsidiaries.txt`
6. `06_notebooklm_guidance_tracker.txt`
7. `07_notebooklm_red_flags_prescreened.txt`

---

## STAGE 2 — GEMINI DEEP RESEARCH

**Go to:** [engine_00B__qtrly_results_audit_gemini_dr.md](engine_00B__qtrly_results_audit_gemini_dr.md)

**Summary:**
- Use Gemini Advanced Deep Research feature
- Execute 3 sector research queries
- Generate comprehensive sector intelligence
- Time: 25-40 minutes | Cost: FREE (with Gemini Advanced)

**Outputs:**
1. Sector Overview Report
2. Peer Benchmarking Report
3. Regulatory Landscape Report
4. `MASTER_Sector_Intelligence_[Sector].md` (combined)

---

## STAGE 3 — CLAUDE OPUS 4.5

**Go to:** [engine_00C__qtrly_results_audit_opus.md](engine_00C__qtrly_results_audit_opus.md)

**Summary:**
- Use Antigravity IDE with Opus 4.5 Extended Thinking
- Attach all 18+ files (Stage 1 + Stage 2 outputs + originals)
- Execute comprehensive forensic prompt
- Generate 13-section institutional report
- Time: 20-30 minutes | Cost: $6-8

**Output:**
- `ENGINE17_[Company]_[Quarter]_FINAL.md` (8,000-12,000 words)

---

## OUTPUT DIRECTORY STRUCTURE

```
/Output/Qtrly_results/[Company_Name]/[Quarter]_[Year]/
├── 00_Source_Documents/
│   └── (All original PDFs)
│
├── 01_Stage1_NotebookLM_Outputs/
│   ├── 01_notebooklm_document_map.txt
│   ├── 02_notebooklm_financial_tables.txt
│   ├── 03_notebooklm_accounting_policies.txt
│   ├── 04_notebooklm_event_timeline.txt
│   ├── 05_notebooklm_rpt_subsidiaries.txt
│   ├── 06_notebooklm_guidance_tracker.txt
│   └── 07_notebooklm_red_flags_prescreened.txt
│
├── 02_Stage2_Gemini_Outputs/
│   ├── Sector_Overview_[Sector].md
│   ├── Peer_Benchmarking_[Sector].md
│   ├── Regulatory_Landscape_[Sector].md
│   └── MASTER_Sector_Intelligence_[Sector].md
│
├── 03_Stage3_Opus_Analysis/
│   └── ENGINE17_[Company]_[Quarter]_FINAL.md
│
└── 04_Logs/
    └── ENGINE17_execution_log_[Company]_[Quarter].txt
```

---

## QUALITY GATES

**All reports must pass 4 gates before routing to ENGINE 05:**

### Gate 1: Completeness
- [ ] All 13 mandatory sections present
- [ ] Metadata block complete
- [ ] Uncertainty note at end
- [ ] Word count: 6,000-15,000
- [ ] Both Cons AND SA analyzed

### Gate 2: Evidence Standards
- [ ] All numbers have source citations
- [ ] Spot-check 10 random numbers (8/10 must match source)
- [ ] No assumptions stated as facts
- [ ] [VERIFY] flags noted where needed

### Gate 3: Neutrality & Compliance
- [ ] No buy/sell/hold recommendations
- [ ] No price targets
- [ ] No banned AI phrases (navigate, tapestry, delve, holistic)
- [ ] No fraud accusations without proof
- [ ] Positives AND negatives covered

### Gate 4: Voice & Readability
- [ ] "We" voice used consistently
- [ ] Natural prose (not bullet-heavy)
- [ ] Minimal formatting (bold only for key items)
- [ ] Jargon defined on first use

**Pass Threshold:** All 4 gates must pass before ENGINE 05 routing.

---

## EXECUTION LOG TEMPLATE

```
ENGINE 17 EXECUTION LOG
========================

Company: [Name]
Sector: [Sector]
Quarter: [QX FYXX]
Date: [DD-MMM-YYYY]

STAGE 0 (Kimi): [Start] - [End] | [X] min | [X] docs fetched
STAGE 1 (NotebookLM): [Start] - [End] | [X] min | 7 files generated
STAGE 2 (Gemini DR): [Start] - [End] | [X] min | 4 files generated  
STAGE 3 (Opus): [Start] - [End] | [X] min | Report: [X] words

TOTAL TIME: [X] minutes
TOTAL COST: $[X]

QUALITY GATES:
- Gate 1 (Completeness): [PASS/FAIL]
- Gate 2 (Evidence): [PASS/FAIL]
- Gate 3 (Neutrality): [PASS/FAIL]
- Gate 4 (Voice): [PASS/FAIL]

STATUS: [Ready for ENGINE 05 / Requires Fixes]

NOTES:
- [Any issues or learnings]
```

---

## FINAL REMINDERS

### Critical Success Factors

1. **Verify NotebookLM outputs** before using in Stage 3
2. **Maintain clean directory structure** for audit trail
3. **Monitor Opus thinking** — if brief (<500 words), may need more depth
4. **Never skip quality gates** — at minimum run Gates 1-3
5. **Always route to ENGINE 05** before publishing

### Monthly Production Capacity

| Metric | Value |
|--------|-------|
| Time per company | ~90 minutes |
| Monthly capacity | 20-25 companies |
| Cost per company | $6-8 |
| Monthly cost | $120-200 |
| Output | 120,000-300,000 words |

### When to Use Kimi vs NotebookLM

| Use Kimi | Use NotebookLM |
|----------|----------------|
| Document count >50 | Default for all other cases |
| Non-English documents | Best accuracy |
| Need faster processing | Superior citations |

---

## NEXT STEPS AFTER COMPLETION

1. **Route to ENGINE 05** — Data Verification (Red Team)
2. **Manual review** by senior analyst
3. **Publish** after all verifications pass
4. **Archive** all intermediate files

---

## RELATED FILES

- [Niveshak Bible](../00-bible/niveshak_bible.md) — Voice, tone, banned phrases
- [Frameworks Index](../00-bible/frameworks_index.md) — Sector-specific frameworks
- [Operating System](../00-bible/niveshak_operating_system_v1.md) — Full engine architecture

---

**END OF ENGINE 00 — QUARTERLY FORENSIC RESEARCH ENGINE (APEX MODE v1.1)**