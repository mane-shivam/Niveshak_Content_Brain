# 🏥 MODEL HEALTH LOG

**Purpose**: Track AI model performance degradation to prevent silent quality decay

---

## TRACKING SCHEMA

| Date | Engine | Model | Issue Type | Severity | Evidence | Action Taken | Resolved |
|------|--------|-------|------------|----------|----------|--------------|----------|
| _Example: 22 Jan 2026_ | _Research Desk_ | _Gemini Deep Research_ | _Data hallucination_ | _Medium_ | _Fabricated Q2 number for XYZ Ltd_ | _Switched to dual-verification protocol_ | _Yes_ |

---

## ISSUE TYPES

**Data Issues**:
- Hallucinations (fabricated numbers/sources)
- Math errors (calculation mistakes)
- Source errors (citing non-existent docs)

**Voice Issues**:
- Tone drift (less institutional)
- Banned AI tells creeping in
- Hype language appearing

**Logic Issues**:
- Contradictory reasoning
- Missing obvious counterarguments
- Framework misapplication

**Wrapper Issues** (Perplexity, Antigravity):
- Quality degradation
- Interface bugs
- Search result hallucinations

---

## SEVERITY LEVELS

**Low**: One-off error, easily caught, no impact on published content  
**Medium**: Recurring pattern, requires attention, caught before publishing  
**High**: Made it past quality gates, public correction needed  
**Critical**: Systematic model failure, immediate replacement required

---

## ALERT THRESHOLDS

**Flag for Investigation**:
- >2 Medium issues in same engine within 1 month
- Any High severity issue
- >5 Low issues in same engine within 1 month

**Model Replacement Trigger**:
- Any Critical issue
- >3 High issues in 2 months
- Consistent degradation trend over 6 weeks

---

## BENCHMARK PROTOCOL

When model flagged for investigation:

1. **Re-run Standard Test**:
   - Feed same prompt from 4 weeks ago
   - Compare output quality
   - Measure degradation

2. **Alternative Model Test**:
   - Run same task with competitor model
   - Compare results
   - Document performance delta

3. **Decision Matrix**:
   - If alternative >20% better → Switch
   - If alternative 10-20% better → Run A/B for 2 weeks
   - If alternative <10% better → Monitor current model 2 more weeks

---

## WEEKLY HEALTH CHECK TEMPLATE

**Week of**: [DD MMM - DD MMM YYYY]

**Engines Used This Week**:
- [ ] Chief Strategist — Health: [Good / Flag / Investigate]
- [ ] Research Desk — Health: [Good / Flag / Investigate]
- [ ] Signal Collector — Health: [Good / Flag / Investigate]
- [ ] Red Team — Health: [Good / Flag / Investigate]
- [ ] Platform Adapter — Health: [Good / Flag / Investigate]
- [ ] Comment Engine — Health: [Good / Flag / Investigate]

**Issues This Week**: [Count]  
**Flags Raised**: [List]  
**Action Items**: [List]

---

**Last Updated**: [Date] | **Total Issues Logged**: [Count] | **Models Replaced**: [Count]
