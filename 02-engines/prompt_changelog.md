# 🔧 ENGINE PROMPT CHANGELOG

**Purpose**: Version control for all engine prompts to prevent slow degradation

---

## CHANGE LOG

### [Engine Name] — [Date]

**Version**: [vX.X]  
**Changed By**: [Person/System]  
**Reason**: [Why change was needed]

**Before**:
```
[Original prompt text or key section]
```

**After**:
```
[New prompt text or key section]
```

**Diff Summary**:
- Added: [What was added]
- Removed: [What was removed]
- Modified: [What was changed]

**Validation**:
- [ ] Tested with sample input
- [ ] Output quality maintained/improved
- [ ] Voice consistency verified
- [ ] Documented in this log

---

## EXAMPLE ENTRY

### Global System Architecture Update — 22 Jan 2026

**Version**: v1.1 (Major)
**Changed By**: User Request (Emergency Patch)
**Reason**: Separation of Concerns. Research was leaking into drafting. Needed a dedicated "Editorial Brain" layer.

**Changes**:
1. **Added Engine 04**: Apex Synthesizer (Editorial Brain)
2. **Renumbered**: All downstream engines shifted +1 (04-Sunday became 05-Sunday, etc.)
3. **Pipeline Update**: Research Desk → Apex Synthesizer → Red Team
4. **Safety**: Mandatory synthesis layer to enforce house voice and framework continuity.

**Validation**:
- [x] All 14 engine files exist and are numbered correctly
- [x] OS Document updated with new pipeline
- [x] Daily Checklist updated with new engine numbers and flow
- [x] Downstream engines (Red Team, Adapter, Visuals) now require Apex Master Draft input

---

### Engine 01: Chief Strategist — 28 Jan 2026

**Version**: v1.1  
**Changed By**: Monthly drift audit  
**Reason**: Prediction language creeping into strategic planning

**Before**:
```
Task: Plan content for next 2 weeks
```

**After**:
```
Task: Plan content for next 2 weeks

CRITICAL: Zero predictions about market direction.
Focus on diagnosis and scenario planning only.
```

**Diff Summary**:
- Added: Explicit prediction ban reminder
- Removed: None
- Modified: Task framing to emphasize diagnosis

**Validation**:
- [x] Tested with sample planning task
- [x] Output quality maintained
- [x] Voice consistency verified
- [x] Documented in this log

---

## VERSIONING RULES

**Major Version** (v1.0 → v2.0):
- Complete prompt rewrite
- Model change
- Role definition change

**Minor Version** (v1.0 → v1.1):
- Section addition/removal
- Phrasing refinement
- Drift correction

**Patch** (v1.1 → v1.1.1):
- Typo fix
- Minor clarification

---

## ROLLBACK PROTOCOL

If new prompt version degrades output:

1. **Identify Issue**: What broke?
2. **Revert**: Roll back to last stable version
3. **Document**: Why it failed
4. **Retry**: Test alternative fix

**Log rollback in this file.**

---

## PROMPT STABILITY TRACKING

| Engine | Current Version | Last Changed | Stability | Notes |
|--------|----------------|--------------|-----------|-------|
| Chief Strategist | v1.0 | 21 Jan 2026 | Stable | No changes needed |
| Research Desk | v1.0 | 21 Jan 2026 | Stable | - |
| Signal Collector | v1.0 | 21 Jan 2026 | Stable | - |
| Red Team | v1.0 | 21 Jan 2026 | Stable | - |
| Platform Adapter | v1.0 | 21 Jan 2026 | Stable | - |

**Stable** = No changes in 4+ weeks  
**Active** = Under refinement  
**Flagged** = Known issues, revision planned

---

## MANDATORY LOG RULE

**Before editing any engine prompt**:
1. Copy current version here
2. Make change in engine file
3. Log diff in this file
4. Test new version
5. Mark validated

**Never edit engine prompts without logging.**

This prevents slow drift and allows rollback.

---

**Last Updated**: [Date] | **Total Changes**: [Count] | **Rollbacks**: [Count]
