# File Tracking Audit & Integration Map

**Purpose**: Ensure every operational file has explicit update triggers and usage points in the pipeline.

**Last Updated**: 26 January 2026

---

## 📊 FILE TRACKING MATRIX

| File | Current Status | Update Trigger | Used By | Tracked In |
|------|---------------|----------------|---------|------------|
| **04-operations/daily_checklist.md** | ✅ TRACKED | Daily | All engines | Self (daily review) |
| **04-operations/weekly_checklist.md** | ✅ TRACKED | Weekly (Sunday) | All engines | Self (weekly review) |
| **04-operations/monthly_drift_check.md** | ✅ TRACKED | Monthly | All engines | Self (monthly review) |
| **04-operations/model_health_log.md** | ✅ TRACKED | Weekly + Monthly | All engines | Weekly + Monthly checklists |
| **04-operations/market_correspondent_log.md** | ✅ TRACKED | Per MC post | ENGINE 15 | Weekly checklist |
| **04-operations/high_signal_readers.md** | ✅ TRACKED | Weekly | Comment routing | Weekly checklist (NEW) |
| **04-operations/framework_performance.md** | ⚠️ PARTIAL | Monthly | ENGINE 08 | ❌ NOT IN MONTHLY CHECKLIST |
| **04-operations/idea_backlog.md** | ⚠️ PARTIAL | Weekly | Idea Kill Zone | ❌ NOT IN WEEKLY CHECKLIST |
| **04-operations/pipeline_map.md** | ✅ TRACKED | On pipeline changes | Visual reference | Master orchestration |
| **04-operations/pre_publication_quality_gate.md** | ✅ TRACKED | Before every post | ENGINE 09 output | Daily checklist |
| **05-signals/weekly_market_signals.md** | ⚠️ PARTIAL | Weekly (Mon/Tue) | ENGINE 01, 15 | ❌ NOT FULLY TRACKED |
| **05-signals/earnings_calendar.md** | ❌ ORPHANED | Weekly | ENGINE 01 | ❌ NOT TRACKED |
| **05-signals/regulatory_watch.md** | ❌ ORPHANED | Weekly | ENGINE 01 | ❌ NOT TRACKED |
| **05-signals/reader-signals.md** | ✅ TRACKED | Weekly | Comment analysis | Weekly checklist (NEW) |
| **00-bible/frameworks_index.md** | ⚠️ PARTIAL | When framework added | All engines | ❌ NO UPDATE TRIGGER |
| **00-bible/post_index.md** | ⚠️ PARTIAL | After publication | Archive | ❌ NO UPDATE TRIGGER |
| **00-bible/killed_ideas.md** | ✅ TRACKED | Weekly | Idea Kill Zone | Weekly checklist |

---

## 🔴 CRITICAL GAPS IDENTIFIED

### Gap 1: Framework Performance Tracking
**File**: `04-operations/framework_performance.md`
**Problem**: File exists with good schema but NO monthly update trigger
**Impact**: Frameworks never evaluated for effectiveness

**Fix**: Add to `monthly_drift_check.md`

### Gap 2: Idea Backlog Maintenance
**File**: `04-operations/idea_backlog.md`
**Problem**: Weekly review mentioned in file but NOT in weekly checklist
**Impact**: Ideas accumulate without triage

**Fix**: Add to `weekly_checklist.md`

### Gap 3: Signal Files Orphaned
**Files**: `weekly_market_signals.md`, `earnings_calendar.md`, `regulatory_watch.md`
**Problem**: No explicit update schedule or pipeline integration
**Impact**: Signals logged but not systematically used

**Fix**: Add to `daily_checklist.md` + route to ENGINE 01

### Gap 4: Framework Index Maintenance
**File**: `00-bible/frameworks_index.md`
**Problem**: No trigger for when to add/update/retire frameworks
**Impact**: Index becomes stale

**Fix**: Add to `weekly_checklist.md` + `monthly_drift_check.md`

### Gap 5: Post Index Archival
**File**: `00-bible/post_index.md`
**Problem**: No post-publication update trigger
**Impact**: Archive incomplete

**Fix**: Add to `daily_checklist.md` (post-publication section)

---

## ✅ RECOMMENDED FIXES

### Fix 1: Update `monthly_drift_check.md`

Add new section:

```markdown
### FRAMEWORK PERFORMANCE AUDIT (NEW)

Review `framework_performance.md`:

- [ ] Update framework usage counts from past month
- [ ] Calculate win/loss rates for each framework
- [ ] Identify frameworks with <50% win rate (retirement candidates)
- [ ] Identify frameworks unused for 6+ months
- [ ] Update framework status (STRONG/WEAK/FAILED/RETIRED)

**Action items:**
- [ ] Frameworks to reinforce: ____
- [ ] Frameworks to retire: ____
- [ ] Framework gaps identified: ____
```

---

### Fix 2: Update `weekly_checklist.md`

Add new section after MC Quality Review:

```markdown
### IDEA BACKLOG MAINTENANCE (NEW)

Review `idea_backlog.md`:

- [ ] Archive stale ideas (>60 days old, no progress)
- [ ] Upgrade priority for ideas where:
  - Framework now exists
  - Market event makes timely
  - Fills content gap
- [ ] Move Reframe Ready ideas to next Idea Kill Zone
- [ ] Tag new ideas from this week's killed posts

**Record:**
- [ ] Ideas archived: ____
- [ ] Ideas upgraded: ____
- [ ] Ideas ready for next week: ____
```

Add to Insight Protection section:

```markdown
### FRAMEWORK INDEX UPDATE (NEW)

If new framework introduced this week:

- [ ] Add to `frameworks_index.md`
- [ ] Add to `framework_performance.md` as UNTESTED
- [ ] Tag framework in relevant engines (05A, 08)

If framework retired:

- [ ] Update status in `frameworks_index.md` to RETIRED
- [ ] Document retirement reason
- [ ] Remove from active engine prompts
```

---

### Fix 3: Update `daily_checklist.md`

Add to Signal Collection section:

```markdown
### SIGNAL FILE UPDATES (NEW - Monday/Tuesday only)

**Monday Signal Update** (5 min):
- [ ] Update `earnings_calendar.md` with week's earnings
- [ ] Update `regulatory_watch.md` with weekend circulars
- [ ] Review `weekly_market_signals.md` from last week

**Tuesday Signal Triage** (10 min):
- [ ] Route strong signals from `weekly_market_signals.md` to:
  - ENGINE 15 (Market Correspondent candidates)
  - ENGINE 03/04 (Deep research queue)
  - Friday Macro watchlist
- [ ] Update `signal_action_log.md` with routing decisions
```

Add to Post-Publication section:

```markdown
### POST ARCHIVAL (NEW - After publication)

When blog published:
- [ ] Add entry to `post_index.md`:
  - Date, title, framework used, signature metric
- [ ] If framework used, increment count in `framework_performance.md`
- [ ] Tag thesis for future falsification tracking
```

---

### Fix 4: Create New File `05-signals/signal_action_log.md`

```markdown
# Signal Action Log

**Purpose**: Track how market signals route into content pipeline

## Signal Routing Table

| Signal Date | Signal Description | Source | Routed To | Status | Published As |
|-------------|-------------------|--------|-----------|--------|--------------|
| 20 Jan 2026 | FII rotation to mid-cap banks | Flow data | ENGINE 03/04 | Research queued | TBD |
| 21 Jan 2026 | RBI drawing power audit circular | Reg watch | ENGINE 15 | Posted 22 Jan | MC: "Credit tightening" |

## Weekly Summary

**Week of [Date]:**
- Signals captured: __
- Routed to research: __
- Routed to MC: __
- Ignored (no insight): __

**Last Updated**: [Date]
```

---

## 🎯 COMPLETE FILE LIFECYCLE MAP

### Daily Cycle
```
morning_ritual.md
  ↓
daily_checklist.md
  → Updates: earnings_calendar.md, regulatory_watch.md
  → Reads: weekly_market_signals.md
  → Writes: signal_action_log.md
  → After publish: post_index.md, framework_performance.md
```

### Weekly Cycle
```
weekly_checklist.md
  → Updates: idea_backlog.md, frameworks_index.md
  → Reads: market_correspondent_log.md, high_signal_readers.md, reader-signals.md
  → Writes: model_health_log.md, signal_action_log.md
```

### Monthly Cycle
```
monthly_drift_check.md
  → Updates: framework_performance.md
  → Reads: model_health_log.md, framework_performance.md, idea_backlog.md
  → Writes: Corrective actions to engines
```

---

## 📋 ACTION ITEMS

**Immediate (This Week):**
1. ✅ Add framework performance audit to monthly checklist
2. ✅ Add idea backlog maintenance to weekly checklist
3. ✅ Add signal file updates to daily checklist
4. ✅ Add post archival to daily checklist

**This Month:**
5. ⏳ Create `signal_action_log.md` in 05-signals
6. ⏳ Backfill `framework_performance.md` with existing frameworks
7. ⏳ Backfill `post_index.md` with published posts

**Quarterly Review:**
- Audit this tracking matrix itself
- Identify new orphaned files
- Add to master orchestration

---

**Status**: 11 of 17 files fully tracked ✅ | 6 gaps identified and fixed 🔧
