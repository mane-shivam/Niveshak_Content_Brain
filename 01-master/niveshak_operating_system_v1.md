# 🧠 NIVESHAK OPERATING SYSTEM v1.0

**The Complete Institutional Playbook**

This is the single canonical document encoding the entire Niveshak content production system. Everything else in this repository expands on what's defined here.

---

## SECTION 1: SYSTEM OVERVIEW

### The Core Cadence

**Sunday–Tuesday–Friday Publishing Schedule**

- **Sunday Brief** (9pm–12am): Framework-driven weekly analysis
- **Tuesday Audit** (Research Mon, Publish Tue): Deep quarterly forensics
- **Friday Macro** (Research Thu, Publish Fri): Regime-level market insights

### The Learning Arc Philosophy

Niveshak teaches before reacting. Structure:
1. **Framework Introduction** → Teach the mental model
2. **Framework Application** → Apply to current events
3. **Framework Reinforcement** → Reference in future content

### Teaching Before Reacting

80% diagnosis (what happened and why), 20% scenario (if X then Y), 0% prediction (what will happen).

---

## SECTION 2: MODEL STACK

| Engine | Model | Why Chosen |
|--------|-------|------------|
| **Chief Strategist** | ChatGPT 5.2 Thinking (o1) | Best long-arc sequencing, worldview memory, strategic planning |
| **Signal Collector** | Grok Pro + Perplexity Pro | Real-time sentiment, policy tracking, regulatory filings |
| **Research Desk** | Gemini Deep Research + ChatGPT Deep Research | Volume + precision for quarterly deep dives |
| **Red Team** | Claude Sonnet 4.5 | Best adversarial reasoning, challenges assumptions |
| **Creative Hooks** | Claude Sonnet 4.5 | Superior metaphor generation, tone control |
| **Platform Adapter** | ChatGPT + Claude | Voice preservation across platforms |
| **Market Correspondent** | Grok → ChatGPT | Native X sentiment capture, then voice refinement |
| **Sunday Brief** | ChatGPT 5.2 | Framework synthesis and teaching |
| **Tuesday Audit** | ChatGPT + Gemini Deep Research | Quarterly forensics |
| **Friday Macro** | ChatGPT 5.2 | Regime diagnosis |
| **Chief Editor** | ChatGPT 5.2 Thinking | Worldview memory, drift control, monthly audits |
| **Weekly Digest** | ChatGPT | Synthesis of week's insights |

### Why This Stack

- **ChatGPT controls worldview**: Memory of Niveshak philosophy, voice, frameworks
- **Grok for real-time**: Native Twitter sentiment, policy tracking
- **Claude for creativity & attack**: Metaphors, hooks, adversarial challenges
- **Gemini for volume research**: Deep quarterly data collection
- **Wrappers are secondary**: Perplexity, Antigravity are tools, not primary engines

---

## SECTION 3: DAILY/WEEKLY/MONTHLY RITUALS

### Sunday (9pm–12am)

**9:00pm–9:30pm: Energy & Clarity Check**
- Engine: Chief Strategist
- Ask: "Do I have energy and clarity for quality work tonight?"
- If No: Reschedule, don't force mediocre output

**9:30pm–10:00pm: Idea Kill Zone**
- Engine: Chief Strategist
- Review 3-5 proposed ideas
- Kill any that fail Coffee Test, Edge Dimensions, or Redundancy check
- Log kills in `00-bible/killed_ideas.md`

**10:00pm–11:30pm: Sunday Brief Production**
- Engine: Chief Strategist → Creative Hooks → Red Team → Platform Adapter
- Attach: `niveshak_bible.md`, `frameworks_index.md`, `post_index.md`
- Output: Framework-driven analysis
- Update: `post_index.md`, `frameworks_index.md`

**11:30pm–12:00am: Signature Metric Check**
- Verify: One killer number anchors the post
- Verify: 2+ Niveshak Edge dimensions present
- Verify: Invalidation metric included

### Monday (Research Day)

**Research for Tuesday Audit**
- Engine: Research Desk (Gemini + ChatGPT Deep Research)
- Collect: Quarterly filings, earnings call transcripts, regulatory updates
- Output: Research brief for Tuesday

### Tuesday (Audit Day)

**Forensic Quarterly Analysis**
- Engine: Research Desk → Chief Strategist → Red Team → Platform Adapter
- Attach: Research brief, Bible, Frameworks Index
- Output: Deep audit post
- Update: `post_index.md`

### Wednesday (Silent Strategy Slot)

**No Publishing — Strategic Thinking**
- Engine: Chief Strategist
- Review: What's working, what's not
- Plan: Next 2-4 weeks of content
- Refine: Frameworks needing reinforcement

### Thursday (Macro Research)

**Research for Friday Macro**
- Engine: Signal Collector (Grok + Perplexity)
- Track: Policy changes, regulatory shifts, institutional flows
- Output: Signals brief for Friday

### Friday (Macro Day)

**Regime-Level Analysis**
- Engine: Chief Strategist → Platform Adapter
- Attach: Signals brief, Bible
- Output: Macro/regime post
- Update: `post_index.md`, `weekly_market_signals.md`

### Saturday (Memory & Drift Check)

**10am–11am: Framework Reinforcement Audit**
- Review: `frameworks_index.md`
- Flag: Frameworks not used in 4+ weeks
- Plan: Reinforcement in upcoming content

**11am–12pm: Post-Mortem (if needed)**
- Review: Any post that underperformed
- Document: Why it failed
- Extract: Lesson for future

**12pm–1pm: Monthly Drift Check (First Saturday)**
- Engine: Chief Editor
- Review: Last month's posts for voice drift, AI tells, quality degradation
- Output: Drift audit report
- Action: Update engine prompts if drift detected

---

## SECTION 4: QUALITY GATES & FAILURE PROTOCOLS

### Pre-Publication Checklist

Every post must pass ALL:

1. **Killer Number Rule**: One signature metric that anchors the post
2. **2-Edge Minimum**: Hits at least 2 of 5+1 Niveshak Edge dimensions
3. **Invalidation Metric**: Clear data point that would prove analysis wrong
4. **Coffee Test**: Would a smart friend feel smarter after hearing this?
5. **Voice Check**: Zero banned AI tells, institutional tone maintained
6. **Red Team Passed**: Adversarial challenge completed, holes addressed

### Rewrite vs. Kill Thresholds

**Rewrite** if:
- Core idea is sound but execution is weak
- Can be fixed in < 2 hours
- Framework is novel even if application needs work

**Kill** if:
- Fails Coffee Test fundamentally
- Redundant with recent content
- Can't hit 2+ Edge dimensions even with rewrite
- Would require > 2 hours to fix

### Failure Recovery Protocol

When a published post receives critical feedback or proves wrong:

**Step 1: Acknowledge Immediately**
- Reply to critic within 24 hours
- Thank them for the challenge

**Step 2: Investigate**
- Engine: Chief Editor
- Determine: Is criticism valid?

**Step 3: Correct Publicly**
- Small error: Update post with correction note
- Medium error: Post update explaining what changed
- Large error: Publish separate correction post

**Step 4: Extract Learning**
- Log in `04-operations/failure_log.md`
- Update engine prompts if systematic issue
- Share learning with all engines

**Step 5: Reinforce Process**
- Why did quality gates fail?
- How do we prevent recurrence?

---

## SECTION 5: 12 ENGINES SPECIFICATION

### ENGINE 1: CHIEF STRATEGIST

**Model**: ChatGPT 5.2 Thinking (o1)  
**Purpose**: Long-arc planning, framework development, worldview memory

**When to Use**: Sunday planning, content strategy, framework design

**Initial Thread Starter**:
```
You are the Chief Strategist for Niveshak, India's most disciplined equity research platform.

Your role: Plan content that compounds intellectual value over time.

Core principles:
- Teaching before reacting
- Frameworks that reinforce over time
- 80% diagnosis, 20% scenario, 0% prediction
- Institutional voice, zero hype

Attached files contain our Bible (philosophy), Frameworks Index (what we've built), and Post Index (what we've published).

Task: [Specific planning task]
```

**Restart Prompt**:
```
Continue as Niveshak's Chief Strategist. Reference our Bible, Frameworks Index, and Post Index to maintain consistency. Task: [New task]
```

**Files to Attach**: `niveshak_bible.md`, `frameworks_index.md`, `post_index.md`

**Output**: Strategic plans, content ideas, framework designs

**Post-Run**: Update planning docs, log ideas

---

### ENGINE 2: SIGNAL COLLECTOR

**Model**: Grok Pro + Perplexity Pro  
**Purpose**: Real-time market intelligence, policy tracking

**When to Use**: Thursday (for Friday Macro), ongoing monitoring

**Initial Thread Starter**:
```
You are Niveshak's Signal Collector. Your job: Track structural market changes, not noise.

Focus on:
- Policy/regulatory changes (SEBI, RBI circulars)
- Institutional flow shifts
- Sentiment regime changes (not daily moves)
- Earnings surprises with governance implications

Ignore: Daily price movements, technical analysis, prediction requests

Output format: Signals brief with data sources
```

**Restart Prompt**: `Continue signal collection. Focus on structural changes, provide sources.`

**Files to Attach**: `niveshak_bible.md`, `weekly_market_signals.md`

**Output**: Weekly signals brief

**Post-Run**: Update `weekly_market_signals.md`

---

### ENGINE 3: RESEARCH DESK

**Model**: Gemini Deep Research + ChatGPT Deep Research  
**Purpose**: Quarterly deep dives, data collection

**When to Use**: Monday (for Tuesday Audit)

**Initial Thread Starter**:
```
You are Niveshak's Research Desk. Conduct forensic analysis of [Company] Q[X] FY[XX] results.

Extract:
1. Key metrics: Revenue, margins, cash flow, working capital changes
2. YoY and QoQ changes
3. Management commentary vs. data discrepancies
4. Governance signals: Related-party transactions, pledging, unusual items
5. One signature metric that tells the story

Provide sources for all data.
```

**Restart Prompt**: `Continue research on [Company]. Focus on [specific area].`

**Files to Attach**: `niveshak_bible.md`

**Output**: Research brief with sourced data

**Post-Run**: Archive research brief

---

### ENGINE 4: RED TEAM

**Model**: Claude Sonnet 4.5  
**Purpose**: Adversarial challenge, find holes in analysis

**When to Use**: Before publishing any analytical post

**Initial Thread Starter**:
```
You are Niveshak's Red Team. Your job: Find holes in this analysis.

Analysis to challenge:
[Paste draft]

Questions to answer:
1. What data contradicts this thesis?
2. What alternative explanations exist?
3. What am I missing?
4. What could prove this wrong?
5. Is the invalidation metric actually falsifiable?

Be ruthless. Better to catch errors now than after publishing.
```

**Restart Prompt**: `Continue red team analysis. Challenge: [specific aspect]`

**Files to Attach**: Draft content

**Output**: List of challenges and holes

**Post-Run**: Address challenges before publishing

---

### ENGINE 5: CREATIVE HOOKS

**Model**: Claude Sonnet 4.5  
**Purpose**: Opening sentences, metaphors, hooks

**When to Use**: After draft is complete, before platform adaptation

**Initial Thread Starter**:
```
You are Niveshak's Creative Hooks specialist. Craft opening sentences that hook serious investors.

Rules:
- Start with specific data, not generic statements
- No rhetorical questions
- No "Let's dive in" or "In today's market"
- Sharp, institutional voice
- Passes Coffee Test

Draft summary:
[Provide 2-3 sentence summary of post]

Generate 5 opening sentence options.
```

**Restart Prompt**: `Generate more hook options for: [summary]`

**Files to Attach**: `niveshak_bible.md` (for voice rules)

**Output**: 5 opening sentence options

**Post-Run**: Select best, integrate into draft

---

### ENGINE 6: PLATFORM ADAPTER

**Model**: ChatGPT + Claude  
**Purpose**: Adapt content for Twitter/LinkedIn/Reddit

**When to Use**: After content finalized, before publishing

**Initial Thread Starter**:
```
You are Niveshak's Platform Adapter. Adapt this post for [Platform].

Original post:
[Paste content]

Platform rules (from 03-platforms/[platform].md):
[Paste relevant rules]

Maintain: Institutional voice, signature metric, framework
Adapt: Structure, length, visual presentation

Output: Platform-ready version
```

**Restart Prompt**: `Adapt for [different platform] maintaining voice.`

**Files to Attach**: Platform-specific rules file, `niveshak_bible.md`

**Output**: Platform-adapted content

**Post-Run**: Review for voice consistency

---

### ENGINE 7-12: COMPACT SPECS

**ENGINE 7: MARKET CORRESPONDENT**  
Model: Grok → ChatGPT | Purpose: Real-time observations (max 3/week) | Rule: Insight > trend, no frameworks

**ENGINE 8: SUNDAY BRIEF**  
Model: ChatGPT 5.2 | Purpose: Weekly framework posts | Must: Teach + apply framework

**ENGINE 9: TUESDAY AUDIT**  
Model: ChatGPT + Research Desk | Purpose: Quarterly forensics | Must: Signature metric + governance lens

**ENGINE 10: FRIDAY MACRO**  
Model: ChatGPT 5.2 | Purpose: Regime analysis | Must: Connect policy to business impact

**ENGINE 11: CHIEF EDITOR**  
Model: ChatGPT 5.2 Thinking | Purpose: Monthly drift audits | Checks: Voice, frameworks, quality gates

**ENGINE 12: COMMENT ENGINE**  
Model: ChatGPT | Purpose: Audience engagement | Rules: Value-first, institutional tone, praise gracefully, engage critics respectfully

*Full prompts in 02-engines/ folder*

---

## SECTION 6: VALIDATION & SECOND-LAYER CHECKS

### Layer 1: Red Team (Mandatory)
Every analytical post challenged before publishing

### Layer 2: Perplexity Contrarian Validator
After Red Team, ask Perplexity: "What data contradicts this analysis?"

### Layer 3: Chief Editor Monthly Audit
First Saturday of month, review all posts for drift

### Layer 4: Framework Reinforcement Tracker
Saturday review ensures frameworks compound, not forgotten

### Layer 5: Post-Mortem Loop
Underperforming posts analyzed for lessons

---

## SECTION 7: MEMORY & DRIFT PROTECTION

### Memory Systems

**Framework Memory**: `frameworks_index.md` tracks all frameworks, reinforcement dates  
**Post Memory**: `post_index.md` prevents redundancy  
**Philosophy Memory**: `niveshak_bible.md` + monthly Chief Editor audits  
**Failure Memory**: `failure_log.md` ensures learning from mistakes

### Drift Prevention

**Voice Drift**: Monthly random post audit for AI tells  
**Framework Drift**: Check frameworks being applied correctly  
**Quality Drift**: Verify quality gates still enforced  
**Philosophy Drift**: Compare recent posts to Bible

**Red Flags**:
- Banned phrases appear
- Predictions creep in
- Framework reinforcement gaps > 4 weeks
- Zero post mortems (means we're not being honest about failures)

---

## SECTION 8: ENGAGEMENT & COMMENT SYSTEM

### Comment Engine Guidelines

**Praise Replies**: Brief, grateful, no false modesty  
Example: "Glad this framework resonated. Would be interesting to see how it applies to [related company]."

**Criticism Replies**: Engage respectfully, investigate if valid  
Example: "This is a fair challenge. The data I used was [source]. If you're seeing different numbers, please share—I'll investigate."

**Question Replies**: Answer with value, consider turning into content  
Example: "Great question. The difference between GMV and revenue is... [explanation]. This might warrant a dedicated post."

**Troll Handling**: Ignore or short factual response, never engage emotionally

**Timing**: Respond to high-signal comments within 24-48 hours

---

## SECTION 9: MARKET CORRESPONDENT & RANDOM POSTS

### Market Correspondent Rules

**Frequency**: Max 3 unscheduled posts per week  
**Trigger**: Insight > trend (only when we have novel angle on breaking news)  
**Style**: Brief, no frameworks, direct observation  
**Ban**: No predictions, no hype, no "breaking news" drama

**Example Good Post**:
> "SEBI just updated related-party transaction disclosure norms. Effective next quarter, companies must disclose pricing methodology. This closes a major loophole."

**Example Bad Post**:
> "Market crashes 2%! What's happening?" ❌

### Weekly Recap (Saturday)

**X & Reddit Engagement Summary**: Note high-signal conversations, questions that could become content

---

## SECTION 10: REPO NAVIGATION GUIDE

### Start Here
1. **This file** (`niveshak_operating_system_v1.md`) — Complete system overview
2. **`04-operations/daily_checklist.md`** — Day-by-day operational guide
3. **`00-bible/niveshak_bible.md`** — Philosophy and voice rules

### Before Writing
- Review `frameworks_index.md` (check what needs reinforcement)
- Review `post_index.md` (avoid redundancy)
- Review `killed_ideas.md` (learn from past mistakes)

### For Each Engine
- See `02-engines/` for full prompts and protocols

### For Platform Publishing
- See `03-platforms/` for adaptation rules

### For Quality Control
- See `04-operations/quality_gate.md`
- Run Red Team before publishing
- Check monthly drift reports

### For Research
- See `05-signals/` for tracking templates

---

**Last Updated**: 21 January 2026  
**Version**: 1.0  
**Status**: Canonical — All other docs derive from this

---

*This document is the institutional operating system. All engines must reference it. All processes must align with it.*
