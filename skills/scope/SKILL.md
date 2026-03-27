---
name: scope
description: |
  Framework-driven feature scoping decisions for product development. Applies 7 product
  frameworks (Lean Startup, JTBD, RICE, etc.) to decide whether a feature belongs in MVP
  or later iterations. Use when: (1) /scope command, (2) "should we include X in MVP?",
  "scope this feature", "MVP or later?", (3) any product feature prioritization decision.
author: Claude Code
version: 1.0.0
date: 2026-03-07
allowed-tools:
  - Read
  - Write
  - Edit
  - Glob
  - Grep
  - WebSearch
  - AskUserQuestion
  - TodoWrite
---

# Feature Scoping Skill

Make disciplined product decisions about whether a feature belongs in MVP or later iterations, using 7 proven frameworks.

## When to Use

- User says `/scope`, "should we include X in MVP?", "scope this feature", "MVP or later?"
- Any feature prioritization decision for a new or existing product
- Choosing between "build it now" vs "build it later" for a specific capability

## Step 1: Gather Context

Use AskUserQuestion to collect:

1. **Feature description** — What's the feature? What would it do?
2. **Product context** — What product is this for? What's the core product hypothesis? (If a PRD exists, read it)
3. **Current user flow** — How long is the current user journey? (minutes, steps, etc.)
4. **Why it's being considered** — What triggered this question? (user request, competitor has it, founder wants it)

If a PRD or product doc exists, read it first to understand the product context.

## Step 2: Apply 7 Frameworks

Analyze the feature through each framework. Present results as a clear table.

### Framework 1: Lean Startup — Hypothesis Test

**Question:** Does this feature help test the core product hypothesis?

| Evaluation | Meaning |
|-----------|---------|
| **Direct** | The feature IS the hypothesis test |
| **Supporting** | Helps test it but isn't the main thing |
| **Irrelevant** | Doesn't help test the core hypothesis |
| **Distracting** | Actively distracts from testing the hypothesis |

### Framework 2: Jobs-to-be-Done

**Question:** Is this the job the user hired the product for?

- What's the primary job-to-be-done?
- Does this feature serve the primary job, a secondary job, or a different job entirely?
- Would users feel the product is incomplete without it?

### Framework 3: RICE Scoring

**Score the feature:**

| Factor | Score (1-10) | Reasoning |
|--------|-------------|-----------|
| **Reach** | ? | How many users will this affect in the first 3 months? |
| **Impact** | ? | How much will it improve the experience? (3=massive, 2=high, 1=medium, 0.5=low, 0.25=minimal) |
| **Confidence** | ? | How sure are we this will work? (100%=high, 80%=medium, 50%=low) |
| **Effort** | ? | Person-weeks to build (higher = more effort) |

**RICE Score = (Reach x Impact x Confidence) / Effort**

### Framework 4: Flow Length Analysis

**Question:** How much time does this add to the user journey?

| Current flow | + This feature | Total | Drop-off risk |
|-------------|----------------|-------|---------------|
| X min | +Y min | Z min | Low/Medium/High/Fatal |

Rules of thumb:
- Every additional minute in a flow loses ~3-5% of users
- Flows over 15 minutes need save/resume
- Flows over 30 minutes need very strong motivation

### Framework 5: Core Hypothesis Test

**Question:** What's the #1 assumption this product needs to validate?

- State the core hypothesis explicitly
- Does this feature help prove or disprove it?
- If the hypothesis fails, does this feature still have value?
- Could we validate the hypothesis WITHOUT this feature?

### Framework 6: Natural Emergence

**Question:** Does this feature emerge organically from existing features?

| Pattern | Signal |
|---------|--------|
| **Natural** | The feature is a byproduct of existing functionality (e.g., analytics from usage data) |
| **Passive** | Can be captured with minimal extra effort during existing flows |
| **Requires dedicated flow** | Needs its own UI, conversation, or data collection step |
| **Parallel product** | Is essentially a separate product |

If a feature can be captured passively or naturally, it costs almost nothing to include. If it requires a dedicated flow, the cost is real.

### Framework 7: Differentiation Value

**Question:** Does this strengthen or dilute our competitive edge?

- What's our #1 differentiator? (from competitive analysis if available)
- Does this feature reinforce that differentiator or spread focus?
- Do competitors already do this well? (if so, it's table stakes, not differentiation)
- Would removing this feature make our positioning weaker?

## Step 3: Synthesize Decision

Combine all 7 frameworks into a decision:

| Verdict | When to use it |
|---------|---------------|
| **MVP** | Feature directly tests core hypothesis, serves primary JTBD, high RICE, manageable flow impact, reinforces differentiation |
| **V1.5 (Light version)** | Feature has value but can be included passively or in lightweight form without adding user flow time |
| **V2 (Full version)** | Feature is valuable but requires dedicated flow, doesn't test core hypothesis, or competitors don't have it yet |
| **Never** | Feature is a distraction, dilutes positioning, or serves a different JTBD |

## Step 4: Present Decision

Format the output as:

### Decision: [Feature Name]

**Verdict: [MVP / V1.5 / V2 / Never]**

| Framework | Finding | Supports MVP? |
|-----------|---------|--------------|
| Lean Startup | [finding] | Yes/No |
| JTBD | [finding] | Yes/No |
| RICE | Score: [X] | Yes/No |
| Flow Length | +[Y] min ([risk] drop-off) | Yes/No |
| Core Hypothesis | [finding] | Yes/No |
| Natural Emergence | [pattern] | Yes/No |
| Differentiation | [finding] | Yes/No |

**Score: [X]/7 frameworks support MVP**

### Phased Approach

| Phase | What to do | Why |
|-------|-----------|-----|
| **MVP** | [specific approach] | [reasoning] |
| **V1.5** | [if applicable] | [reasoning] |
| **V2** | [if applicable] | [reasoning] |

### If Not MVP — Passive Alternative

If the verdict is V1.5 or later, always suggest a passive/lightweight alternative that captures some value with zero extra user flow time. Examples:
- AI detects patterns during existing conversation instead of asking directly
- Collect metadata passively from user behavior
- Offer as optional post-completion add-on
- Surface through existing UI without dedicated section

## Step 5: Save Output

Save to the project folder if one exists, or present inline.

## Tips from Experience

- **The biggest risk is usually flow length** — adding 10 min to a 20 min flow is fatal
- **"Passive capture" is the secret weapon** — many features can be included at near-zero cost if you don't try to do them perfectly
- **Core hypothesis is the tiebreaker** — when frameworks disagree, always defer to "does this help test the core hypothesis?"
- **Competitors having a feature doesn't mean you need it** — it might be table stakes, or it might be their differentiator (not yours)
- **V1.5 is often the right answer** — not MVP, not V2, but a lightweight version that captures 60% of the value at 10% of the cost
