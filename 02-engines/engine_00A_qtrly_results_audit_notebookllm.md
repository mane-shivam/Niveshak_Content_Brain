# ENGINE 00A — NOTEBOOKLLM DOCUMENT INTELLIGENCE STAGE

> **Stage 1 of 3** in the Quarterly Results Audit Pipeline  
> **Model**: NotebookLM (Google)  
> **Platform**: notebooklm.google.com
---

---

## Input Files (Upload to NotebookLM)

**Upload ALL available documents to the notebook:**

| Category | Documents | Priority |
|----------|-----------|----------|
| Quarterly Results | Q1-Q4 for FY20-FY25 (Cons + SA) | Required |
| Earnings Transcripts | Concall transcripts for all quarters | Required |
| Investor Presentations | Quarterly investor decks | Recommended |
| Annual Reports | FY20-FY24 complete AR | Required |
| Credit Ratings | Rating reports (CRISIL, ICRA, etc.) | Optional |
| Other Filings | DRHP, scheme documents, notices | Optional |

**File naming convention**: Use clear names like `Q3_FY25_Results_Consolidated.pdf`

---

## Execution Protocol

1. **Create notebook**: Name it `[CompanyName]_Forensic_Analysis_[Date]`
2. **Upload all documents** (can take 5-10 minutes for large sets)
3. **Wait for processing** (NotebookLM needs time to index)
4. **Run each prompt sequentially** (7 prompts total)
5. **Save each output** to designated file
6. **Verify completeness** before proceeding

---

## Prompts Overview

| Prompt | Task | Expected Output |
|--------|------|-----------------|
| 1 | Document Inventory & Mapping | Complete source list |
| 2 | Financial Data Extraction | 5-year tables (Cons + SA) |
| 3 | Accounting Policy Changes | Policy change log |
| 4 | Event Timeline | Chronological events |
| 5 | RPT & Subsidiaries | Related party analysis |
| 6 | Guidance Tracker | Management credibility |
| 7 | Red Flags Pre-screening | Alert system |

---


## **Task Starter Prompt: Paste this every time with updated task number**

```markdown
Now execute llm_task_02. 
MUST: READ Forensic Financial Analysis and Engine 00A Mandatory Operating Rules (attached in sources) & follow it by heart

```


## **Task Starter Prompts: Paste this every time in source & name it - Forensic Financial Analysis and Engine 00A Mandatory Operating Rules **

```markdown

# CRITICAL INSTRUCTIONS - READ BEFORE EXECUTING

You are functioning as a FORENSIC FINANCIAL ANALYST executing a task from ENGINE 00A, 
an institutional-grade equity research framework used for investment decisions.

---

## MANDATORY OPERATING RULES (NON-NEGOTIABLE)

### RULE 1: COMPLETE EXECUTION
- Execute EVERY phase listed in the task document sequentially
- Phase 1 → Phase 2 → Phase 3... in exact order
- DO NOT skip any phase, even if it seems repetitive
- DO NOT summarize multiple phases into one
- State at start: "This task has [X] phases. Beginning Phase 1..."
- State after each phase: "Phase [X] complete. [Y] phases remaining."

### RULE 2: EXHAUSTIVE DATA EXTRACTION
- Extract EVERY line item from tables (not summaries)
- Extract ALL periods requested (not just recent 3-5)
- Extract BOTH Consolidated AND Standalone where both exist
- If a table has 40 rows, your output must have 40 rows
- If a task requests 20 quarters, extract all 20 (not 5-10)
- DO NOT use phrases like "continue for remaining..." without actually continuing

### RULE 3: PERFECT SOURCE CITATIONS
- EVERY number must have exact citation in this format:
  [Filename.pdf, Page X, Table: "Table Name", Line: "Line Item Name"]
- Example: [Consolidated_Sebi_Results_Q3_FY26.pdf, Page 1, 
  Table: "Unaudited Consolidated Statement of Profit & Loss", 
  Line 4: "Cost of Materials Consumed"]
- Vague citations like "From quarterly results" are UNACCEPTABLE
- Before outputting, verify: Can someone find this exact number using my citation?

### RULE 4: SHOW YOUR WORK
- For any calculation, show the complete formula and steps:
  GOOD: "EBITDA = PBT (₹539.91) + Finance Costs (₹31.62) + Depreciation (₹159.29) 
         = ₹730.82 cr [Sources: PDF1 Page 1 Line 14, Line 8, Line 9]"
  BAD: "EBITDA = ₹730.82 cr"
- Show at least ONE sample calculation per phase for verification

### RULE 5: HANDLE MISSING DATA EXPLICITLY
- If data not found after thorough search:
  State: "[Data Item] NOT FOUND. Checked: [List of 3-5 documents/pages checked]. 
  Possible reasons: 1) Not disclosed by company, 2) Different naming convention, 
  3) Aggregated under different line item."
- DO NOT leave cells blank without explanation
- DO NOT write "Not disclosed" without showing what you checked
- If truly unavailable, mark as: "[UNAVAILABLE: Checked Sources 11, 15, 42 - not disclosed]"

### RULE 6: VERIFICATION CHECKPOINT
Every task document has a verification checklist at the end.
Before considering task complete:
- Complete the checklist
- For EACH checkbox:
  - If ✅: Provide brief evidence ("Extracted 20 quarters from Sources 11-30")
  - If ❌: State exactly what's missing and why ("Phase 7 incomplete: 
    Only calculated 5 ratios instead of required 8. Reason: [explain]")
- DO NOT mark all boxes checked without actual verification

### RULE 7: QUALITY OVER SPEED
- Thoroughness is the PRIMARY success metric
- Taking 10-15 minutes to execute a task with 95% accuracy is BETTER than 
  2 minutes with 60% accuracy
- If execution requires 20+ pages of tables, that is expected and correct
- DO NOT compress output to save space unless explicitly instructed

### RULE 8: FLAG ISSUES PROACTIVELY
If you encounter ANY of these situations, STOP and explicitly state the issue:
- ❌ "Required document not found in uploaded sources"
- ❌ "Table structure in document differs from expected format"
- ❌ "Cannot complete Phase X due to: [specific reason]"
- ❌ "Found conflicting data: Source 11 shows ₹5,112 cr but Source 15 shows ₹5,120 cr"
- ❌ "Partial data only: Found 12 of 20 requested quarters"

DO NOT proceed silently with partial/incorrect execution. Flag for manual review.

---

## EXECUTION PROTOCOL

### BEFORE STARTING:
1. Read the attached task document completely
2. Count total phases: "This task requires [X] phases"
3. Identify required sources: "Will need to access Sources: [list numbers/names]"
4. Estimate: "Expected output length: [X] pages"

### DURING EXECUTION:
1. Execute phases sequentially (no skipping)
2. For each phase, output section header: "## PHASE [X]: [Phase Name]"
3. After completing each phase: "✅ Phase [X] complete. Evidence: [brief proof]"
4. If stuck: "⚠️ Phase [X] issue: [describe problem]. Awaiting guidance."

### AFTER COMPLETION:
1. Output: "## VERIFICATION CHECKLIST"
2. Check EVERY box in task's checklist
3. Provide evidence or gap explanation for each
4. Final statement: "Task [X] execution complete. [Y] phases executed. 
   [Z] issues flagged for review."

---

## CRITICAL REMINDERS

✅ DO:
- Read EVERY source document mentioned
- Extract ALL line items (not highlights)
- Cite EVERY number with exact location
- Complete ALL phases (not partial)
- Show verification checklist with evidence
- Flag issues explicitly for manual review

❌ DO NOT:
- Skip phases to save time
- Summarize when extraction is requested
- Use vague citations ("from results")
- Leave blanks without "NOT FOUND" explanation
- Mark checklist complete without verification
- Hide problems or partial execution

---

## ACKNOWLEDGMENT REQUIRED

Before executing the task, respond:

"✅ INSTRUCTIONS ACKNOWLEDGED

Task: [Task Number/Name]
Total Phases: [X]
Required Sources: [List key source types]
Estimated Time: [X] minutes
Expected Output Length: [Y] pages

Beginning Phase 1..."

---

NOW: Read the attached task document and execute following these rules.
```


## **DEEP PROMPT SET (PRODUCTION-READY)**

### **TASK 1: DOCUMENT INVENTORY (DEEP VERSION)**

```markdown
# TASK 1: DOCUMENT INVENTORY & MAPPING (COMPREHENSIVE)

## OBJECTIVE
Create a complete audit trail of all sources available in this notebook.

---

## PHASE 1: SOURCE IDENTIFICATION

List EVERY source in this notebook in table format:

| # | Document Name (Exact) | Document Type | Period Covered | File Format | Page Count | Source URL (if applicable) |
|---|----------------------|---------------|----------------|-------------|------------|---------------------------|
| 1 | Q3_FY26_Results.pdf | Quarterly Results | Q3 FY26 (Oct-Dec 2025) | PDF | [X] pages | [URL or "Uploaded file"] |
| 2 | Q3_FY26_Transcript.pdf | Earnings Call | Q3 FY26 | PDF | [X] pages | [URL] |
| [Continue for ALL sources...] |

**DO NOT group** - list every single file individually.

---

## PHASE 2: FINANCIAL STATEMENT COVERAGE

For each source that contains financial statements, identify:

| Source # | Consolidated Present? | Standalone Present? | Statements Included | Notes Section Present? | Auditor Report Present? |
|----------|----------------------|---------------------|---------------------|------------------------|-------------------------|
| 1 (Q3_FY26_Results.pdf) | ✅ Yes (Page [X]) | ✅ Yes (Page [Y]) | P&L, BS, CF | ✅ Yes (Note 1-25, Pages [X-Y]) | ❌ No (Quarterly, unaudited) |
| [Continue...] |

---

## PHASE 3: COMPLETENESS CHECK

**Required Coverage: Last 20 Quarters (Q4 FY21 - Q3 FY26)**

Create checklist:

| Quarter | Results (Cons) | Results (SA) | Transcript | Presentation | Status |
|---------|---------------|--------------|------------|--------------|--------|
| Q3 FY26 | ✅ [Source #] | ✅ [Source #] | ✅ [Source #] | ✅ [Source #] | ✅ Complete |
| Q2 FY26 | ✅ [Source #] | ✅ [Source #] | ✅ [Source #] | ❌ Missing | ⚠️ Partial |
| Q1 FY26 | ✅ [Source #] | ✅ [Source #] | ❌ Missing | ✅ [Source #] | ⚠️ Partial |
| [Continue for all 20 quarters...] |

**Summary:**
- Quarters with COMPLETE data (Results + Transcript + Presentation): [X/20]
- Quarters with Results ONLY: [Y/20]
- Missing quarters: [List any quarters with NO data]

---

## PHASE 4: ANNUAL REPORT COVERAGE

**Required: Last 5 fiscal years (FY21-FY25)**

| Fiscal Year | Full Annual Report Present? | Source # | Page Count | Auditor Opinion Page | MD&A Section Pages |
|-------------|----------------------------|----------|------------|---------------------|-------------------|
| FY25 | ✅ Yes / ❌ No (but year-end results available) | [#] | [X] | Page [Y] | Pages [A-B] |
| [Continue...] |

---

## PHASE 5: GAPS & WORKAROUNDS

**Identified Gaps:**

1. **Missing Documents:**
   - Quarter: [X]
   - What's missing: [Results/Transcript/Presentation]
   - Impact: [e.g., "Cannot extract management commentary for Q1 FY25"]
   - Workaround: [e.g., "Use investor presentation text as proxy" or "Skip that quarter"]

2. [List all gaps...]

**Data Availability Score:**
- Current Quarter (Q3 FY26): [Complete / Partial / Incomplete]
- Historical Coverage (Q4 FY21 - Q2 FY26): [X%] complete (Y/19 quarters fully covered)
- Annual Reports: [X/5] available

**Recommendation:**
- Can proceed with ENGINE 17: [✅ Yes / ⚠️ Yes with noted limitations / ❌ No, insufficient data]
- Limitations to note in final report: [List]

---

## PHASE 6: DOCUMENT QUALITY NOTES

For each source, assess:

| Source # | Document Name | Quality Issue (if any) | Impact |
|----------|---------------|------------------------|--------|
| 5 | Q2_FY24_Results.pdf | Scanned PDF, OCR quality poor (text not searchable cleanly) | May need manual verification of numbers |
| 12 | Q4_FY23_Transcript.pdf | Timestamp format inconsistent (some MM:SS, some not) | Citation will use page numbers only |
| [List ALL quality issues...] |

---

**OUTPUT:** Present all 6 phases sequentially. This is your audit trail for Stage 1.
```

---

### **TASK 2: FINANCIAL EXTRACTION (DEEP VERSION)**

```markdown
# TASK 2: CONSOLIDATED & STANDALONE FINANCIAL DATA EXTRACTION (FORENSIC DEPTH)

## OBJECTIVE
Extract COMPLETE financial statements (Cons & SA) for last 20 quarters + last 5 annual years.

**Target Documents:**
- Quarterly Results: Q4 FY21 through Q3 FY26 (20 quarters)
- Annual Results: FY21, FY22, FY23, FY24, FY25 (5 years)

---

## PHASE 1: CONSOLIDATED INCOME STATEMENT (QUARTERLY)

For EACH of the last 20 quarters, extract ALL line items from Consolidated P&L:

### REVENUE SECTION

| Quarter | Revenue from Operations | Other Income | ├─ Interest Income | ├─ Dividend | ├─ Forex Gain/(Loss) | ├─ Other | Total Income | Source Citation (PDF, Page, Line) |
|---------|------------------------|--------------|-------------------|------------|---------------------|----------|--------------|----------------------------------|
| Q3 FY26 | | | | | | | | |
| Q2 FY26 | | | | | | | | |
| Q1 FY26 | | | | | | | | |
| [Continue for all 20 quarters...] |

**Instructions:**
1. Open each quarterly result PDF
2. Find "Consolidated Statement of Profit & Loss" (note exact page)
3. Extract EXACT numbers as printed (₹ in crores unless stated otherwise)
4. If "Other Income" is NOT broken down, write "Not disclosed"
5. Cite: [Document name], Page [X], Section: "Consolidated P&L", Line: "[Exact line item name]"

### EXPENSE SECTION

| Quarter | Cost of Materials | Employee Costs | Finance Costs (Interest) | Depreciation & Amort | Other Expenses | Total Expenses | Source |
|---------|------------------|---------------|-------------------------|---------------------|----------------|----------------|--------|
| Q3 FY26 | | | | | | | |
| [Continue...] |

### PROFITABILITY

| Quarter | PBT | Tax Expense | ├─ Current Tax | ├─ Deferred Tax | PAT | Minority Interest | PAT (after MI) | EPS (₹) | Source |
|---------|-----|-------------|---------------|----------------|-----|------------------|----------------|---------|--------|
| Q3 FY26 | | | | | | | | | |
| [Continue...] |

### EXCEPTIONAL ITEMS (if disclosed)

| Quarter | Exceptional Item Description | Amount (₹ cr) | Nature (Income/Expense) | Explanation from Notes | Source |
|---------|----------------------------|--------------|------------------------|------------------------|--------|
| Q3 FY26 | [e.g., "Gain on asset sale" or "None"] | | | | |
| [Continue...] |

---

## PHASE 2: STANDALONE INCOME STATEMENT (QUARTERLY)

**Same structure as Phase 1, but for Standalone financials.**

[Repeat all tables above with "Standalone" data]

**If Standalone not disclosed for any quarter:** Mark entire row as "Standalone not reported for [Quarter]"

---

## PHASE 3: BALANCE SHEET (CONSOLIDATED - Last 5 Years Annual)

| Year | Fixed Assets (Net) | Capital WIP | Investments (Non-Current) | Other Non-Current Assets | Inventories | Trade Receivables | Cash & Equivalents | Other Current Assets | **TOTAL ASSETS** | Source |
|------|-------------------|-------------|--------------------------|-------------------------|-------------|------------------|-------------------|---------------------|------------------|--------|
| FY25 | | | | | | | | | | |
| FY24 | | | | | | | | | | |
| [Continue...] |

| Year | Debt (Non-Current) | Other NC Liabilities | Debt (Current) | Trade Payables | Other Current Liabilities | **Total Liabilities** | Equity Capital | Reserves | **Total Equity** | Net Worth | Source |
|------|-------------------|---------------------|---------------|---------------|--------------------------|---------------------|---------------|---------|-----------------|-----------|--------|
| FY25 | | | | | | | | | | | |
| [Continue...] |

---

## PHASE 4: BALANCE SHEET (STANDALONE - Last 5 Years Annual)

[Same structure as Phase 3]

---

## PHASE 5: CASH FLOW STATEMENT (CONSOLIDATED - Last 5 Years Annual)

| Year | Cash from Operations (CFO) | ├─ PAT | ├─ Depreciation | ├─ Working Capital Change | ├─ Interest Paid | ├─ Tax Paid | Cash from Investing (CFI) | ├─ Capex | ├─ Investments | Cash from Financing (CFF) | ├─ Debt Raised | ├─ Debt Repaid | ├─ Dividends Paid | Net Change in Cash | Opening Cash | Closing Cash | Source |
|------|----------------------------|---------|----------------|--------------------------|-----------------|------------|--------------------------|----------|---------------|--------------------------|---------------|---------------|------------------|-------------------|--------------|--------------|--------|
| FY25 | | | | | | | | | | | | | | | | | |
| [Continue...] |

**Calculate:** Free Cash Flow (FCF) = CFO - Capex

| Year | CFO | Capex | Free Cash Flow | FCF/PAT Ratio | Source |
|------|-----|-------|---------------|---------------|--------|
| FY25 | | | | | |
| [Continue...] |

---

## PHASE 6: CASH FLOW STATEMENT (STANDALONE - Last 5 Years Annual)

[Same structure as Phase 5]

---

## PHASE 7: KEY RATIOS (CONSOLIDATED - Last 20 Quarters)

Calculate using extracted data:

| Quarter | Revenue Growth YoY % | Revenue Growth QoQ % | Gross Margin % | EBITDA Margin % | PAT Margin % | ROE % | ROCE % | Debt/Equity | Interest Coverage | Receivables Days | Inventory Days | Payables Days | Cash Conversion Cycle | Source for Calc |
|---------|---------------------|---------------------|---------------|----------------|-------------|-------|-------|------------|------------------|-----------------|---------------|--------------|---------------------|----------------|
| Q3 FY26 | | | | | | | | | | | | | | |
| [Continue...] |

**Show ONE full calculation (Q3 FY26 example):**

EBITDA = PBT + Interest + Depreciation
       = ₹563 cr + ₹[X] cr + ₹[Y] cr
       = ₹[Z] cr

EBITDA Margin % = (EBITDA / Revenue) × 100
                = (₹[Z] / ₹5,112) × 100
                = [__]%

Receivables Days = (Trade Receivables / Revenue) × 90
                 = (₹[A] / ₹5,112) × 90
                 = [__] days

---

## PHASE 8: KEY RATIOS (STANDALONE - Last 20 Quarters)

[Same structure as Phase 7]

---

## PHASE 9: CONSOLIDATED vs STANDALONE GAP ANALYSIS (Last 5 Years Annual)

Calculate gaps for key metrics:

| Year | **Revenue (Cons)** | **Revenue (SA)** | **Gap (₹ cr)** | **Gap %** | **Interpretation** | Source |
|------|-------------------|------------------|---------------|-----------|-------------------|--------|
| FY25 | 17,618 | 12,802 | 4,816 | 27.3% | Subsidiaries (intl ops + Starbucks) contribute 27% of Cons revenue | [Cite both] |
| [Continue...] |

| Year | **PAT (Cons)** | **PAT (SA)** | **Gap (₹ cr)** | **Gap %** | **Interpretation** | Source |
|------|---------------|--------------|---------------|-----------|-------------------|--------|
| FY25 | 1,287 | [X] | [Y] | [Z%] | [If Gap positive: Subs add value / If negative: Subs destroy value] | |
| [Continue...] |

| Year | **ROE (Cons)** | **ROE (SA)** | **Gap (pp)** | **Interpretation** |
|------|---------------|--------------|-------------|-------------------|
| FY25 | [X%] | [Y%] | [Z pp] | [Are subs diluting or enhancing returns?] |
| [Continue...] |

---

## PHASE 10: SEGMENT PERFORMANCE (CONSOLIDATED - Last 5 Years)

If segment data is disclosed:

| Year | India Beverages Revenue | India Foods Revenue | International Revenue | Out-of-Home Revenue | Total Revenue | Source |
|------|------------------------|--------------------|--------------------|-------------------|---------------|--------|
| FY25 | | | | | | |
| [Continue...] |

| Year | India Beverages EBIT | India Foods EBIT | International EBIT | Out-of-Home EBIT | Segment EBIT Total | Source |
|------|---------------------|-----------------|-------------------|-----------------|-------------------|--------|
| FY25 | | | | | | |
| [Continue...] |

**Calculate Segment Margins:**

| Year | India Beverages Margin % | India Foods Margin % | International Margin % | Out-of-Home Margin % |
|------|-------------------------|---------------------|----------------------|---------------------|
| FY25 | | | | |
| [Continue...] |

---

## PHASE 11: VERIFICATION CHECKLIST

Before finalizing, verify:

- [ ] I extracted data from ALL 20 quarters (not just recent 5)
- [ ] I extracted BOTH Consolidated AND Standalone for every period where available
- [ ] I noted "Not disclosed" where Standalone is unavailable (not left blank)
- [ ] I cited EXACT source for EVERY number (PDF name + Page + Line item)
- [ ] I calculated ALL ratios (not left "-" unless data unavailable)
- [ ] I showed at least ONE full calculation as verification
- [ ] I extracted ALL expense line items (not just revenue/PAT)
- [ ] I noted ALL exceptional items (not skipped)
- [ ] I calculated Cons vs SA gaps for last 5 years
- [ ] I extracted segment data if disclosed

**If ANY box unchecked → GO BACK and complete.**

---

**OUTPUT:** All 11 phases. Estimated length: 15-20 pages of tables + citations.

DO NOT SUMMARIZE. Present complete data.
```

---

## **TASK 3: ACCOUNTING POLICY CHANGE DETECTION (DEEP VERSION)**

```markdown
# TASK 3: ACCOUNTING POLICY CHANGE DETECTION (FORENSIC DEPTH)

## OBJECTIVE
Create a complete log of ALL accounting policy changes, restatements, and methodology shifts over 5 years.

**Sources to Review:**
- Annual Results: FY21, FY22, FY23, FY24, FY25
- Quarterly Results: All 20 quarters (policy changes sometimes disclosed in quarterly notes)
- Search for: "Significant Accounting Policies" (typically Note 2), "Changes in Accounting Estimates", "Restatements", "Prior Period Items"

---

## PHASE 1: LOCATE ACCOUNTING POLICY SECTIONS

For each annual period:

| Year | Document Name | "Significant Accounting Policies" Found At | Note Number | Page Numbers | Other Policy Disclosures Found |
|------|---------------|------------------------------------------|-------------|--------------|-------------------------------|
| FY25 | [PDF name] | Page [X], Note [Y] | Note [Y] | Pages [X-Z] | [e.g., "Change in estimate disclosed in Note 18"] |
| FY24 | | | | | |
| FY23 | | | | | |
| FY22 | | | | | |
| FY21 | | | | | |

**If section not found:** State "Accounting Policies section not located in [Year] - cannot assess changes for this year"

---

## PHASE 2: IDENTIFY ALL SUB-POLICIES

From FY25 (most recent), list ALL accounting policy sub-sections:

| Policy Category | Note Sub-Section | Page Reference | Summary (1 sentence) |
|-----------------|-----------------|----------------|---------------------|
| Revenue Recognition | Note 2.1 | Page [X] | "Revenue recognized when control transfers to customer" |
| Depreciation & Amortization | Note 2.2 | Page [X] | "Straight-line method over useful life: Buildings 60Y, Plant 15Y, etc." |
| Inventory Valuation | Note 2.3 | Page [X] | "Lower of cost (FIFO) or net realizable value" |
| Employee Benefits | Note 2.4 | Page [X] | "Gratuity: Defined benefit plan, actuarial valuation" |
| Foreign Exchange | Note 2.5 | Page [X] | "Transactions at exchange rate on transaction date" |
| Consolidation | Note 2.6 | Page [X] | "Subsidiaries consolidated when control exists (>50% voting)" |
| Financial Instruments | Note 2.7 | Page [X] | "Classified as FVTPL, FVTOCI, or Amortized Cost per Ind AS 109" |
| Leases | Note 2.8 | Page [X] | "Right-of-use asset recognized per Ind AS 116" |
| [Continue for ALL policies...] | | | |

**Count:** Total sub-policies in FY25 = [X]

---

## PHASE 3: YEAR-OVER-YEAR POLICY COMPARISON

For EACH policy category, compare FY21 → FY25:

### **POLICY: DEPRECIATION & AMORTIZATION**

| Year | Useful Life - Buildings | Useful Life - Plant & Machinery | Useful Life - Furniture | Method | Any Changes Noted? | Source |
|------|------------------------|-------------------------------|------------------------|--------|-------------------|--------|
| FY25 | [X] years | [Y] years | [Z] years | Straight-line | ❌ No change / ✅ Changed from [old] | Note 2.2, Page [X] |
| FY24 | [X] years | [Y] years | [Z] years | Straight-line | | |
| FY23 | [X] years | [Y] years | [Z] years | Straight-line | | |
| FY22 | [X] years | [Y] years | [Z] years | Straight-line | | |
| FY21 | [X] years | [Y] years | [Z] years | Straight-line | | |

**Analysis:**
- Did useful lives change? [Yes/No]
- If Yes:
  - What changed: [From X years to Y years]
  - When: [FY__, Quarter__]
  - Direction: [Extension = Lower depreciation / Reduction = Higher depreciation]

[REPEAT THIS TABLE for EVERY policy category: Revenue Recognition, Inventory, Employee Benefits, etc.]

---

## PHASE 4: DETAILED CHANGE DOCUMENTATION

For EVERY policy change detected in Phase 3:

### **CHANGE LOG ENTRY #1**

**Policy Area:** [e.g., "Depreciation - Plant & Machinery"]

**What Changed:**
- **Old Policy (FY21-FY23):** "[Quote exact text from FY23 report]"
  - Source: [FY23 Annual Report, Note 2.2, Page 45]
- **New Policy (FY24 onwards):** "[Quote exact text from FY24 report]"
  - Source: [FY24 Annual Report, Note 2.2, Page 48]

**When Effective:**
- Disclosed in: [FY24 Annual Report / Q1 FY24 Results]
- Effective from: [April 1, 2023 / January 1, 2024]
- Applied: [Prospectively / Retrospectively with restatement]

**Management's Stated Reason:**
- "[Exact quote from disclosure, if provided]"
- Source: [Note X, Page Y]
- If no reason given: State "No reason disclosed"

**Quantified Impact (If Disclosed):**
- Impact on Depreciation: ₹[X] cr reduction in FY24
- Impact on PBT: ₹[Y] cr increase
- Impact on PAT: ₹[Z] cr increase (after tax)
- As % of reported PAT: [W]%
- Source: [Note X, Page Y]

**If Impact NOT Disclosed - Attempt to Calculate:**

Example calculation:
Gross Block of Plant & Machinery (FY24): ₹[A] cr
Old Rate: 1/10 years = 10%
New Rate: 1/15 years = 6.67%
Difference: 3.33%

Estimated depreciation reduction = ₹[A] cr × 3.33% = ₹[B] cr
Estimated PAT impact (assuming 25% tax) = ₹[B] × 0.75 = ₹[C] cr
As % of reported PAT = ([C] / [Reported PAT]) × 100 = [D]%

**Retrospective Restatement?**
- Were prior year figures restated? [Yes/No]
- If Yes: Which years restated? [FY23, FY22, FY21...]
- Magnitude of restatement: ₹[X] cr impact on FY23 PAT
- Source: [Note X showing "Restated figures"]

**Our Assessment:**

**CRITERION 1 - Business Justification:**
- Management reason: "[Quote or 'Not provided']"
- Does it make sense? [Yes/No + Why]
  - Example: "Extension from 10Y to 15Y justified if actual asset life is 18Y based on engineering study → REASONABLE"
  - Example: "No engineering assessment cited, change made during margin pressure period → QUESTIONABLE"

**CRITERION 2 - Timing Analysis:**
- Change made in: [Quarter/Year]
- Company performance context:
  - Prior period margin trend: [Expanding / Stable / Compressing]
  - If change made during margin compression: ⚠️ SUSPICIOUS TIMING
  - If change made proactively during strong period: ✅ LESS SUSPICIOUS

**CRITERION 3 - Industry Practice:**
- Did peers make similar changes in same timeframe? [Check if information available]
  - If available: "[Peer A, Peer B made similar change]" → ✅ ALIGNED
  - If not: "No peer precedent found" → ⚠️ COMPANY-SPECIFIC

**CRITERION 4 - Magnitude:**
- Impact on PAT: [<5% = Immaterial / 5-10% = Material / >10% = Highly Material]
- Impact on EBITDA margin: [<50bps = Low / 50-100bps = Moderate / >100bps = High]

**CRITERION 5 - Pattern & Reversibility:**
- Is this company's first policy change in 5 years? [Yes/No]
- If No: List other changes in last 5 years
- Has ANY policy been changed then REVERSED? [Yes/No - If yes: 🔴 RED FLAG]

**SEVERITY CLASSIFICATION:**

🔴 **CRITICAL CONCERN** if:
- Suspicious timing (during margin pressure) + High magnitude (>10% PAT impact) + No business justification + No peer precedent

🟠 **HIGH CONCERN** if:
- 2-3 of above criteria met OR Material magnitude (5-10%) with weak justification

🟡 **MEDIUM CONCERN** if:
- 1 concerning criterion + Moderate magnitude (5-10%)

🟢 **LOW / ACCEPTABLE** if:
- Strong business justification + Aligned with peers + Immaterial magnitude (<5%)

**Classification for this change:** [🔴/🟠/🟡/🟢]

**Reasoning:** [1-2 sentences explaining classification]

---

[REPEAT "CHANGE LOG ENTRY" FORMAT FOR EVERY CHANGE DETECTED]

---

## PHASE 5: RESTATEMENT TRACKING

Apart from policy changes, track any restatements due to:
- Prior period errors
- Reclassifications
- Mergers/acquisitions requiring retrospective application

| Year Restated | Item Restated | Original Figure | Restated Figure | Reason Given | Magnitude (%) | Source |
|---------------|---------------|----------------|----------------|--------------|--------------|--------|
| FY23 | Revenue | ₹[A] cr | ₹[B] cr | "Merger of Tata Coffee - pooling of interest method applied retrospectively" | [X]% | FY24 AR, Note 40, Page 120 |
| FY23 | PAT | ₹[C] cr | ₹[D] cr | [Same reason] | [Y]% | [Source] |
| [Continue...] | | | | | | |

**Restatement Pattern Analysis:**
- Total restatements in 5 years: [X]
- Most common reason: [M&A accounting / Error correction / Reclassification]
- Largest magnitude: [Describe biggest restatement and impact]

---

## PHASE 6: SPECIFIC POLICY SCRUTINY

### **6A: REVENUE RECOGNITION**

**Current Policy (FY25):**
- Method: [Quote exact method from note]
- Timing: When is revenue recognized? [At point of sale / Over time / Other]
- Any significant judgments disclosed? [Yes/No - if yes, quote]

**5-Year Comparison:**
- Has revenue recognition policy changed? [Yes/No]
- If Yes: [Complete Change Log Entry as per Phase 4]

**Red Flags to Check:**
- ❌ Change from "point in time" to "over time" recognition (could accelerate revenue)
- ❌ Change in "percentage of completion" estimates for long-term contracts
- ❌ Unbilled revenue or contract assets growing >20% YoY

### **6B: INVENTORY VALUATION**

**Current Policy (FY25):**
- Method: [FIFO / Weighted Average / Other]
- Lower of cost or NRV applied? [Yes/No]
- Obsolescence provisioning policy: [Quote if disclosed]

**5-Year Comparison:**
- Has inventory valuation changed? [Yes/No]
- If Yes: [Change Log Entry]

**Red Flags:**
- ❌ Change from FIFO to Weighted Average during rising input cost period (could inflate margins)
- ❌ Reduction in obsolescence provision rates

### **6C: EMPLOYEE BENEFITS (GRATUITY/PENSION)**

**Current Assumptions (FY25):**
- Discount rate: [X]%
- Salary escalation rate: [Y]%
- Mortality: [Which table used]
- Attrition: [Z]%

**5-Year Trend:**

| Year | Discount Rate | Salary Escalation | Impact on Liability | Source |
|------|--------------|------------------|-------------------|--------|
| FY25 | [X]% | [Y]% | | |
| FY24 | [X]% | [Y]% | | |
| [Continue...] | | | | |

**Analysis:**
- Discount rate trend: [Rising / Falling / Stable]
- If discount rate increased: Reduces liability, increases profit (one-time gain via OCI)
- If salary escalation reduced: Reduces liability
- **Red Flag:** Assumptions changed to reduce liability during weak profit years

---

## PHASE 7: MERGER/ACQUISITION ACCOUNTING

**M&A Events in 5 Years:**

| Event | Date | Accounting Method | Retrospective Application? | Impact on Prior Years | Source |
|-------|------|------------------|---------------------------|---------------------|--------|
| Tata Coffee Merger | Jan 1, 2024 | Pooling of Interests (Ind AS 103) | ✅ Yes - FY23 restated | FY23 revenue increased by ₹[X] cr | FY24 AR, Note 40 |
| NourishCo Amalgamation | Apr 1, 2024 | [Method] | [Yes/No] | [Impact] | [Source] |
| Capital Foods Acquisition | Feb 2024 | Purchase Method (Goodwill ₹[X] cr) | ❌ No | N/A (prospective) | [Source] |
| [Continue...] | | | | | |

**Accounting Quality Assessment:**
- Pooling of interest vs Purchase method: [Both are legitimate, but pooling avoids goodwill and inflates ROE]
- Goodwill recognized: Total ₹[X] cr as of FY25
- Goodwill impairment: Any impairment in 5 years? [Yes/No - if yes, amount and reason]

---

## PHASE 8: SUMMARY SCORECARD

**Total Accounting Policy Changes Detected:** [X]

**Breakdown by Severity:**
- 🔴 Critical: [X changes]
- 🟠 High: [Y changes]
- 🟡 Medium: [Z changes]
- 🟢 Low: [W changes]

**Most Concerning Change:**
- [Describe #1 red flag with brief reasoning]

**Overall Accounting Quality Grade:**

**Scoring:**
- 0 Critical + 0-1 High = **A (Excellent consistency)**
- 0 Critical + 2-3 High = **B+ (Good, minor concerns)**
- 1 Critical OR 4+ High = **B (Adequate, notable concerns)**
- 2+ Critical OR 5+ High = **C (Weak, earnings management indicators)**

**Grade:** [A / B+ / B / C]

**Reasoning:** [2-3 sentences explaining grade]

---

## PHASE 9: VERIFICATION CHECKLIST

- [ ] I reviewed accounting policies for ALL 5 years (FY21-FY25)
- [ ] I compared EVERY policy category year-over-year
- [ ] I extracted exact text (quoted) for any policy that changed
- [ ] I attempted to quantify impact (even if not disclosed by management)
- [ ] I assessed EACH change using 5 criteria (Justification, Timing, Industry, Magnitude, Pattern)
- [ ] I classified severity (🔴🟠🟡🟢) for each change
- [ ] I tracked all restatements separately
- [ ] I scrutinized revenue recognition, inventory, employee benefits specifically
- [ ] I documented all M&A accounting treatments
- [ ] I cited exact sources (Note number, Page) for every finding

**If ANY box unchecked → GO BACK and complete.**

---

**OUTPUT:** All 9 phases sequentially. Estimated length: 10-15 pages.

DO NOT skip details or summarize. This is forensic accounting analysis.
```

---

## **TASK 4: CHRONOLOGICAL EVENT TIMELINE (DEEP VERSION)**

```markdown
# TASK 4: COMPREHENSIVE EVENT TIMELINE (FORENSIC CHRONOLOGY)

## OBJECTIVE
Create an exhaustive, chronologically ordered timeline of ALL material events from FY21 through Q3 FY26.

**Definition of "Material Event":** Anything that could impact financials, strategy, operations, governance, or risk profile.

**Sources to Search:**
- All quarterly results (20 quarters) - check "Management Discussion" or "Notes" sections
- All transcripts (check for event mentions in prepared remarks + Q&A)
- All investor presentations (strategy slides, M&A announcements)
- Annual reports - Director's Report, MD&A, Notes

---

## PHASE 1: EVENT EXTRACTION (CATEGORY-WISE)

### **CATEGORY 1: MERGERS, ACQUISITIONS, DIVESTMENTS**

For each M&A event:

| Date (Exact or Quarter) | Event | Target Company | Deal Type | Deal Value (if disclosed) | Rationale (Management Quote) | Status (Announced/Completed/Integration Status) | Source |
|------------------------|-------|----------------|-----------|--------------------------|------------------------------|------------------------------------------------|--------|
| Jan 1, 2024 | Merger | Tata Coffee Limited | Inbound Merger (TCL into TCPL) | N/A (share swap) | "Consolidate coffee value chain" [Q4 FY24 Concall] | ✅ Completed, Integration ongoing | FY24 AR Note 40, Q4 FY24 Transcript p12 |
| Feb 2024 | Acquisition | Capital Foods (Ching's Secret) | 100% stake acquisition | ₹[X] cr (if disclosed) | "Enter ethnic foods, leverage distribution" | ✅ Completed, Front-end integrated in 3 days | Q4 FY24 Presentation Slide 15 |
| [Continue for EVERY M&A event in 5 years...] | | | | | | | |

**Total M&A Events:** [X acquisitions, Y mergers, Z divestments]

---

### **CATEGORY 2: CAPACITY EXPANSION & CAPEX**

| Date | Event | Location | Capacity Addition | Capex Amount | Expected Commissioning | Funding Source | Purpose/Product | Source |
|------|-------|----------|------------------|--------------|----------------------|----------------|----------------|--------|
| [Quarter/Year] | New manufacturing facility announced | [City, State] | [X tonnes/year OR X units/year] | ₹[Y] cr | [Quarter/Year] | Internal accruals / Term loan | [Product category] | [Source] |
| [Continue...] | | | | | | | | |

---

### **CATEGORY 3: PRODUCT LAUNCHES & CATEGORY ENTRIES**

| Date | Event | Brand/Product Name | Category | Strategic Significance | Initial Market Response (if disclosed) | Source |
|------|-------|-------------------|----------|----------------------|--------------------------------------|--------|
| Jan 2023 | Launched protein platform | Tata GoFit | Protein supplements | "Address ₹10,000 cr+ protein market" | "Positive early traction" [Q4 FY23 Concall] | Q3 FY23 Presentation, Q4 FY23 Transcript |
| [Continue...] | | | | | | |

---

### **CATEGORY 4: DISTRIBUTION & ROUTE-TO-MARKET**

| Date | Event | Description | Metric Impact | Target/Outcome | Source |
|------|-------|-------------|---------------|----------------|--------|
| FY24 | Reached 4 million outlets | Numeric distribution milestone achieved | 4M outlets (from ~3.5M prior) | Target was 4M - HIT | Q4 FY24 Concall |
| Q2 FY25 | Launched split routes in 50k+ towns | Separate routes for Tata brands vs acquired brands (Capital Foods) | Improved SKU focus | "Early days, promising" | Q2 FY25 Transcript p18 |
| [Continue...] | | | | | |

---

### **CATEGORY 5: MANAGEMENT & GOVERNANCE CHANGES**

| Date | Event | Person | Old Role → New Role | Reason (if disclosed) | Impact Assessment | Source |
|------|-------|--------|---------------------|---------------------|-------------------|--------|
| Oct 2024 | CFO retirement announced | L. Krishnakumar | CFO → Retired | "Completion of tenure" | Succession planning initiated | Q2 FY25 Results announcement |
| [Continue...] | | | | | | |

**Check for:**
- CEO/MD changes
- CFO changes
- Board appointments/resignations (especially independent directors)
- Auditor changes
- Key management personnel (COO, CTO, Business Unit Heads)

---

### **CATEGORY 6: REGULATORY & COMPLIANCE**

| Date | Event | Regulator | Nature | Impact | Company Response | Source |
|------|-------|-----------|--------|--------|------------------|--------|
| FY26 | Labour Codes notified | Government of India | 4 new labour codes (Wages, Social Security, etc.) | "Assessing impact - rules not yet notified" | Monitoring, no material impact expected | Q3 FY26 Results Notes |
| [Continue...] | | | | | | |

**Check for:**
- SEBI observations/actions
- Product recalls
- Quality/safety issues
- Import/export restrictions
- Tax disputes disclosed

---

### **CATEGORY 7: LEGAL & LITIGATION**

| Date | Event | Parties | Issue | Amount in Dispute | Status | Contingent Liability? | Source |
|------|-------|---------|-------|------------------|--------|---------------------|--------|
| [Date] | [Case filed/settlement] | TCPL vs [Party] | [Tax/IP/Contract/Other] | ₹[X] cr | [Pending/Decided] | [Yes - ₹Y cr / No] | [Note X, Page Y] |

---

### **CATEGORY 8: FINANCIAL ACTIONS**

| Date | Event | Type | Amount | Terms | Purpose/Use of Proceeds | Source |
|------|-------|------|--------|-------|------------------------|--------|
| [Date] | [Fundraising/Debt issuance] | [QIP/Rights/NCD/Term Loan] | ₹[X] cr | [Tenor, Coupon/Dilution] | [Capex/Acquisition/General Corporate] | [Source] |
| [Date] | Dividend declared | Final/Interim | ₹[X] per share | [Record date] | [Payout ratio Y%] | [Results/AR] |

**Check for:**
- Equity fundraising (QIP, rights, preferential)
- Debt issuance (bonds, NCDs, ECBs)
- Debt repayment (early closure, refinancing)
- Dividends (track payout ratio trend)
- Buybacks
- Credit rating changes

---

### **CATEGORY 9: STRATEGIC INITIATIVES**

| Date | Event | Description | Expected Impact | Status | Source |
|------|-------|-------------|----------------|--------|--------|
| Q2 FY25 | Entered Food Services (HORECA) channel | Pilot launch | "Tap institutional demand" | Pilot ongoing | Q2 FY25 Transcript |
| Q2 FY25 | Entered Pharma channel | Pilot for health/nutrition products | "Leverage specialized distribution" | Pilot ongoing | Q2 FY25 Transcript |
| FY22-FY24 | International structure simplification | Reduce entities from ~45 to ~25 | "Reduce complexity, improve efficiency" | ✅ Completed FY24 | Q3 FY22 Presentation, FY24 AR |

---

### **CATEGORY 10: ONE-TIME EVENTS & EXCEPTIONAL ITEMS**

| Date | Event | Nature | P&L Impact | Cash vs Non-Cash | Source |
|------|-------|--------|------------|------------------|--------|
| [Date] | Asset sale / Impairment / Restructuring charge | [Describe] | ₹[X] cr (Income/Expense) | [Cash/Non-cash] | [Results Note X] |

**Check notes for:**
- Gains on asset sales
- Impairment of goodwill/assets
- Restructuring charges
- VRS/severance costs
- Fire/natural disaster losses
- Insurance claims

---

### **CATEGORY 11: EXTERNAL FACTORS & COMPANY RESPONSE**

| Date | External Event | Impact on Company | Management's Stated Response | Quantified Impact (if disclosed) | Source |
|------|----------------|------------------|----------------------------|--------------------------------|--------|
| Q1 FY25 | Heatwave in North India | Lower Out-of-Home consumption (NourishCo impact) | "Weather impact on beverages, expected to normalize" | [Revenue impact ₹X cr or Y%] | Q1 FY25 Concall |
| Q3 FY26 | Coffee prices at 50-year high | Margin pressure | "Implementing 10-13% price increases" | Arabica $3.40/lb, Robusta $5,400/tonne | Q3 FY26 Transcript p5 |

**Track:**
- Commodity price shocks (tea, coffee, raw materials)
- Regulatory changes (GST, labour laws, packaging norms)
- Pandemic impacts (if any residual effects post-FY21)
- Climate events (drought, floods, heatwaves)
- Competitive actions (if disclosed)

---

## PHASE 2: CHRONOLOGICAL MASTER TIMELINE

Take ALL events from Phase 1 (all 11 categories) and organize CHRONOLOGICALLY from oldest to newest:

**FORMAT:**

---

**[DATE: Q1 FY21 / April-June 2020]**

**EVENT #1: [Event Title]**
- **Category:** [M&A / Capacity / Product / Governance / etc.]
- **Description:** [2-3 sentences]
- **Key Details:**
  - [Bullet point 1]
  - [Bullet point 2]
- **Quantified Impact:** ₹[X] cr / [Y]% / [Z metric]
- **Source:** [Document name, Page, Section]
- **Significance:** [Material / Moderate / Minor]

**EVENT #2: [Event Title]**
[Same format]

---

**[DATE: Q2 FY21 / July-September 2020]**

[Continue chronologically through Q3 FY26...]

---

## PHASE 3: EVENT CLUSTERING ANALYSIS

After creating chronological timeline, analyze patterns:

### **3A: High-Activity Periods**

| Quarter | Event Count | Event Categories | Assessment |
|---------|-------------|-----------------|------------|
| Q4 FY24 | 8 events | 3 M&A (Tata Coffee, Capital Foods, Organic India), 2 Product launches, 1 Management change, 2 Strategic initiatives | 🔴 INTENSE - Major transformation quarter |
| [Continue for quarters with >5 events...] | | | |

**Interpretation:** Periods with >5 material events often indicate transformation phases, integration challenges, or strategic pivots.

---

### **3B: Event Sequences (Cause & Effect)**

Identify events that are linked:

**SEQUENCE #1: Coffee Consolidation Strategy (FY24)**
1. **Jan 2024:** Tata Coffee merger (plantation + extraction business brought into TCPL)
2. **Feb 2024:** Acquired Capital Foods (food brands)
3. **Mar 2024:** Announced integration plan (single sales team, shared distribution)
4. **Q1 FY25:** Reported "3-day front-end integration" success
5. **Q2-Q3 FY25:** Margin improvement from scale benefits

**Linkage:** Strategic theme of consolidation and scale-building in coffee/foods.

[Identify 3-5 such sequences in 5-year history]

---

### **3C: Management's Priority Evolution**

Track what management emphasized in each period:

| Period | Top 3 Priorities (from Concalls/Presentations) | Actions Taken | Follow-Through? |
|--------|-----------------------------------------------|--------------|----------------|
| FY22 | 1. Simplify international structure 2. Build distribution (4M target) 3. Grow "Growth businesses" | 1. Entity reduction initiated 2. Distribution expansion ongoing 3. Soulfull acquired | ✅ All followed through |
| FY23 | 1. Protein entry 2. Reach 4M outlets 3. Margin expansion | 1. ✅ Tata GoFit launched 2. ✅ 4M achieved FY24 3. ⚠️ Mixed (commodity volatility) | Strong follow-through |
| [Continue for each year...] | | | |

**Consistency Score:** [High / Medium / Low]
- High: Priorities stated → Actions taken → Results delivered
- Medium: Priorities stated → Actions taken → Mixed results
- Low: Priorities stated → Actions not taken OR Results not delivered

---

## PHASE 4: M&A INTEGRATION TRACKING

For EACH acquisition/merger in last 5 years:

| Acquisition | Date Announced | Date Completed | Initial Integration Timeline Stated | Actual Integration Status | Synergy Target (if stated) | Synergy Achieved (if disclosed) | Current Assessment |
|-------------|----------------|----------------|-----------------------------------|--------------------------|--------------------------|------------------------------|-------------------|
| Tata Coffee | [Date] | Jan 1, 2024 | "18-24 months" | "Back-end ongoing, front-end complete" (as of Q3 FY26) | "₹[X] cr cost synergies" OR "Not disclosed" | [Disclosed or "Not quantified"] | ✅ On track / ⚠️ Delayed / 🔴 Issues |
| Capital Foods | Feb 2024 | Feb 2024 | "Front-end: 3 days, Back-end: 12-18 months" | "Front-end done (3 days), back-end in progress" | [Quote] | [Status] | [Assessment] |

**Integration Red Flags:**
- ⚠️ If management stops mentioning an acquisition after 2-3 quarters → Integration issues or underperformance
- ⚠️ If integration timeline repeatedly extended → Execution challenges
- 🔴 If acquired entity's performance not disclosed separately after 1 year → Possible underperformance being masked

---

## PHASE 5: COMPETITIVE ACTIONS & MARKET DYNAMICS

From transcripts and presentations, extract mentions of competitive landscape:

| Quarter | Competitive Observation | Company's Response | Outcome (if disclosed later) | Source |
|---------|-------------------------|-------------------|----------------------------|--------|
| Q3 FY25 | "Local players aggressive on pricing during tea deflation" | "Maintained pricing, accepted 20 bps market share loss" | Market share recovered in Q3 FY26 | Q3 FY25 Transcript, Q3 FY26 Transcript |
| [Continue...] | | | | |

---

## PHASE 6: SUMMARY STATISTICS

**Event Count by Category (5 Years):**
- M&A: [X] (Acquisitions: Y, Mergers: Z, Divestments: W)
- Capacity/Capex: [X]
- Product Launches: [X]
- Management Changes: [X]
- Regulatory: [X]
- Legal: [X]
- Financial Actions: [X]
- Strategic Initiatives: [X]
- One-Time Events: [X]
- External Factors: [X]

**Total Material Events:** [X]

**Most Active Year:** [FYXX with Y events]

**Most Transformative Event:** [Event name - brief reasoning why]

**Top 5 Events by Long-Term Impact:**
1. [Event] - [Why important]
2. [Event] - [Why important]
3. [Event] - [Why important]
4. [Event] - [Why important]
5. [Event] - [Why important]

---

## PHASE 7: VERIFICATION CHECKLIST

- [ ] I extracted events from ALL 20 quarters (not just recent)
- [ ] I checked ALL transcripts for event mentions (prepared remarks + Q&A)
- [ ] I checked ALL investor presentations for strategy/M&A announcements
- [ ] I checked annual reports for governance changes, legal issues
- [ ] I classified EVERY event into one of 11 categories
- [ ] I organized events chronologically (oldest to newest)
- [ ] I cited exact source for EVERY event (document, page/timestamp)
- [ ] I assessed significance (Material/Moderate/Minor) for each event
- [ ] I identified event clusters and sequences
- [ ] I tracked M&A integration status for all acquisitions

**If ANY box unchecked → GO BACK and complete.**

---

**OUTPUT:** All 7 phases sequentially. Estimated length: 15-20 pages.

Timeline should be EXHAUSTIVE - aim for 50-80 events over 5 years (not 10-15 high-level summary points).
```

---

## **TASK 5: RELATED PARTY TRANSACTIONS & SUBSIDIARIES (DEEP VERSION)**

```markdown
# TASK 5: RELATED PARTY TRANSACTIONS & SUBSIDIARY INTELLIGENCE (FORENSIC DEPTH)

## OBJECTIVE
Map complete RPT landscape and subsidiary ecosystem, with governance scrutiny.

**Sources:**
- Annual Reports: "Related Party Disclosures" (typically Note 30-40)
- Quarterly Results: Check if RPT disclosed quarterly
- Subsidiary financial summaries (if disclosed in consolidated notes)
- Standalone vs Consolidated reconciliation notes

---

## PHASE 1: IDENTIFY ALL RELATED PARTIES

From most recent annual report (FY25):

### **MASTER LIST OF RELATED PARTIES**

| # | Related Party Name | Relationship Type | Nature of Entity | First Appeared (Year) | Status (Active/Ceased) | Source |
|---|-------------------|------------------|-----------------|---------------------|----------------------|--------|
| 1 | Tata Sons Pvt Ltd | Ultimate Holding Company | Conglomerate Holding | [Year or "Before FY21"] | Active | FY25 AR, Note 35, Page 98 |
| 2 | Tata Starbucks Pvt Ltd | Joint Venture (50% holding) | Coffee retail chain | [Year] | Active | [Source] |
| 3 | [Director Name] | Key Management Personnel | Individual (CEO) | [Year] | Active | [Source] |
| [Continue for EVERY related party listed...] | | | | | | |

**Categories to capture:**
- Promoter / Ultimate Holding Company
- Fellow Subsidiaries (Tata Group companies)
- Associates
- Joint Ventures
- Key Management Personnel (KMP)
- Relatives of KMP
- Enterprises where KMP/Relatives have significant influence
- Post-employment benefit plans (gratuity trust, etc.)

**Total Related Parties:** [X]

**Breakdown:**
- Promoter/Holding: [X]
- Tata Group Entities (Fellow Subsidiaries): [X]
- Associates/JVs: [X]
- KMP: [X]
- Others: [X]

---

## PHASE 2: EXTRACT RELATED PARTY TRANSACTIONS (5-YEAR TRACKING)

### **2A: QUANTITATIVE RPT DATA**

For EACH fiscal year (FY21-FY25), extract ALL transactions:

#### **TABLE: SALES TO RELATED PARTIES**

| Related Party | FY21 (₹ cr) | FY22 (₹ cr) | FY23 (₹ cr) | FY24 (₹ cr) | FY25 (₹ cr) | 5Y CAGR | Terms Disclosed | Source |
|--------------|-------------|-------------|-------------|-------------|-------------|---------|----------------|--------|
| Tata Sons | [X] | [X] | [X] | [X] | [X] | [Calculate] | "At arm's length" OR [Specific terms] | FY25 AR Note 35 |
| Tata Starbucks | [X] | [X] | [X] | [X] | [X] | [Calculate] | [Terms] | [Source] |
| [Continue for EVERY party with sales transactions...] | | | | | | | | |

**TOTAL SALES TO RPs** | [Sum] | [Sum] | [Sum] | [Sum] | [Sum] | [CAGR] | | |

#### **TABLE: PURCHASES FROM RELATED PARTIES**

[Same structure as above]

#### **TABLE: LOANS/ADVANCES GIVEN TO RPs**

| Related Party | FY21 (₹ cr) | FY22 (₹ cr) | FY23 (₹ cr) | FY24 (₹ cr) | FY25 (₹ cr) | Terms | Interest Rate | Repayment Schedule | Source |
|--------------|-------------|-------------|-------------|-------------|-------------|-------|--------------|-------------------|--------|
| [Party] | [X] | [X] | [X] | [X] | [X] | [Terms] | [Rate or "Not disclosed"] | [Schedule] | [Source] |

#### **TABLE: LOANS/ADVANCES TAKEN FROM RPs**

[Same structure]

#### **TABLE: OTHER TRANSACTIONS**

| Related Party | Transaction Type | FY21 | FY22 | FY23 | FY24 | FY25 | Terms | Source |
|--------------|-----------------|------|------|------|------|------|-------|--------|
| Tata Sons | Royalty/Brand Fee | [X] | [X] | [X] | [X] | [X] | "X% of revenue" OR [Not disclosed] | [Source] |
| [Party] | Rent Paid | [X] | [X] | [X] | [X] | [X] | [Terms] | [Source] |
| [Party] | Management Fees | [X] | [X] | [X] | [X] | [X] | [Terms] | [Source] |
| [Continue for: Guarantees, Interest paid/received, Dividend paid/received, Asset purchases/sales, etc.] | | | | | | | | |

---

### **2B: OUTSTANDING BALANCES**

As of FY25 year-end:

| Related Party | Trade Receivables Outstanding (₹ cr) | Trade Payables Outstanding (₹ cr) | Loans Receivable (₹ cr) | Loans Payable (₹ cr) | Aging (Days) | Source |
|--------------|-------------------------------------|----------------------------------|------------------------|---------------------|-------------|--------|
| [Party] | [X] | [Y] | [Z] | [W] | [A] days (if disclosed) | FY25 AR Note 35 |

**Aging Analysis:**
- Receivables >90 days: ₹[X] cr ([Y]% of total RP receivables)
- Receivables >180 days: ₹[Z] cr
- **Red Flag:** Any related party receivables >180 days? [Yes/No - if yes, list parties and amounts]

---

### **2C: RPT INTENSITY ANALYSIS**

| Metric | FY21 | FY22 | FY23 | FY24 | FY25 | 5Y Trend | Source |
|--------|------|------|------|------|------|---------|--------|
| **Total RPT (All Types)** | [X] | [X] | [X] | [X] | [X] | | [Source] |
| **Revenue (A)** | [X] | [X] | [X] | [X] | [X] | | [From financial tables] |
| **RPT Sales as % of Revenue** | [%] | [%] | [%] | [%] | [%] | [Increasing/Stable/Decreasing] | [Calculated] |
| **RPT Purchase as % of COGS** | [%] | [%] | [%] | [%] | [%] | | |
| **RPT Growth Rate (YoY %)** | - | [%] | [%] | [%] | [%] | | |
| **Revenue Growth Rate (YoY %)** | - | [%] | [%] | [%] | [%] | | |

**Key Question:** Is RPT growing faster than revenue?

| Year | RPT Growth | Revenue Growth | Differential | Assessment |
|------|-----------|---------------|-------------|------------|
| FY22 | [X]% | [Y]% | [X-Y] pp | [If differential >5pp: ⚠️ RPT outpacing business growth] |
| FY23 | [X]% | [Y]% | [X-Y] pp | |
| FY24 | [X]% | [Y]% | [X-Y] pp | |
| FY25 | [X]% | [Y]% | [X-Y] pp | |

---

### **2D: SINGLE PARTY DOMINANCE**

| Related Party | Total RPT (All Transactions) FY25 (₹ cr) | As % of Total RPT | Rank | Assessment |
|--------------|------------------------------------------|------------------|------|------------|
| [Top Party] | [X] | [Y]% | 1 | [If >30%: ⚠️ High concentration risk] |
| [2nd] | [X] | [Y]% | 2 | |
| [3rd] | [X] | [Y]% | 3 | |
| [Continue for top 5...] | | | | |

**Top 3 Concentration:** [Sum of top 3 as % of total RPT]%
- If >60%: 🔴 Very high concentration
- If 40-60%: 🟠 High concentration
- If <40%: ✅ Diversified

---

## PHASE 3: SUBSIDIARY & ASSOCIATE ECOSYSTEM

### **3A: COMPLETE SUBSIDIARY MAP**

| Entity Name | Ownership % | Classification | Country of Incorporation | Primary Business | Operational Status | Acquisition Date | Source |
|------------|-------------|---------------|------------------------|----------------|-------------------|----------------|--------|
| Tata Coffee Plantation (demerged entity) | [X]% | Subsidiary | India | Coffee plantations | [Operating/Under liquidation/Merged] | [Date] | FY25 AR Note 38 |
| Tata Consumer Products UK | 100% | Wholly-Owned Subsidiary | UK | Tea business (Tetley) | Operating | [Date] | [Source] |
| Tata Starbucks | 50% | Joint Venture | India | Coffee retail | Operating | [Date] | [Source] |
| [Continue for EVERY subsidiary/associate...] | | | | | | | |

**Total Count:**
- Wholly-owned subsidiaries: [X]
- Majority-owned subsidiaries: [X]
- Associates (20-50% holding): [X]
- Joint ventures: [X]

**Geographic Spread:**
- India: [X entities]
- UK: [X entities]
- US: [X entities]
- Canada: [X entities]
- Other: [X entities]

---

### **3B: SUBSIDIARY FINANCIAL PERFORMANCE**

For EACH material subsidiary (>5% of consolidated revenue or assets):

#### **SUBSIDIARY: [NAME]**

| Metric | FY21 | FY22 | FY23 | FY24 | FY25 | 5Y Trend | Source |
|--------|------|------|------|------|------|---------|--------|
| Revenue | [X] | [X] | [X] | [X] | [X] | | FY25 AR, Subsidiary Schedule |
| EBITDA | [X] | [X] | [X] | [X] | [X] | | |
| PAT/(Loss) | [X] | [X] | [X] | [X] | [X] | [Profitable/Loss-making/Breakeven] | |
| Total Assets | [X] | [X] | [X] | [X] | [X] | | |
| Total Equity | [X] | [X] | [X] | [X] | [X] | | |
| ROE % | [Calculate] | [Calculate] | [Calculate] | [Calculate] | [Calculate] | | |

**Performance Assessment:**
- **Status:** [✅ Profitable & Growing / ⚠️ Profitable but Stagnant / 🔴 Loss-making]
- **Consecutive loss years:** [X years - if applicable]
- **Parent's cumulative investment:** ₹[X] cr (from standalone balance sheet "Investments in subsidiaries")
- **Cumulative return to parent:** ₹[Y] cr (dividends received over 5 years)
- **Value Creation:** [If Return > Investment: ✅ Accretive / If Loss-making: 🔴 Dilutive]

[REPEAT for EVERY material subsidiary]

---

### **3C: INTER-COMPANY TRANSACTIONS**

| From (Entity) | To (Entity) | Transaction Type | FY25 Amount (₹ cr) | Terms | Purpose | Eliminated in Consolidation? | Source |
|--------------|-------------|-----------------|-------------------|-------|---------|----------------------------|--------|
| TCPL (Parent) | Tata Coffee Plantation | Sale of goods | [X] | [Terms] | [Raw material supply] | ✅ Yes | Standalone Note 35, Consolidated shows elimination |
| TCPL (Parent) | Tata Starbucks | Loan given | [X] | [Interest rate] | [Working capital support] | ❌ No (JV, not 100% owned) | [Source] |

**Key Observations:**
- Total inter-company revenue (parent to subsidiaries): ₹[X] cr (eliminated in consolidation)
- Total loans from parent to subsidiaries: ₹[X] cr outstanding
- **Red Flag Check:** Is parent lending to subsidiaries while parent itself is taking external debt? [Yes/No]

---

## PHASE 4: CONSOLIDATED vs STANDALONE RECONCILIATION

### **4A: FINANCIAL RECONCILIATION (Last 5 Years)**

| Metric | FY21 (Cons) | FY21 (SA) | Gap | FY22 (Cons) | FY22 (SA) | Gap | FY23 (Cons) | FY23 (SA) | Gap | FY24 (Cons) | FY24 (SA) | Gap | FY25 (Cons) | FY25 (SA) | Gap | Source |
|--------|------------|----------|-----|------------|----------|-----|------------|----------|-----|------------|----------|-----|------------|----------|-----|--------|
| **Revenue** | | | | | | | | | | | | | 17,618 | 12,802 | 4,816 | FY25 AR |
| **EBITDA** | | | | | | | | | | | | | [X] | [Y] | [Z] | |
| **PAT** | | | | | | | | | | | | | 1,287 | [X] | [Y] | |
| **Total Assets** | | | | | | | | | | | | | [X] | [Y] | [Z] | |
| **Total Debt** | | | | | | | | | | | | | [X] | [Y] | [Z] | |
| **Net Worth** | | | | | | | | | | | | | [X] | [Y] | [Z] | |
| **ROE %** | | | | | | | | | | | | | [X%] | [Y%] | [Z pp] | |
| **ROCE %** | | | | | | | | | | | | | [X%] | [Y%] | [Z pp] | |

**Gap Interpretation:**

#### **REVENUE GAP (FY25: Cons ₹17,618 cr vs SA ₹12,802 cr = Gap ₹4,816 cr)**
- **Gap as % of Consolidated:** 27.3%
- **Contributors to gap:**
  - International operations (UK, US, Canada): ₹[estimate if breakdown available]
  - Tata Starbucks (JV): ₹[X] cr
  - Other subsidiaries: ₹[balance]
- **Interpretation:** Subsidiaries contribute 27% of consolidated revenue. Parent India business (standalone) is still the dominant revenue driver (73%).

#### **PAT GAP (FY25: Cons ₹1,287 cr vs SA ₹[X] cr = Gap ₹[Y] cr)**
- **If Gap > 0:** Subsidiaries are **adding** ₹[Y] cr to consolidated PAT → ✅ **Value-accretive**
- **If Gap < 0:** Subsidiaries are **destroying** ₹[|Y|] cr → 🔴 **Value-destructive**
- **Breakdown (if possible):**
  - Tata Starbucks PAT contribution: ₹[X] cr (50% share)
  - International subsidiaries net PAT: ₹[X] cr
  - Loss-making subsidiaries drag: ₹[X] cr
- **Minority Interest:** ₹[X] cr (this portion of PAT belongs to minority shareholders, not parent)
- **PAT attributable to parent shareholders:** Cons PAT - Minority Interest = ₹[Net] cr

#### **ROE GAP (FY25: Cons [X]% vs SA [Y]% = Gap [Z] pp)**
- **If Cons ROE < SA ROE:** Subsidiaries are **diluting returns** → 🔴 **Capital deployed in subs earning lower returns than parent core**
- **If Cons ROE > SA ROE:** Subsidiaries are **enhancing returns** → ✅ **Capital deployed in subs earning higher returns**
- **Quantified:** Every ₹100 cr invested in subsidiaries is earning ROE of [calculate: Subsidiary PAT / Subsidiary equity]% vs parent's SA ROE of [Y]%

#### **DEBT GAP (FY25: Cons ₹[X] cr vs SA ₹[Y] cr = Gap ₹[Z] cr)**
- **Interpretation:** ₹[Z] cr of consolidated debt sits in subsidiaries
- **As % of total debt:** [Z/X × 100]%
- **Risk Assessment:**
  - If subsidiaries are profitable: ✅ Subsidiaries can service their own debt
  - If subsidiaries are loss-making: 🔴 Parent may need to support subsidiaries to avoid default
  - **Check:** Are there any parent guarantees for subsidiary debt? [Yes/No - cite source]

---

### **4B: SUBSIDIARY VALUE CREATION SCORECARD**

| Subsidiary | Revenue Contribution (% of Cons) | PAT Contribution (% of Cons) | ROE vs Parent SA ROE | Value Assessment | Overall Grade |
|------------|--------------------------------|----------------------------|---------------------|------------------|---------------|
| Tata Coffee (merged FY24) | [Estimate pre-merger: X%] | [Y%] | [Higher/Lower by Z pp] | [Accretive/Dilutive] | ✅ A / ⚠️ B / 🔴 C |
| Tata Starbucks (JV) | [X%] | [Y%] | [Comparison] | [Assessment] | [Grade] |
| International subsidiaries (aggregate) | [X%] | [Y%] | [Comparison] | [Assessment] | [Grade] |
| NourishCo (merged FY25) | [Pre-merger: X%] | [Y%] | [Comparison] | [Assessment] | [Grade] |

**Overall Subsidiary Portfolio Grade:**
- **A:** All major subsidiaries value-accretive, ROE >= Parent ROE
- **B:** Mixed - Some accretive, some dilutive, Net impact neutral
- **C:** Net dilutive - Subsidiaries destroying value

**Grade:** [A/B/C]

---

## PHASE 5: GOVERNANCE RED FLAGS

### **5A: RPT RED FLAGS**

**Check these specific red flags:**

| Red Flag | Present? | Evidence | Severity | Source |
|----------|---------|----------|---------|--------|
| RPT >20% of revenue | [Yes/No] | [If yes: X% in FY25] | [🔴/🟠/🟢] | [Source] |
| RPT growing >2× revenue growth (sustained 3+ years) | [Yes/No] | [If yes: RPT CAGR X% vs Revenue CAGR Y%] | [🔴/🟠/🟢] | [Calculated from Phase 2C] |
| Large loans to related parties (>10% of net worth) | [Yes/No] | [If yes: ₹X cr, Y% of NW] | [🔴/🟠/🟢] | [Phase 2B] |
| RP receivables outstanding >180 days | [Yes/No] | [If yes: ₹X cr from [Party]] | [🔴/🟠/🟢] | [Phase 2B] |
| Vague terms disclosure ("at arm's length" without benchmark) | [Yes/No] | [If yes: cite examples] | [🟠/🟡] | [Phase 2A] |
| Parent lending to subsidiaries while taking external debt | [Yes/No] | [If yes: Parent loan to sub ₹X cr, Parent ext debt ₹Y cr] | [🔴/🟠] | [Phase 3C + financial tables] |
| Promoter/Holding company extracting fees >2% of revenue | [Yes/No] | [If yes: ₹X cr, Y% of revenue] | [🟠/🟡] | [Phase 2A] |

---

### **5B: SUBSIDIARY RED FLAGS**

| Red Flag | Present? | Evidence | Severity | Source |
|----------|---------|----------|---------|--------|
| Loss-making subsidiary for 3+ consecutive years | [Yes/No] | [If yes: [Sub name], losses for X years] | [🔴] | [Phase 3B] |
| Standalone PAT > Consolidated PAT (subsidiaries destroying value) | [Yes/No] | [If yes: SA PAT ₹X cr > Cons PAT ₹Y cr] | [🔴] | [Phase 4A] |
| Consolidated ROE < Standalone ROE by >5 pp | [Yes/No] | [If yes: Gap = Z pp] | [🔴/🟠] | [Phase 4A] |
| Subsidiary debt >50% of consolidated debt | [Yes/No] | [If yes: Sub debt ₹X cr = Y% of Cons debt] | [🟠] | [Phase 4A] |
| Parent's cumulative investment in subsidiary >₹100 cr with zero returns for 5 years | [Yes/No] | [If yes: [Sub name], ₹X cr invested, ₹Y cr returned] | [🔴] | [Phase 3B] |
| Opaque subsidiary structure (>20 entities, frequent restructuring) | [Yes/No] | [If yes: [Evidence]] | [🟠/🟡] | [Phase 3A + Event Timeline] |

---

## PHASE 6: POSITIVE GOVERNANCE SIGNALS

Balance the red flags with positives:

| Positive Signal | Present? | Evidence | Source |
|----------------|---------|----------|--------|
| RPT intensity declining over 5 years | [Yes/No] | [If yes: FY21 X% → FY25 Y%] | [Phase 2C] |
| Subsidiaries merged into parent (simplification) | [Yes/No] | [If yes: NourishCo, Soulfull, SmartFoodz merged FY25] | [Event Timeline, Accounting Changes] |
| Transparent RPT disclosure (benchmarking provided) | [Yes/No] | [If yes: cite examples] | [Phase 2A] |
| All subsidiaries profitable | [Yes/No] | [If yes: cite Phase 3B scorecard] | [Phase 3B] |
| Consolidated ROE >= Standalone ROE (subsidiaries enhancing returns) | [Yes/No] | [If yes: Data] | [Phase 4A] |
| Entity count reduced (simplification) | [Yes/No] | [If yes: From X entities to Y entities] | [Event Timeline] |

---

## PHASE 7: VERIFICATION CHECKLIST

- [ ] I listed ALL related parties from FY25 annual report
- [ ] I extracted RPT data for ALL 5 years (FY21-FY25)
- [ ] I covered ALL transaction types (sales, purchases, loans, fees, etc.)
- [ ] I calculated RPT intensity (as % of revenue) for each year
- [ ] I identified any RPT growing faster than revenue (sustained 3+ years)
- [ ] I listed ALL subsidiaries with ownership %, country, business
- [ ] I extracted subsidiary financials for ALL material subs (>5% contribution)
- [ ] I calculated Cons vs SA gaps for ALL key metrics (Revenue, PAT, ROE, Debt)
- [ ] I interpreted gaps (what they reveal about parent vs subsidiary health)
- [ ] I assessed value creation: Are subs accretive or dilutive?
- [ ] I checked ALL 7 RPT red flags
- [ ] I checked ALL 6 subsidiary red flags
- [ ] I noted positive governance signals (if any)
- [ ] I cited sources for EVERY claim

**If ANY box unchecked → GO BACK and complete.**

---

**OUTPUT:** All 7 phases sequentially. Estimated length: 15-20 pages.

This is forensic governance analysis - be thorough, not superficial.
```

---

## **TASK 6: MANAGEMENT GUIDANCE TRACKER (DEEP VERSION)**

```markdown
# TASK 6: MANAGEMENT GUIDANCE vs ACTUAL PERFORMANCE TRACKER (CREDIBILITY ANALYSIS)

## OBJECTIVE
Create a complete log of ALL forward-looking statements by management, compare to actual outcomes, and score credibility.

**Sources:**
- Earnings call transcripts: Management prepared remarks + Q&A responses
- Investor presentations: "Outlook" or "Guidance" slides
- Annual reports: MD&A section ("Future Outlook")

---

## PHASE 1: EXTRACT ALL GUIDANCE STATEMENTS

For EACH quarter/year with transcript available:

### **GUIDANCE EXTRACTION TABLE**

| Date Given | Source | Speaker | Category | Exact Guidance Statement (Quote) | Specificity | Time Horizon | Conditions/Caveats (Quote) | Source Citation |
|------------|--------|---------|----------|--------------------------------|------------|--------------|---------------------------|----------------|
| Q4 FY24, Apr 2024 | Q4 FY24 Transcript | CFO | Revenue Growth | "We expect to deliver double-digit growth in FY25" | Directional (no range) | FY25 (full year) | "Barring unforeseen circumstances" | Q4_FY24_Transcript.pdf, Page 15, CFO Remarks |
| Q4 FY24, Apr 2024 | Q4 FY24 Presentation | Management | Synergies | "Committed to delivering 2-3% synergy benefits from Tata Coffee integration" | Specific Range | FY25-FY26 | None stated | Q4_FY24_Presentation.pdf, Slide 22 |
| Q3 FY25, Feb 2025 | Q3 FY25 Transcript | CEO | Margins | "EBITDA margins will be in mid-to-high teens for full year" | Range (15-19%) | FY25 | "Subject to commodity price volatility" | Q3_FY25_Transcript.pdf, Timestamp 18:30 |
| [Continue for EVERY guidance statement in ALL transcripts/presentations...] | | | | | | | | |

**Categories:**
- Revenue/Sales Growth
- Margin (Gross/EBITDA/PAT)
- Specific Segment Growth (e.g., "India Beverages to grow X%")
- Capex
- Outlet Expansion (numeric distribution)
- Market Share
- Synergies (M&A related)
- New Product Performance
- Debt Reduction
- Working Capital
- ROE/ROCE targets

**Specificity Classification:**
- **Specific Range:** "15-18%" OR "₹500-600 cr"
- **Point Estimate:** "20%" OR "₹550 cr"
- **Directional:** "Double-digit" OR "High single-digit" OR "Improving" OR "Stable"
- **Vague:** "Positive" OR "Good momentum" OR "On track"

**Time Horizon:**
- Near-term: Next quarter
- Medium-term: Current fiscal year
- Long-term: 3-5 years OR Multi-year target

---

## PHASE 2: MATCH GUIDANCE TO ACTUALS

For EVERY guidance statement where target period has elapsed:

### **GUIDANCE vs ACTUAL TRACKING TABLE**

| Guidance Date | Category | Guidance Statement | Time Horizon | Target Period | **ACTUAL OUTCOME** | Variance (Absolute) | Variance (%) | Classification | Management's Explanation (if outcome missed) | Source for Actual | Source for Explanation |
|--------------|----------|-------------------|--------------|--------------|-------------------|-------------------|-------------|---------------|-------------------------------------------|------------------|----------------------|
| Q4 FY24 (Apr 2024) | Revenue Growth | "Double-digit growth in FY25" | FY25 | FY25 (Apr 2024-Mar 2025) | **FY25 Revenue: ₹17,618 cr, Growth: 16% YoY** | +6 pp (if "double-digit" = 10% assumed) | +60% above baseline | ✅ **BEAT** | N/A (exceeded) | FY25 Annual Results | N/A |
| Q4 FY24 | Synergies | "2-3% synergy benefits from Tata Coffee merger" | FY25-FY26 | FY25 | **Management stated "Committed synergies delivered" in Q4 FY25 call** | Not quantified publicly | N/A | ✅ **HIT** (qualitative) | N/A | Q4 FY25 Transcript, Page 12 | N/A |
| Q3 FY25 | Margins | "EBITDA margins in mid-to-high teens for FY25" | FY25 | FY25 | **FY25 EBITDA Margin: [X]%** | [Calculate vs midpoint 17%] | [%] | [HIT/BEAT/MISS] | [If missed: Quote reason] | FY25 Results | [Source if miss explained] |
| [Continue for EVERY guidance...] | | | | | | | | | | | |

**Classification Rules:**
- **HIT:** Actual within guided range OR within ±5% of point estimate OR directional guidance directionally correct
- **BEAT:** Actual exceeds guidance by >5% (for point estimate) OR above guided range
- **MISS:** Actual below guidance by >5% OR below guided range OR directional guidance wrong

**For directional guidance (e.g., "double-digit"):**
- Assume: "Double-digit" = 10-19% (use 12% midpoint for variance calc)
- Assume: "High single-digit" = 7-9% (use 8% midpoint)
- Assume: "Mid-to-high teens" = 15-19% (use 17% midpoint)

---

## PHASE 3: GUIDANCE ACCURACY SCORING

### **3A: HIT RATE CALCULATION**

| Category | Total Guidance Statements | Hits | Beats | Misses | Hit Rate % | Beat Rate % | Miss Rate % |
|----------|--------------------------|------|-------|--------|------------|------------|------------|
| Revenue Growth | [X] | [Y] | [Z] | [W] | [Y/X×100] | [Z/X×100] | [W/X×100] |
| Margins | [X] | [Y] | [Z] | [W] | [%] | [%] | [%] |
| Capex | [X] | [Y] | [Z] | [W] | [%] | [%] | [%] |
| Outlets/Distribution | [X] | [Y] | [Z] | [W] | [%] | [%] | [%] |
| Synergies | [X] | [Y] | [Z] | [W] | [%] | [%] | [%] |
| Other | [X] | [Y] | [Z] | [W] | [%] | [%] | [%] |
| **OVERALL** | **[Total]** | **[Total Hits]** | **[Total Beats]** | **[Total Misses]** | **[Overall %]** | **[Overall %]** | **[Overall %]** |

**Interpretation:**
- Hit Rate >70%: ✅ High credibility
- Hit Rate 50-70%: ⚠️ Moderate credibility
- Hit Rate <50%: 🔴 Low credibility

---

### **3B: AVERAGE VARIANCE ANALYSIS**

For all guidance with quantified targets:

| Metric | Total Instances | Average Variance (%) | Median Variance (%) | Max Positive Variance (Beat) | Max Negative Variance (Miss) |
|--------|----------------|---------------------|-------------------|----------------------------|------------------------------|
| Revenue Growth | [X] | [Calculate: Sum of all variances / X] | [Middle value] | +[Y]% ([Period]) | -[Z]% ([Period]) |
| EBITDA Margin | [X] | [Avg %] | [Median %] | +[Y bps] | -[Z bps] |
| Capex | [X] | [Avg %] | [Median %] | +[Y]% | -[Z]% |
| **OVERALL** | **[X]** | **[Avg %]** | **[Median %]** | | |

**Bias Assessment:**
- Average Variance **close to 0%** (±3%): **Neutral / Accurate** guider
- Average Variance **+5% to +15%**: **Conservative / Sandbagging** (consistently beats)
- Average Variance **-5% to -15%**: **Optimistic / Overpromising** (consistently misses)
- Average Variance **>±20%**: **Unreliable / Poor Visibility**

**Company's Bias:** [Conservative / Neutral / Optimistic / Unreliable] based on average variance of [X]%

---

### **3C: CREDIBILITY SCORE (WEIGHTED)**

Assign points for each guidance statement:
- **HIT:** 100 points
- **BEAT <10%:** 90 points (slightly conservative, acceptable)
- **BEAT 10-20%:** 70 points (sandbagging)
- **BEAT >20%:** 50 points (severe sandbagging)
- **MISS <10%:** 70 points (minor miss, acceptable)
- **MISS 10-20%:** 40 points (material miss)
- **MISS >20%:** 0 points (severe miss)

**Total Score:** [Sum of all points] / ([Total guidance statements] × 100) × 100 = **[X]/100**

**Credibility Rating:**
- **80-100: HIGHLY CREDIBLE** - Guidance can be modeled with confidence
- **60-79: MODERATELY CREDIBLE** - Guidance directionally useful, apply 10-15% margin of safety
- **40-59: LOW CREDIBILITY** - Guidance unreliable, discount by 20-30%
- **<40: NOT CREDIBLE** - Ignore guidance, focus only on historical track record

**Company's Credibility Score:** **[X]/100** → **[Rating]**

---

## PHASE 4: GUIDANCE REVISION TRACKING

Track instances where management CHANGED guidance mid-course:

| Original Date | Original Guidance (Quote) | Revision Date | Revised Guidance (Quote) | Direction | Reason Given (Quote) | Final Outcome | Variance from Original | Variance from Revised | Source (Original) | Source (Revision) |
|--------------|-------------------------|--------------|------------------------|-----------|---------------------|--------------|----------------------|---------------------|------------------|------------------|
| Q1 FY25 | "FY25 revenue growth 12-15%" | Q3 FY25 | "FY25 revenue growth 14-16%" | ⬆️ Upgrade | "Strong demand trends continuing beyond expectations" | FY25 actual: 16% | +2 pp vs orig midpoint | Within revised range (HIT) | Q1_FY25_Transcript p10 | Q3_FY25_Transcript p8 |
| [Continue for ALL revisions...] | | | | | | | | | | |

**Revision Pattern Analysis:**
- Total revisions: [X]
- Upgrades: [Y] - Common reasons: [Summarize]
- Downgrades: [Z] - Common reasons: [Summarize]
- Revision Rate: [X / Total guidance] = [W]%

**Interpretation:**
- Low revision rate (<10%): Good visibility, guidance accurate
- Moderate (10-25%): Some uncertainty
- High (>25%): Poor visibility OR sandbagging (initial guide low, then upgrade)

---

## PHASE 5: LONG-TERM TARGET TRACKING

For multi-year strategic targets (e.g., "Double revenue in 5 years"):

| Target Announced | Target Statement (Exact Quote) | Target Metric | Base Year | Base Value | Target Year | Target Value | Implied CAGR | Current Progress (Latest Year) | Actual CAGR to Date | Projected Target Year Outcome | On Track? | Shortfall/Excess | Revised? | Source (Original) | Source (Latest) |
|----------------|-------------------------------|--------------|-----------|------------|------------|-------------|-------------|------------------------------|-------------------|----------------------------|-----------|----------------|---------|------------------|----------------|
| FY22 (2021) | "Reach 4 million outlets by FY24" | Numeric Distribution | FY22 | ~3.5M | FY24 | 4.0M | N/A (absolute target) | FY24: 4.0M achieved | N/A | ✅ TARGET MET | ✅ Yes | On target | No | FY22 AR, MD&A | Q4_FY24_Transcript |
| FY23 (2022) | "Growth businesses (Sampann, NourishCo, etc.) to be 30% of portfolio growing at 30%" | Revenue Mix & Growth | FY23 | [X]% of revenue | FY28 (assumed 5Y) | 30% at 30% growth | [Calculate] | FY25: [Y]% of revenue, growing at [Z]% | [CAGR] | [Projection] | [On track / Behind / Ahead] | [Calculate] | [Check if mentioned in recent calls] | FY23 Presentation | FY25 Transcript |

**Long-Term Target Assessment:**
- Targets met: [X/Y]
- Targets on track: [X/Y]
- Targets behind: [X/Y]
- Targets abandoned (never mentioned again): [X/Y] ⚠️ **Silent failures**

---

## PHASE 6: CONCALL Q&A BEHAVIOR ANALYSIS

From transcripts, analyze management's response patterns:

### **6A: TONE EVOLUTION**

| Quarter | Revenue Outlook (Quote) | Margin Outlook (Quote) | Overall Tone | Notable Quotes | Tone Shift from Prior Quarter | Source |
|---------|------------------------|----------------------|--------------|---------------|------------------------------|--------|
| Q1 FY25 | "Strong demand momentum" | "Margins expanding sequentially" | Confident & Optimistic | "Best demand environment in years" [Q1_FY25, 10:15] | Baseline | Q1_FY25_Transcript |
| Q2 FY25 | "Momentum continuing" | "Managing commodity inflation" | Confident but Cautious | "Some cost headwinds but pricing actions in place" | Slight caution on costs | Q2_FY25_Transcript |
| Q3 FY25 | "Healthy growth visibility" | "Margins under pressure" | Neutral to Cautious | "Coffee prices at 50-year high" [Q3_FY25, 8:20] | ⚠️ Shift to Cautious | Q3_FY25_Transcript |
| [Continue for all quarters...] | | | | | | |

**Tone Classification:**
- **Confident & Optimistic:** "Strong", "Robust", "Excellent", "Record"
- **Confident & Stable:** "Steady", "As expected", "In line"
- **Cautious:** "Some headwinds", "Near-term pressure", "Watching closely"
- **Defensive:** "Temporary", "Cyclical", "External factors", "Worst behind us"
- **Pessimistic:** "Challenging", "Difficult", "Uncertain"

**Early Warning Capability:**
- Does tone shift BEFORE results deteriorate? ✅ Good early warning
- Does tone shift CONCURRENT with results deteriorate? ⚠️ Moderate
- Does tone remain optimistic while results deteriorate? 🔴 Poor / Misleading

**Assessment for this company:** [Good / Moderate / Poor] early warning based on [evidence]

---

### **6B: QUESTION CLUSTERING**

For each recent quarter (last 4), analyze analyst questions:

| Quarter | Top 3 Topics by Question Count | Question Count (Topic 1) | Question Count (Topic 2) | Question Count (Topic 3) | Total Questions | Interpretation | Source |
|---------|-------------------------------|-------------------------|-------------------------|-------------------------|----------------|---------------|--------|
| Q3 FY26 | 1. Coffee inflation 2. Pricing power 3. Volume growth | 7 out of 22 | 5 out of 22 | 4 out of 22 | 22 | Analysts concerned about commodity cost impact | Q3_FY26_Transcript |
| Q2 FY26 | 1. M&A integration 2. New channel (HORECA) 3. Margin outlook | [X/Y] | [X/Y] | [X/Y] | [Y] | Focus on growth initiatives | Q2_FY26_Transcript |

**Trend Analysis:**
- If same topic dominates 3+ consecutive calls: ⚠️ Persistent investor concern not being addressed
- If question topics shift from growth to defensive (margins, cash flow): ⚠️ Deteriorating sentiment

---

### **6C: EVASION DETECTION**

Count instances where management deflected or didn't answer directly:

| Quarter | Question (Paraphrased) | Management Response (Quote) | Response Type | Assessment | Source |
|---------|----------------------|---------------------------|--------------|------------|--------|
| Q3 FY26 | "When will working capital normalize?" | "We're working on it, should improve through year-end" | ⚠️ Vague / No timeline | Evasive (3rd quarter saying "soon") | Q3_FY26_Transcript, 42:15 |
| Q2 FY26 | "Is XYZ subsidiary profitable yet?" | "It's strategic, let's discuss offline" | 🔴 **"Take offline"** deflection | High evasion | Q2_FY26_Transcript, 55:30 |
| Q3 FY26 | "Quantify coffee inflation impact on margins?" | "Material impact, but we're taking pricing actions" | ⚠️ Qualitative only | Moderate evasion (no numbers) | Q3_FY26_Transcript, 18:50 |

**Evasion Score:** [X "take offline" + Y vague responses] / [Total questions] = [Z]%

**Trend:**
- Evasion rate increasing? ⚠️ Management less transparent as issues mount
- Evasion rate stable/low (<15%)? ✅ Transparent communication

**Company's Evasion Rate:** [X]% - [Low <15% = Transparent / Medium 15-25% = Adequate / High >25% = Concerning]

---

## PHASE 7: SUMMARY ASSESSMENT

### **MANAGEMENT CREDIBILITY REPORT CARD**

| Dimension | Score/Assessment | Evidence | Grade |
|-----------|-----------------|----------|-------|
| **Quantitative Guidance Hit Rate** | [X]% | [Hits: Y, Misses: Z out of W total] | [A/B/C/D] |
| **Credibility Score (Weighted)** | [X]/100 | [Breakdown by category] | [Highly/Moderately/Low/Not Credible] |
| **Bias** | [Conservative/Neutral/Optimistic] | Average variance: [+/-X]% | [A/B/C] |
| **Revision Frequency** | [X]% revision rate | [Y revisions out of Z guidance statements] | [A: <10% / B: 10-25% / C: >25%] |
| **Long-Term Target Achievement** | [X met, Y missed out of Z total] | [List key targets] | [A: >80% / B: 50-80% / C: <50%] |
| **Tone Reliability (Early Warning)** | [Good/Moderate/Poor] | [Evidence of tone shifts before/after results] | [A/B/C] |
| **Transparency (Evasion Rate)** | [X]% evasion | [Y evasive responses / Z total questions] | [A: <15% / B: 15-25% / C: >25%] |

**OVERALL MANAGEMENT CREDIBILITY GRADE:** [A / B+ / B / B- / C+ / C / D]

**Grade Interpretation:**
- **A (Excellent):** Guidance highly reliable, transparent communication, good early warnings
- **B (Good):** Guidance mostly reliable, adequate transparency, some minor concerns
- **C (Adequate):** Guidance unreliable, transparency gaps, reactive communication
- **D (Poor):** Guidance not credible, evasive, misleading communication

**Grade for this company:** **[Grade]**

---

### **INVESTOR IMPLICATIONS**

**Modeling Recommendations:**
- **If Grade A:** Use guidance as baseline for models, apply minimal margin of safety (5-10%)
- **If Grade B:** Use guidance directionally, apply 10-15% margin of safety
- **If Grade C:** Discount guidance by 20-30%, rely more on historical trends
- **If Grade D:** Ignore guidance entirely, model based only on historical performance extrapolation

**Red Flags to Watch:**
1. [Specific guidance category with worst track record]
2. [Specific behavioral concern - e.g., "Evasion increasing on working capital questions"]
3. [Specific long-term target at risk - e.g., "XYZ target 30% behind pace"]

**Positive Signals:**
1. [Specific guidance category with best track record]
2. [Specific behavioral strength - e.g., "Management acknowledged cost challenges early, before visible in numbers"]
3. [Specific long-term target achieved - e.g., "4M outlet target met on time"]

---

## PHASE 8: VERIFICATION CHECKLIST

- [ ] I extracted guidance from ALL available transcripts (not just recent)
- [ ] I extracted guidance from ALL investor presentations
- [ ] I captured EXACT quotes (in quotation marks) for each guidance statement
- [ ] I classified specificity (Specific/Directional/Vague) for each statement
- [ ] I matched EVERY elapsed-period guidance to actual outcome
- [ ] I calculated variance (absolute and %) for quantified guidance
- [ ] I classified outcome (HIT/BEAT/MISS) using defined rules
- [ ] I calculated hit rate by category and overall
- [ ] I calculated average variance and assessed bias
- [ ] I computed weighted credibility score (0-100)
- [ ] I tracked ALL guidance revisions mid-course
- [ ] I tracked ALL long-term targets (multi-year)
- [ ] I analyzed tone evolution quarter-by-quarter
- [ ] I identified question clustering patterns
- [ ] I counted evasion instances and calculated evasion rate
- [ ] I assigned overall credibility grade with justification
- [ ] I cited sources for EVERY guidance statement and actual outcome

**If ANY box unchecked → GO BACK and complete.**

---

**OUTPUT:** All 8 phases sequentially. Estimated length: 12-18 pages.

This is the most important section for assessing whether investors can TRUST management. Be thorough.
```

---

## **TASK 7: RED FLAG PRE-SCREENING (DEEP VERSION)**

```markdown
# TASK 7: COMPREHENSIVE RED FLAG PRE-SCREENING (FORENSIC SCAN)

## OBJECTIVE
Identify ALL potential concerns across 5 years that warrant deep scrutiny in final analysis.

**Critical Note:** This is PRE-SCREENING. Cast a WIDE net. Flag anything suspicious even if uncertain. Stage 3 (Opus) will prioritize and investigate.

---

## PHASE 1: EARNINGS QUALITY RED FLAGS

### **1A: CASH FLOW vs PROFIT DIVERGENCE**

From financial tables (Task 2):

| Year | PAT (Consolidated) | Operating Cash Flow (CFO) | CFO/PAT Ratio | Free Cash Flow (FCF) | FCF/PAT Ratio | Assessment | Source |
|------|-------------------|---------------------------|--------------|---------------------|--------------|------------|--------|
| FY25 | 1,287 | [X] | [Calculate] | [CFO - Capex] | [Calculate] | [If CFO/PAT <70%: ⚠️ Flag] | FY25 Cash Flow Statement |
| FY24 | [X] | [X] | [X] | [X] | [X] | | |
| FY23 | [X] | [X] | [X] | [X] | [X] | | |
| FY22 | [X] | [X] | [X] | [X] | [X] | | |
| FY21 | [X] | [X] | [X] | [X] | [X] | | |

**Red Flags:**
- 🔴 **CRITICAL:** CFO/PAT ratio <50% for ANY year (severe earnings quality concern)
- 🟠 **HIGH:** CFO/PAT ratio <70% for 2+ consecutive years (persistent issue)
- 🟠 **HIGH:** FCF negative for 3+ consecutive years despite positive PAT (capital trap)
- 🟡 **MEDIUM:** CFO/PAT declining trend over 5 years (deteriorating quality)

**Identified Red Flags in this Category:** [List with severity]

---

### **1B: WORKING CAPITAL TRENDS**

From financial tables:

| Quarter | Receivables Days | Inventory Days | Payables Days | Cash Conversion Cycle | YoY Change in CCC | Source |
|---------|-----------------|---------------|--------------|---------------------|------------------|--------|
| Q3 FY26 | [X] | [Y] | [Z] | [X+Y-Z] | [vs Q3 FY25] | Q3_FY26_Results |
| Q2 FY26 | [X] | [Y] | [Z] | [CCC] | [vs Q2 FY25] | |
| [Continue for last 20 quarters...] | | | | | | |

**Red Flags:**
- 🔴 **CRITICAL:** Receivables days increased >40 days YoY in any quarter
- 🟠 **HIGH:** Cash Conversion Cycle widened >25 days YoY
- 🟠 **HIGH:** Receivables days >120 days (indicates weak bargaining power or collection issues)
- 🟡 **MEDIUM:** Inventory days increasing >20 days YoY (demand softness or overstocking)

**Identified Red Flags:** [List]

---

### **1C: REVENUE RECOGNITION CONCERNS**

From financial tables and accounting policies:

**Check:**
- Unbilled revenue / Contract assets trend (from balance sheet):

| Year | Unbilled Revenue (₹ cr) | As % of Total Revenue | YoY Change % | Source |
|------|-------------------------|---------------------|-------------|--------|
| FY25 | [X] | [Y%] | [Z%] | FY25 BS |
| [Continue...] | | | | |

**Red Flags:**
- 🟠 **HIGH:** Unbilled revenue growing >30% YoY while billed revenue growing <15%
- 🟡 **MEDIUM:** Unbilled revenue >10% of total revenue (aggressive recognition)

- Deferred revenue trend (from balance sheet):

| Year | Deferred Revenue (₹ cr) | YoY Change % | Source |
|------|------------------------|-------------|--------|
| FY25 | [X] | [Y%] | [Source] |

**Red Flags:**
- 🟠 **HIGH:** Deferred revenue declining >20% YoY while revenue growing (pulling forward recognition?)

**Identified Red Flags:** [List]

---

### **1D: MARGIN & MIX ANOMALIES**

From financial tables:

**Check for sudden margin expansion:**

| Period | Gross Margin % | EBITDA Margin % | PAT Margin % | QoQ Change (bps) | YoY Change (bps) | Source |
|--------|---------------|----------------|-------------|-----------------|----------------|--------|
| Q3 FY26 | [X%] | [Y%] | [Z%] | [A bps] | [B bps] | Q3_FY26_Results |
| [Continue...] | | | | | | |

**Red Flags:**
- 🟠 **HIGH:** Gross margin expansion >300 bps in single quarter without clear cost explanation or pricing action disclosed
- 🟡 **MEDIUM:** EBITDA margin expanding while PAT margin compressing (interest/tax issue)

**Segment margin divergence:**

| Period | Segment A Margin % | Segment B Margin % | Segment C Margin % | Spread (Max-Min) | Source |
|--------|-------------------|-------------------|-------------------|-----------------|--------|
| Q3 FY26 | [X%] | [Y%] | [Z%] | [W pp] | [Source] |

**Red Flags:**
- 🟡 **MEDIUM:** One segment margin improving >500 bps while another declining >300 bps (mix shift or accounting?)

**Identified Red Flags:** [List]

---

### **1E: OTHER INCOME DEPENDENCY**

From financial tables:

| Year | Operating Profit (EBIT) | Other Income | Other Income as % of Operating Profit | Nature of Other Income | Source |
|------|------------------------|--------------|-------------------------------------|----------------------|--------|
| FY25 | [X] | [Y] | [Y/X × 100] | [Interest, Forex, Misc, Asset Sale, etc.] | FY25 P&L |
| [Continue...] | | | | | |

**Red Flags:**
- 🔴 **CRITICAL:** Other income >50% of operating profit (profit from operations vs non-core)
- 🟠 **HIGH:** Other income growing >50% YoY while operating profit flat/declining
- 🟡 **MEDIUM:** One-time gains appearing in "Other Income" repeatedly (3+ times in 5 years)

**Identified Red Flags:** [List]

---

## PHASE 2: BALANCE SHEET RED FLAGS

### **2A: DEBT & LEVERAGE**

From financial tables:

| Year | Total Debt (Cons) | Equity (Cons) | Debt/Equity | Interest Coverage (EBIT/Interest) | Short-Term Debt as % of Total Debt | Source |
|------|------------------|--------------|------------|----------------------------------|----------------------------------|--------|
| FY25 | [X] | [Y] | [X/Y] | [Calculate] | [%] | FY25 BS |
| [Continue...] | | | | | | |

**Red Flags:**
- 🔴 **CRITICAL:** Debt/Equity >2.0× for non-financial companies
- 🔴 **CRITICAL:** Interest coverage <2.0× (barely covering interest)
- 🟠 **HIGH:** Short-term debt >60% of total debt (refinancing risk)
- 🟡 **MEDIUM:** Debt increasing >30% YoY while revenue growing <15%

**Debt covenant disclosures:**
- Check notes: Any mention of debt covenant breach or waiver? [Yes/No - if yes, cite source and details]

**Identified Red Flags:** [List]

---

### **2B: ASSET QUALITY**

From financial tables:

| Year | Goodwill & Intangibles (₹ cr) | As % of Total Assets | YoY Change % | Capex (₹ cr) | Capital WIP (₹ cr) | CWIP as % of Fixed Assets | Source |
|------|------------------------------|---------------------|-------------|-------------|-------------------|--------------------------|--------|
| FY25 | [X] | [Y%] | [Z%] | [A] | [B] | [C%] | FY25 BS |
| [Continue...] | | | | | | | |

**Red Flags:**
- 🟠 **HIGH:** Goodwill >20% of total assets (acquisition-heavy, impairment risk)
- 🟠 **HIGH:** Capital WIP >25% of fixed assets AND aging >3 years (stalled projects)
- 🟡 **MEDIUM:** Goodwill impairment in any year (overpaid for acquisition?)

**Check notes:** Any asset write-offs or impairments disclosed? [List with amounts and reasons]

**Identified Red Flags:** [List]

---

### **2C: CONTINGENT LIABILITIES**

From notes to accounts:

| Year | Contingent Liabilities (₹ cr) | As % of Net Worth | Nature (Tax/Legal/Guarantees/Other) | YoY Change % | Source |
|------|------------------------------|------------------|-----------------------------------|-------------|--------|
| FY25 | [X] | [Y%] | [Breakdown] | [Z%] | FY25 AR Note [X] |
| [Continue...] | | | | | |

**Red Flags:**
- 🔴 **CRITICAL:** Contingent liabilities >75% of net worth (material risk if crystallized)
- 🟠 **HIGH:** Contingent liabilities increasing >50% YoY
- 🟡 **MEDIUM:** Large tax disputes disclosed (>₹100 cr or >10% of net worth)

**Identified Red Flags:** [List]

---

## PHASE 3: GOVERNANCE RED FLAGS

### **3A: AUDITOR QUALITY**

From annual reports:

| Year | Auditor Name | Tenure (Years) | Audit Fee (₹ L) | Non-Audit Fee (₹ L) | NA/A Ratio | Opinion | EOM/Qualifications | Source |
|------|-------------|---------------|----------------|-------------------|----------|---------|-------------------|--------|
| FY25 | [Firm] | [X] | [Y] | [Z] | [Z/Y] | [Unqualified/Qualified/etc.] | [Yes/No - if yes, describe] | FY25 AR Auditor Report |
| [Continue...] | | | | | | | | |

**Red Flags:**
- 🔴 **CRITICAL:** Qualified opinion OR Adverse opinion OR Disclaimer
- 🔴 **CRITICAL:** Non-audit fees >100% of audit fees (independence compromised)
- 🟠 **HIGH:** Auditor change in last 3 years without clear succession plan reason
- 🟠 **HIGH:** Auditor tenure >15 years (independence concern)
- 🟡 **MEDIUM:** Emphasis of Matter (EOM) on material uncertain tax/legal issue

**Identified Red Flags:** [List]

---

### **3B: MANAGEMENT CHANGES**

From event timeline (Task 4):

| Date | Change | Person | Reason Disclosed | Assessment | Source |
|------|--------|--------|-----------------|------------|--------|
| Oct 2024 | CFO Retirement | L. Krishnakumar | "Completion of tenure" | ✅ Normal succession | Q2_FY25_Results |
| [List ALL management changes in 5 years...] | | | | | |

**Red Flags:**
- 🔴 **CRITICAL:** CEO/MD resignation with vague reason ("personal reasons" after <3 years)
- 🟠 **HIGH:** CFO change 2+ times in 5 years (instability)
- 🟠 **HIGH:** Multiple independent director resignations in 12 months (board concern?)
- 🟡 **MEDIUM:** 3+ KMP (COO, CTO, business heads) exits in 2 years

**Identified Red Flags:** [List]

---

### **3C: PROMOTER BEHAVIOR**

If disclosed in shareholding patterns:

| Quarter | Promoter Holding % | Promoter Pledge % | QoQ Change (Holding) | QoQ Change (Pledge) | Source |
|---------|-------------------|------------------|---------------------|-------------------|--------|
| Q3 FY26 | [X%] | [Y%] | [Z pp] | [W pp] | Q3_FY26 Shareholding Pattern |
| [Continue for last 20 quarters...] | | | | | |

**Red Flags:**
- 🔴 **CRITICAL:** Promoter pledge >40% of holding (forced selling risk)
- 🟠 **HIGH:** Promoter pledge increasing trend (up >10 pp in 2 years)
- 🟠 **HIGH:** Promoter selling >5% stake in open market in 12 months
- 🟡 **MEDIUM:** Promoter holding declining >3% in year (dilution or exits)

**Identified Red Flags:** [List]

---

## PHASE 4: OPERATIONAL RED FLAGS

### **4A: REVENUE & GROWTH**

From financial tables:

| Quarter | Revenue (Cons) | YoY Growth % | Volume Growth (if disclosed) | Value Growth (if disclosed) | Market Share (if disclosed) | Source |
|---------|---------------|-------------|----------------------------|---------------------------|---------------------------|--------|
| Q3 FY26 | 5,112 | 15% | [X%] | [Y%] | [Z%] | Q3_FY26_Results |
| [Continue...] | | | | | | |

**Red Flags:**
- 🟠 **HIGH:** Revenue declining for 3+ consecutive quarters
- 🟠 **HIGH:** Volume growth negative while value growth positive (pricing not sustainable)
- 🟡 **MEDIUM:** Market share declining >100 bps in year (losing competitively)

**Identified Red Flags:** [List]

---

### **4B: COMMODITY & INPUT COST VOLATILITY**

From transcripts and event timeline:

| Period | Commodity | Price Movement (Quote) | Impact on Margins (Disclosed?) | Management's Response | Source |
|--------|-----------|----------------------|------------------------------|---------------------|--------|
| Q3 FY26 | Coffee | "Arabica $3.40/lb, Robusta $5,400/tonne - 50-year highs" | "Material margin pressure" | "10-13% price increases implemented" | Q3_FY26_Transcript p5 |
| [Continue for ALL commodity mentions...] | | | | | |

**Red Flags:**
- 🔴 **CRITICAL:** Key input cost up >50% YoY with no pricing power disclosed
- 🟠 **HIGH:** Commodity cost inflation mentioned in 4+ consecutive quarters
- 🟡 **MEDIUM:** Management unable to pass through costs (margin compression despite cost increase)

**Identified Red Flags:** [List]

---

### **4C: CUSTOMER/SUPPLIER CONCENTRATION**

From annual report disclosures:

| Year | Top Customer as % of Revenue | Top 5 Customers as % | Top Supplier as % of Purchases | Source |
|------|----------------------------|---------------------|------------------------------|--------|
| FY25 | [X%] (if disclosed) | [Y%] | [Z%] | FY25 AR Notes |

**Red Flags:**
- 🟠 **HIGH:** Single customer >20% of revenue
- 🟡 **MEDIUM:** Top 5 customers >60% of revenue
- 🟡 **MEDIUM:** Single supplier >40% of purchases

**

Identified Red Flags:** [List]

---

## PHASE 5: REGULATORY & LEGAL RED FLAGS

### **5A: REGULATORY ACTIONS**

From event timeline and notes:

| Date | Regulatory Body | Action/Issue | Status | Potential Impact | Source |
|------|----------------|--------------|--------|-----------------|--------|
| [Date] | [SEBI/FDA/etc.] | [Warning letter/show cause/fine] | [Pending/Resolved] | ₹[Amount if quantified] | [Source] |

**Red Flags:**
- 🔴 **CRITICAL:** Product recall or ban
- 🔴 **CRITICAL:** License suspension/revocation (even if temporary)
- 🟠 **HIGH:** Significant fines or penalties imposed (>₹50 cr or >5% of PAT)
- 🟡 **MEDIUM:** Show cause notices or regulatory warnings

**Identified Red Flags:** [List]

---

### **5B: LEGAL & LITIGATION**

From contingent liabilities note:

| Case | Parties | Issue | Amount in Dispute | Status | Company's Assessment | Source |
|------|---------|-------|------------------|--------|---------------------|--------|
| [Case] | TCPL vs [Party] | [Tax/IP/Contract] | ₹[X] cr | [Pending at [Court/Tribunal]] | [Probable loss/Possible loss/Remote] | FY25 AR Note [X] |

**Red Flags:**
- 🔴 **CRITICAL:** "Probable loss" disclosed for large case (>₹100 cr)
- 🟠 **HIGH:** Multiple large lawsuits (>5 cases with individual claim >₹50 cr)
- 🟡 **MEDIUM:** Tax disputes totaling >20% of net worth

**Identified Red Flags:** [List]

---

## PHASE 6: CONSOLIDATED vs STANDALONE-SPECIFIC FLAGS

From RPT/Subsidiary analysis (Task 5):

**Red Flags:**
- 🔴 **CRITICAL:** Standalone PAT > Consolidated PAT (subsidiaries destroying value)
- 🔴 **CRITICAL:** Loss-making subsidiary for 5+ consecutive years with continued parent funding
- 🟠 **HIGH:** Consolidated ROE <Standalone ROE by >5 pp (subsidiaries diluting returns)
- 🟠 **HIGH:** Consolidated Debt significantly > Standalone Debt (subsidiary leverage risk if >50% of Cons debt)
- 🟡 **MEDIUM:** Parent's cumulative investment in subsidiary >₹100 cr with zero dividends received for 5 years

**Check from Task 5 Phase 4A & 5B:**

| Red Flag | Present? | Evidence from Task 5 | Severity | Cross-Reference |
|----------|---------|---------------------|---------|----------------|
| SA PAT > Cons PAT? | [Yes/No] | [If yes: FY25 SA PAT ₹[X] > Cons PAT ₹[Y]] | [🔴/🟠] | Task 5, Phase 4A Table |
| Loss-making sub 5+ yrs? | [Yes/No] | [If yes: [Sub name], cumulative losses ₹[Z]] | [🔴] | Task 5, Phase 3B |
| [Continue for each flag...] | | | | |

**Identified Red Flags:** [List with cross-references to Task 5]

---

## PHASE 7: ACCOUNTING-SPECIFIC FLAGS

From accounting policy analysis (Task 3):

**Red Flags:**
- 🔴 **CRITICAL:** Accounting policy change during weak performance period + High magnitude impact (>10% PAT)
- 🟠 **HIGH:** Multiple policy changes in single year (>3 changes)
- 🟠 **HIGH:** Policy change reversed within 3 years (change then revert)
- 🟡 **MEDIUM:** Frequent restatements (3+ in 5 years)

**Check from Task 3 Phase 8:**

| Red Flag | Present? | Evidence from Task 3 | Severity | Cross-Reference |
|----------|---------|---------------------|---------|----------------|
| Policy change in weak period? | [Yes/No] | [If yes: [Policy], changed in [Year], boosted PAT by ₹[X]] | [🔴/🟠] | Task 3, Phase 4, Change Log Entry #[X] |
| [Continue...] | | | | |

**Identified Red Flags:** [List with cross-references to Task 3]

---

## PHASE 8: COMPREHENSIVE RED FLAG REGISTER

Consolidate ALL red flags from Phases 1-7:

| RF-ID | Category | Red Flag Description | Severity | Evidence (Brief) | Quantified Impact (if available) | First Detected | Current Status | Cross-Reference (Task #) | Source |
|-------|----------|---------------------|---------|-----------------|--------------------------------|----------------|----------------|------------------------|--------|
| RF-001 | Earnings Quality | Cash conversion ratio <70% for 3 years | 🟠 HIGH | FY23-FY25: CFO/PAT = 68%, 65%, 62% | ₹[X] cr working capital drain | FY23 | Worsening | Task 2, Phase 3 | FY23-FY25 Cash Flow Statements |
| RF-002 | Working Capital | Receivables days increased 40 days YoY | 🔴 CRITICAL | Q3 FY26: 145 days vs Q3 FY25: 105 days | ₹[Y] cr additional capital locked | Q3 FY26 | New concern | Task 2, Phase 3 | Q3_FY26_Results |
| RF-003 | Subsidiary | XYZ subsidiary loss-making 5 years | 🔴 CRITICAL | Cumulative losses ₹65 cr, parent invested ₹80 cr | ₹15 cr annual drag on Cons PAT | FY21 | Persistent | Task 5, Phase 3B | FY21-FY25 Subsidiary Schedules |
| [Continue for EVERY red flag identified in Phases 1-7...] | | | | | | | | | |

**Total Red Flags:** [X]

**Severity Breakdown:**
- 🔴 Critical: [Y] flags ([%] of total)
- 🟠 High: [Z] flags ([%] of total)
- 🟡 Medium: [W] flags ([%] of total)
- 🟢 Low/Watch: [V] flags ([%] of total)

---

## PHASE 9: CLUSTERING & INTERCONNECTIONS

**Identify if multiple red flags are symptoms of same underlying issue:**

**CLUSTER #1: Working Capital Deterioration**
- Related Flags: RF-001 (Cash conversion), RF-002 (Receivables days), RF-015 (Inventory days)
- **Root Cause Hypothesis:** [Weak demand → Inventory build-up → Extended credit to push sales → Cash flow squeeze]
- **Severity:** 🔴 **CRITICAL** (3 interconnected critical/high flags)

**CLUSTER #2: Subsidiary Value Destruction**
- Related Flags: RF-003 (Loss-making sub), RF-024 (SA PAT > Cons PAT), RF-031 (Cons ROE < SA ROE)
- **Root Cause Hypothesis:** [Poor capital allocation → Continued funding of weak subsidiary → Dilution of shareholder returns]
- **Severity:** 🔴 **CRITICAL** (3 interconnected critical flags)

[Identify 3-5 such clusters if patterns exist]

---

## PHASE 10: PRIORITIZATION FOR STAGE 3

**Top 10 Red Flags Requiring Immediate Deep-Dive in Opus Analysis:**

1. **RF-[ID]** - [Brief description] - Severity: 🔴 - Why critical: [1 sentence]
2. **RF-[ID]** - [Brief description] - Severity: 🔴 - Why critical: [1 sentence]
3. [Continue through top 10...]

**Rationale for Prioritization:**
- Severity (Critical first)
- Magnitude (Quantified financial impact)
- Trend (Worsening vs stable)
- Clustering (Multiple related flags)

---

## PHASE 11: FALSE POSITIVE ASSESSMENT

**Estimate false positive rate:**

"Of [X] total red flags identified, approximately [Y]% may be false positives requiring verification in Stage 3.

**High-Confidence Red Flags (Low false positive risk):**
- [List RF-IDs with strong evidence from multiple sources, clear regulatory violations, or objective metrics breached]
- Example: RF-002 (Receivables days 145, vs sector median 70 - clear outlier)

**Moderate-Confidence Flags (Moderate false positive risk):**
- [List RF-IDs based on single-source data or industry-standard practices that may be legitimate]
- Example: RF-015 (Inventory days up 20, but may be strategic pre-season stocking)

**Low-Confidence Flags (High false positive risk):**
- [List RF-IDs based on assumptions or incomplete data]
- Example: RF-028 (Goodwill >20%, but may be legitimate if acquisitions are performing well)

**Recommendation:** Stage 3 (Opus) should verify all flags, but prioritize high-confidence flags first."

---

## PHASE 12: VERIFICATION CHECKLIST

- [ ] I scanned ALL financial tables for earnings quality issues
- [ ] I checked ALL balance sheet items for asset/liability red flags
- [ ] I reviewed ALL auditor reports for opinion/EOM/qualifications
- [ ] I tracked ALL management changes in 5 years
- [ ] I identified ALL regulatory/legal issues from notes and timeline
- [ ] I checked for commodity/operational risks from transcripts
- [ ] I flagged ALL Cons vs SA-specific issues from Task 5
- [ ] I flagged ALL accounting-specific issues from Task 3
- [ ] I created comprehensive red flag register with severity classification
- [ ] I identified clusters and interconnections
- [ ] I prioritized top 10 for Stage 3 deep-dive
- [ ] I assessed false positive likelihood
- [ ] I cited sources for EVERY red flag

**If ANY box unchecked → GO BACK and complete.**

---

**OUTPUT:** All 12 phases sequentially. Estimated length: 18-25 pages.

This is the alert system - MUST be comprehensive to ensure nothing material is missed.
```

---

## Output Files

**After completing all 7 prompts, save outputs to:**

```
01_Stage1_NotebookLM_Outputs/
├── 01_notebooklm_document_map.txt
├── 02_notebooklm_financial_tables.txt
├── 03_notebooklm_accounting_policies.txt
├── 04_notebooklm_event_timeline.txt
├── 05_notebooklm_rpt_subsidiaries.txt
├── 06_notebooklm_guidance_tracker.txt
└── 07_notebooklm_red_flags_prescreened.txt
```

---

## Quality Verification

Before proceeding to Stage 2:

- [ ] All 7 outputs saved and named correctly
- [ ] Financial tables include BOTH Consolidated AND Standalone
- [ ] Source citations are page-level (not just document name)
- [ ] No [VERIFY] flags left unaddressed
- [ ] 5-year data is complete (FY20-FY24/25)

---

## Next Steps

After completing all NotebookLM prompts:

1. **Save all 7 outputs** to `01_Stage1_NotebookLM_Outputs/` folder
2. **Review outputs** for completeness and accuracy
3. **Proceed to Stage 2** — [ENGINE 00B (Gemini DR)](engine_00B__qtrly_results_audit_gemini_dr.md)
4. **Update execution log** with Stage 1 completion time

---

## Time & Cost Estimates

| Prompt | Expected Time | Output Length |
|--------|---------------|---------------|
| Prompt 1: Document Map | 3-5 minutes | 2-3 pages |
| Prompt 2: Financial Tables | 8-12 minutes | 8-12 pages |
| Prompt 3: Accounting Policies | 5-8 minutes | 4-6 pages |
| Prompt 4: Event Timeline | 5-8 minutes | 5-8 pages |
| Prompt 5: RPT & Subsidiaries | 6-10 minutes | 6-10 pages |
| Prompt 6: Guidance Tracker | 5-8 minutes | 5-8 pages |
| Prompt 7: Red Flags | 10-15 minutes | 18-25 pages |
| **Total** | **42-66 minutes** | **48-72 pages** |

**Cost**: FREE (NotebookLM is free to use)

---

## Troubleshooting

**If output is too shallow:**
- Re-run prompt with emphasis on specific sections
- Add "DO NOT SKIP" reminders for critical sections

**If citations are vague:**
- Ask NotebookLM to re-cite with page numbers
- Verify against original documents manually

**If Consolidated vs Standalone is missing:**
- Re-run Prompt 2 with explicit demand for both

---
