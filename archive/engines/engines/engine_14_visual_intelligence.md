# 🧠 ENGINE 14 — VISUAL INTELLIGENCE & DESIGN ENGINE

**Status: Mandatory Final Layer Before Publishing**
**Primary Model: Claude Opus 4.5 (Thinking Mode)**
**Backup Model: ChatGPT 5.2 Thinking**

---

## 🎯 PURPOSE

This engine converts elite analytical content into:
- High-impact institutional visuals
- Platform-optimized charts & diagrams
- Shareable “killer visuals”
- Memory anchors for frameworks

Goals:
- Increase retention and share rate
- Make frameworks visually memorable
- Improve credibility through clean data design
- Never dilute Niveshak voice

This engine runs **ONLY AFTER content is approved**.

---

## ⛔ CORE RULES

1. **Content is sacred**
   This engine never edits thesis, tone, or argument.

2. **No decorative visuals**
   Every visual must:
   - Teach something
   - Prove something
   - Anchor memory

3. **Max 3 visuals per post**
   Quality > clutter.

4. **One “Killer Visual” mandatory per analytical post**
   One chart that:
   - Summarizes the entire thesis
   - Can travel independently on Twitter
   - Teaches the core framework or divergence

---

## 🔵 WHEN TO RUN

Run after:
- Red Team verdict = PUBLISH
- Platform versions ready

Before:
- Final scheduling
- Posting

---

## 📂 FILES TO ATTACH

Always attach:
- **Polished Draft (Engine 04.1 Output)** — NOT raw Apex draft
- `00-bible/niveshak_bible.md` (voice & bans)
- Platform files:
  - `03-platforms/twitter_thread.md`
  - `03-platforms/linkedin_post.md`

Optional:
- Research brief (if heavy data post)

---

## 🧠 STARTER PROMPT (PRIMARY)

Use with **Claude Opus 4.5 Thinking**.

```
You are Niveshak’s Visual Intelligence & Design Engine.

ROLE:
You are an institutional data-visualization strategist for equity research.
Your job is to translate elite analytical content into high-impact visuals.

ATTACHED:
- Final approved post
- niveshak_bible.md (voice & bans)
- Platform rules (Twitter, LinkedIn)

TASK:

1. Identify ALL visual opportunities in this post:
   - Key arguments that deserve visuals
   - Data points that can be visualized
   - Frameworks that benefit from diagrams

2. Propose a VISUAL PLAN with 3 layers:

LAYER A — MUST-HAVE VISUALS (max 2)
These are critical for understanding the thesis.

For each:
- Visual title
- What it shows
- Chart type (line, bar, scatter, waterfall, flow, table, timeline, framework diagram)
- Exact data points to extract from the post
- Where to place in the post (after which paragraph)
- Which platform(s) it is best for

LAYER B — GOOD-TO-HAVE VISUALS (max 2)
Optional visuals that improve clarity or engagement.

LAYER C — THE KILLER VISUAL (MANDATORY)
Design ONE visual that:
- Captures the full thesis in one frame
- Can stand alone on Twitter
- Teaches the core framework or divergence

Explain:
- Why this is the killer visual
- What behaviour it should trigger in readers

3. PLATFORM OPTIMIZATION

For each proposed visual specify:
- Best platform (Twitter / LinkedIn / Reddit)
- Ideal aspect ratio
- Caption / annotation style
- Whether it should appear:
  - Inline in thread
  - As first image
  - As summary image at end

4. VISUAL EXECUTION INSTRUCTIONS

For EACH visual provide:

- Chart specification:
  - Axes
  - Units
  - Labels
  - Color logic (institutional, no flashy colors)
  - Highlight rules (what to circle, annotate, shade)

- Data extraction table:
  - List all numbers required
  - From which paragraph or section to extract

5. GENERATE DRAFT VISUALS (IF POSSIBLE)

If any visual can be directly created from the text:
- Generate a draft chart or table
- Or generate Python / Excel / Google Sheets instructions

6. RESOURCE SUGGESTIONS

Recommend best tools for this post:
- Finance-grade charting tools
- Templates
- Public datasets if relevant

RULES:
- No decorative images
- No stock photos
- No AI art
- Only data, frameworks, and diagrams
- Respect Niveshak voice: institutional, calm, precise

OUTPUT FORMAT:
Section 1 — Visual Opportunity Map  
Section 2 — Must-Have Visuals  
Section 3 — Good-To-Have Visuals  
Section 4 — Killer Visual Design  
Section 5 — Platform Placement Plan  
Section 6 — Execution Instructions  
Section 7 — Tool & Resource Suggestions
```

---

## 🔁 RE-STARTER PROMPT (WHEN REVISING VISUALS)

```
You are continuing as Niveshak’s Visual Intelligence Engine.

PREVIOUS OUTPUT:
[Paste previous visual plan]

NEW INPUT:
- Updated post OR
- Feedback on visuals OR
- Platform-specific constraints

TASK:
- Refine visual plan
- Improve killer visual
- Optimize for shareability and clarity
- Remove any visual that does not materially improve understanding

Focus on:
- Clarity over beauty
- Memory over decoration
- Framework anchoring
```

---

## 🔵 OUTPUT FILES & LOGGING

After running Engine 14:

Update:

### 1. Add to post folder (if you create one):
- `/visuals/post_[date]_visual_plan.md`

### 2. Update in `post_index.md`:
Add columns:
- Killer Visual Used (Yes/No)
- Visual Type (Chart / Framework / Table / Timeline)

---

## 🔴 TOOL STACK (VERY IMPORTANT)

Here are the best tools for your use case. This matters a lot.

### 🥇 RAW DATA & FINANCE CHARTS

**Best Overall: Flourish (by Canva)**
- Excellent for:
  - Time series
  - Waterfall
  - Scatter
  - Institutional look

**Best for serious work: Datawrapper**
- Used by FT, Economist, Bloomberg
- Perfect for:
  - Clean charts
  - Regulatory-safe visuals
  - Exportable PNG/SVG

**Best for internal power users: Python (Matplotlib + Plotly)**
When you want:
- Full control
- Reusable templates
- Later automation

---

### 🥈 FRAMEWORK & DIAGRAM TOOLS

**Excalidraw** — best for:
- Framework diagrams
- Flow charts
- Teaching visuals

**Miro / FigJam** — for:
- Multi-step system diagrams

---

### 🥉 QUICK TABLE / SUMMARY VISUALS

- Google Sheets
- Excel
- Notion tables

---

### ❌ TO AVOID

- Midjourney / DALL·E (art, not data)
- Canva templates (too influencer)
- Infographic generators (destroy credibility)
