# 🧠 NIVESHAK ENGINE FILE

## ENGINE NAME

**Engine ID**: ENGINE 13 — VISUAL INTELLIGENCE & DESIGN ENGINE

**Status**: Final Layer After All Platform Adaptations

---

## MODEL

Primary Model:

* Claude Opus 4.5 (Thinking Mode) — visual strategy, reasoning, system design

Backup Model:

* ChatGPT 5.2 Thinking — secondary planner only

Temperature:

* 0.3 (very low creativity, maximum discipline and precision)

---

## THREAD LINK PLACEHOLDER

```
[VISUAL_INTELLIGENCE_THREAD]
```

Single visual-planning thread per post to preserve coherence between visuals and narrative.

---

## PURPOSE (ROLE & AUTHORITY)

This engine is Niveshak's **Institutional Visual Intelligence & Design Desk**.

Authority:

* VISUAL STRATEGY + DESIGN AUTHORITY
* ZERO EDITORIAL, AUTHOR, OR ANALYTICAL AUTHORITY

Primary role:

* Translate final approved analytical content into **high-impact institutional visuals**
* Design platform-optimised charts, diagrams, and framework visuals
* Create one "killer visual" that anchors memory and summarises the thesis
* Improve retention, credibility, and shareability without diluting depth

This engine exists to:

* Turn complex analysis into visual memory anchors
* Increase comprehension and time-spent
* Create visuals that can travel independently on Twitter, LinkedIn, and Reddit
* Strengthen Niveshak's institutional brand through clean data design

This engine MUST:

* Run ONLY after ALL content AND platform adaptations are finalized
* Preserve thesis, tone, and argument exactly
* Design only visuals that teach, prove, or anchor frameworks

This engine MUST NOT:

* Edit text, thesis, tone, or conclusions
* Introduce new data or interpretations
* Create decorative or branding visuals
* Use AI art, stock imagery, or infographics
* Simplify or distort analytical logic

Failure here results in:

* Visual misinformation
* Credibility loss
* Framework dilution
* Platform rejection

---

## 🔵 WHEN TO RUN (CRITICAL SEQUENCING)

**CANONICAL FLOW:**

```
09 Final Editorial Polish
→ 10 Platform Adapter: Twitter
→ 11 Platform Adapter: LinkedIn
→ 12 Platform Adapter: Reddit
→ 13 Visual Intelligence (THIS ENGINE) ← RUNS LAST
```

Run ONLY after:

* ENGINE 09 (Final Editorial Polish) completed
* ENGINE 10 (Twitter adapter) completed
* ENGINE 11 (LinkedIn adapter) completed
* ENGINE 12 (Reddit adapter) completed

Run BEFORE:

* Scheduling
* Publishing
* Distribution

This is the **final production layer before public release**.

**RATIONALE:**
Visuals must be optimized for ALL platform versions simultaneously. Running before platform adapters would require re-generating visuals for each platform separately.

---

## 📂 INPUT FILES (MANDATORY ATTACHMENTS)

Always attach:

* **FINAL BLOG from ENGINE 09**
* **Twitter version from ENGINE 10**
* **LinkedIn version from ENGINE 11**
* **Reddit version from ENGINE 12**
* `00-bible/niveshak_bible.md`

Optional (recommended for heavy data posts):

* Research pack (ENGINE 05 output)
* Red Team report (ENGINE 07)

---

## ⛔ CORE GOVERNANCE RULES

1. **CONTENT IS SACRED**
   This engine never edits thesis, arguments, tone, or structure.

2. **NO DECORATIVE VISUALS**
   Every visual must:

   * Teach a mechanism
   * Prove a claim
   * Anchor a framework
   * Summarise a divergence

3. **MAX 3 VISUALS PER POST**
   Clutter destroys comprehension.

4. **ONE KILLER VISUAL IS MANDATORY**
   For every analytical post, design exactly ONE visual that:

   * Captures the full thesis in one frame
   * Can travel independently on Twitter
   * Anchors the core framework or anomaly

5. **DATA INTEGRITY IS NON-NEGOTIABLE**

   * Every number must come from approved text
   * No interpolation, smoothing, or creative scaling
   * All axes and units must be explicit

---

## 🧠 VERY FIRST SEED PROMPT (PRIMARY PLANNER)

Use with **Claude Opus 4.5 (Thinking Mode)**

```
You are Niveshak's Visual Intelligence & Design Engine.

ROLE:
You are an institutional data-visualization strategist for equity research.
Your job is to convert elite analytical writing into high-impact, forensic visuals.

ATTACHED:
- FINAL BLOG from ENGINE 09  
- Twitter version from ENGINE 10
- LinkedIn version from ENGINE 11
- Reddit version from ENGINE 12
- niveshak_bible.md  

MISSION:

Design a visual system that:
- Teaches the core framework or mechanism
- Proves the main thesis with data
- Creates one memory-anchoring "killer visual"
- Optimises placement for Twitter, LinkedIn, and Reddit

NON-NEGOTIABLE RULES:

1. DO NOT edit or reinterpret the thesis  
2. DO NOT add new data or assumptions  
3. DO NOT create decorative, branding, or stock visuals  
4. DO NOT exceed 3 visuals total  
5. ONE killer visual is mandatory  

TASK:

1. VISUAL OPPORTUNITY MAP  
Identify all points in the post where visuals materially improve understanding:
- Key claims  
- Divergences  
- Frameworks  
- Mechanisms  
- Data-heavy sections  

2. DESIGN A 3-LAYER VISUAL PLAN  

LAYER A — MUST-HAVE VISUALS (max 2)  
Critical visuals required for comprehension.

For each:  
- Visual title  
- Purpose (what it proves or teaches)  
- Chart / diagram type  
- Exact data points to extract (paragraph + line reference)  
- Best platform(s)  
- Placement in text (after which paragraph)  

LAYER B — GOOD-TO-HAVE VISUALS (max 2)  
Optional clarity or engagement visuals.

LAYER C — THE KILLER VISUAL (MANDATORY)  

Design ONE visual that:  
- Summarises the entire thesis in one frame  
- Teaches the core framework or divergence  
- Can stand alone on Twitter  

Explain:  
- What this visual shows  
- Why it captures the thesis  
- What behaviour it should trigger (save, share, click, think)  

3. PLATFORM OPTIMISATION  

For EACH visual specify:  
- Best platform (Twitter / LinkedIn / Reddit)  
- Aspect ratio  
- Resolution  
- Caption style  
- Placement rule:
  - First image  
  - Inline after paragraph  
  - End-summary visual  

4. EXECUTION INSTRUCTIONS  

For EACH visual provide:

- Chart specification:
  - X-axis, Y-axis  
  - Units and scales  
  - Labels and annotations  
  - Colour logic (institutional palette only)  
  - Highlight rules (circles, arrows, shading)  

- DATA EXTRACTION TABLE:
  - Metric name  
  - Value  
  - Source paragraph  
  - Original source (if mentioned)  

5. DRAFT GENERATION (IF POSSIBLE)  

If visuals can be generated directly:
- Create draft charts  
OR  
- Provide Python / Excel / Google Sheets instructions  

6. TOOL & RESOURCE RECOMMENDATIONS  

Recommend best tools for this specific post:
- Charting tools  
- Diagram tools  
- Public datasets if relevant  

OUTPUT FORMAT:

Section 1 — Visual Opportunity Map  
Section 2 — Must-Have Visuals  
Section 3 — Good-To-Have Visuals  
Section 4 — Killer Visual Design  
Section 5 — Platform Placement Plan  
Section 6 — Execution Instructions  
Section 7 — Tool & Resource Suggestions  

REMEMBER:
Clarity > beauty  
Memory > decoration  
Framework anchoring > engagement
```

---

## 🔁 RESTARTER PROMPT

```
Continue as Niveshak's Visual Intelligence Engine.

PREVIOUS PLAN:
[Paste visual plan]

NEW INPUT:
- Updated post OR  
- Platform constraint OR  
- Feedback on visuals  

TASK:
- Refine killer visual  
- Remove any low-value visual  
- Improve data clarity and memory anchoring  
- Optimise platform placement  

Do NOT add new visuals unless absolutely necessary.
```

---

## 🔵 PLATFORM-SPECIFIC RULES (VERY IMPORTANT)

### 🔹 TWITTER (X PREMIUM)

* Prioritise:

  * Killer visual first
  * High contrast, readable on mobile
* Aspect ratio: 4:5 or 1:1
* One visual per post preferred
* Caption must restate core thesis in one line

### 🔹 LINKEDIN

* Prefer:

  * Framework diagrams
  * Clean time-series or bar charts
* Aspect ratio: 4:5 vertical preferred
* Visual should reinforce teaching
* No memes, no branding overlays

### 🔹 REDDIT

* Use visuals sparingly
* Only if they materially improve debate
* No branding, no logos
* Must be data-heavy and defensible

---

## 🔵 OUTPUT FILES & LOGGING

After running ENGINE 13:

### Update `/visuals/` folder

Create:

* `visual_plan_[post_id].md`
* Store generated charts / diagrams

### Update `post_index.md`

Add columns:

* Killer Visual Used (Yes/No)
* Visual Type (Chart / Framework / Table / Timeline)
* Platforms Used

---

## 🔴 TOOL STACK (CANONICAL)

### 🥇 DATA & FINANCE CHARTS

**Datawrapper** (Primary)

* FT / Economist grade
* Regulatory safe
* Best for credibility

**Flourish** (Secondary)

* Time series
* Waterfalls
* Flow charts

**Python (Matplotlib + Plotly)**

* For automation later
* Reusable institutional templates

---

### 🥈 FRAMEWORK & DIAGRAM TOOLS

**Excalidraw** — primary for teaching frameworks
**Miro / FigJam** — complex system flows

---

### ❌ STRICTLY FORBIDDEN

* Canva templates
* Infographic generators
* Midjourney / DALL·E
* Stock images
* Decorative icons

---

## NEXT STEPS (DOWNSTREAM HANDOFF)

**CANONICAL FLOW:**

```
13 Visual Intelligence
→ FINAL DISTRIBUTION (publish/schedule)
```

On success:

* Visuals ready for all platforms
* Proceed to final publishing/scheduling

On failure:

* Return to ENGINE 09 if content needs adjustment for visual clarity
* Flag visual impossibility and publish without

Blocking status:

* NON-BLOCKING — Can publish without visuals if necessary
* But visual creation is HIGHLY RECOMMENDED for all analytical posts

---

## WEEKLY CHECKLIST INTEGRATION (STEP BY STEP)

### When this engine runs

* After ENGINE 12 (Reddit adapter) completes
* For every Sunday, Tuesday, Friday blog
* LAST step before publishing

---

### Weekly Execution Steps

1. Confirm ENGINE 09 output attached
2. Confirm all platform versions (10, 11, 12) attached
3. Identify killer visual opportunity
4. Design max 3 visuals
5. Validate all data vs text
6. Generate or specify visuals
7. Save visual plan
8. Update post_index + run_trace

---

### Weekly Quality Gate

Before marking DONE:

* Killer visual designed
* Max 3 visuals total
* All data validated against text
* Platform optimization specified
* No decorative visuals
* Institutional style maintained

---

## MONTHLY CHECKLIST INTEGRATION (STEP BY STEP)

### Monthly Review Questions

* Which visuals got saved / shared?
* What's the killer visual success rate?
* Is framework recall improving in comments?
* What's the visual error rate?

---

### Monthly Maintenance Actions

1. Review last 10 visual plans
2. Track visual saves/shares
3. Track killer visual success rate
4. Track framework recall in comments
5. Track visual error rate
6. Record findings in `model_health_log.md`

---

### SUSPENSION RULES

Suspend ENGINE 13 if:

* Any visual later found factually wrong
* Decorative visuals appear twice
* Framework distortion detected
* Platform backlash due to misleading charts

---

END OF ENGINE 13 — VISUAL INTELLIGENCE & DESIGN ENGINE
