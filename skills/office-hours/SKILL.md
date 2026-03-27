---
name: office-hours
description: "YC-style product stress test. Separates real demand from wishful thinking with 6 forcing questions. Use before building anything new — features, products, or pivots."
version: 1.0.0
date: 2026-03-19
inspired_by: "gstack/office-hours by Garry Tan (YC)"
---

# Office Hours

## The Rule

Before building anything, prove that real people want it — not just that the idea sounds good.

## When to Use

- Before starting a new product or feature
- When deciding between multiple directions
- When someone says "we should build X" and you want to pressure-test it
- When evaluating a pivot or major scope change

## Two Modes

### Startup Mode (default)

For real products that need to find users and make money. Applies rigorous demand validation.

### Builder Mode

For hackathons, side projects, learning exercises, and creative experiments. Skips demand validation, focuses on design clarity and feasibility.

Ask which mode to use. Default to Startup Mode unless told otherwise.

## The 6 Forcing Questions (Startup Mode)

Ask these one at a time. Wait for each answer before proceeding.

### 1. Who is the specific person with this problem?

Not a demographic. A real person. "Freelance designers at agencies with 10-50 employees" is better than "creative professionals." "Solo founders who failed their first launch" is even better.

**Red flag:** If the answer is "everyone" or very broad, the problem isn't well-defined yet.

### 2. What are they doing today without your product?

Every problem has an existing solution — even if it's manual, painful, or duct-taped together. If nobody is doing anything about this problem today, the problem may not be real.

**Red flag:** "Nothing — nobody has solved this yet." (Almost always wrong.)

### 3. What evidence do you have that people want this?

Ranked from strongest to weakest:

| Evidence tier | Example |
|--------------|---------|
| Revenue | People are paying for a prototype or waitlist |
| Letters of intent | Signed commitments to buy when ready |
| Active workarounds | People hacking together solutions themselves |
| Interviews | Conversations where they described the pain unprompted |
| Survey responses | People said they'd use it (weakest — talk is cheap) |

**Red flag:** Only survey data or "people say they want it." Interest is not demand.

### 4. Why will they switch from their current solution to yours?

Switching has a cost. Your product has to be dramatically better — not slightly better. The bar is usually 10x improvement on the dimension that matters most.

**Red flag:** "It's a better UX" without a specific, measurable improvement.

### 5. What's the simplest version you could ship in 2 weeks?

If the answer requires more than 2 weeks of building, the scope is too big. Find the one feature that proves the core value.

**Red flag:** "We need to build the full platform first."

### 6. How will you know it's working?

Define one metric that proves the product is delivering value. Not vanity metrics (page views, signups). Usage metrics (tasks completed, time saved, retention at day 7).

**Red flag:** "We'll look at signups." (Signups measure curiosity, not value.)

## After the 6 Questions

Produce a written summary:

```
## Office Hours Summary

**Product idea:** [one sentence]
**Target user:** [specific person]
**Current solution:** [what they do today]
**Evidence tier:** [revenue/LOI/workarounds/interviews/surveys]
**Switching motivation:** [why they'd change]
**2-week MVP:** [the simplest version]
**Success metric:** [one measurable outcome]

**Verdict:** [STRONG SIGNAL / NEEDS MORE EVIDENCE / RETHINK]
```

## Builder Mode

Skip questions 2-4. Focus on:
1. What are you building and for whom?
2. What's the simplest version?
3. How will you know it works?

Then help design and build. No demand gatekeeping.

## Key Principle

The job is to find the truth, not to be encouraging. A "rethink" verdict early saves months of building the wrong thing.
