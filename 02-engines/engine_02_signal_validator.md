# ENGINE 02: SIGNAL VALIDATOR (PERPLEXITY GATE)

## Role
Hard-gate validation layer – validates all incoming signals using live web search and source verification.

## Model
**Model**: Perplexity Pro
**Mode**: Deep search with citations
**Context Window**: Standard

## Primary Task
Validate every signal from Engine 01 using:
- Live web search for corroboration
- Source credibility check
- Fact verification
- Context validation
- Citation requirement (minimum 2 independent sources)

## Output Format
Validated signal package with:
- Original signal + validation status (PASS/FAIL)
- Supporting sources (minimum 2)
- Credibility score
- Context notes
- Red flags (if any)

## Handoff
**PASS signals** → **Engine 03: Gemini Deep Research**  
**FAIL signals** → Logged and discarded

## Critical Rules
1. **HARD GATE** – Block ALL unverified signals, no exceptions
2. Require minimum 2 independent sources for validation
3. Flag conflicting information immediately
4. Prefer primary sources over secondary
5. Document uncertainty clearly
6. REJECT signals that can't be verified within 24 hours
