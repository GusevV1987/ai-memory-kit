---
name: plan-ceo-review
description: "Founder-mode strategic plan review. Stress-tests plans across 11 dimensions from a CEO perspective — business risk, scope creep, failure modes, and go/no-go readiness."
version: 1.0.0
date: 2026-03-19
inspired_by: "gstack/plan-ceo-review by Garry Tan (YC)"
---

# Plan — CEO Review

## The Rule

Before executing any significant plan, review it through the lens of a founder who owns the outcome.

## When to Use

- Before executing a multi-step implementation plan
- Before any major architecture decision
- When a plan touches production systems, user data, or costs money
- When you want a "would I bet the company on this?" gut check

## The 11 Review Dimensions

Score each 1-10. Flag anything below 7.

### 1. Problem Clarity
Is the problem statement specific and falsifiable? Can you explain what success looks like in one sentence?

### 2. Scope Discipline
Does the plan do exactly what's needed — no more, no less? Is every item justified? Would you cut anything if you had half the time?

### 3. Architecture Fit
Does this fit into the existing system, or does it introduce a new pattern? New patterns need 3x the justification.

### 4. Failure Modes
What happens when this breaks? What's the blast radius? Is there a rollback path? How long until someone notices?

### 5. Security Surface
Does this expand the attack surface? Does it handle credentials, user data, or external inputs? What's the worst case if an attacker targets this specifically?

### 6. Dependency Risk
What external systems does this rely on? What happens if they're down, slow, or change their API? Are there fallbacks?

### 7. Operational Burden
Who maintains this after it ships? Does it add monitoring, alerts, or manual intervention? Does it make the on-call rotation harder?

### 8. Cost Impact
What does this cost to run? Does it scale linearly or exponentially? Are there usage-based charges that could surprise you?

### 9. Reversibility
If this turns out to be wrong, how hard is it to undo? Prefer reversible decisions. Irreversible ones need more scrutiny.

### 10. Timeline Realism
Is the time estimate honest? Does it account for testing, deployment, documentation, and the inevitable surprises? Double your gut estimate.

### 11. Strategic Alignment
Does this move the company closer to its core goal, or is it a detour? Would you still do this if you only had 3 months of runway?

## Output Format

```
## CEO Review: [Plan Name]

| Dimension | Score | Notes |
|-----------|-------|-------|
| Problem Clarity | X/10 | |
| Scope Discipline | X/10 | |
| Architecture Fit | X/10 | |
| Failure Modes | X/10 | |
| Security Surface | X/10 | |
| Dependency Risk | X/10 | |
| Operational Burden | X/10 | |
| Cost Impact | X/10 | |
| Reversibility | X/10 | |
| Timeline Realism | X/10 | |
| Strategic Alignment | X/10 | |

**Average:** X/10

### Failure Modes Registry
1. [Specific failure mode] → [Mitigation or acceptance]
2. [Specific failure mode] → [Mitigation or acceptance]

### Scope Recommendations
- **Keep:** [Items that are essential]
- **Cut:** [Items that can wait]
- **Add:** [Missing items that should be there]

### Verdict
[GO / GO WITH CHANGES / NO-GO]

[One paragraph explaining the verdict]
```

## Scope Postures

When recommending scope changes, choose one:

| Posture | When to use |
|---------|------------|
| **Expand** | Critical gaps found — plan is incomplete without these additions |
| **Hold** | Plan is solid as-is |
| **Trim** | Plan has nice-to-haves that increase risk without proportional value |
| **Reduce** | Plan is too ambitious — cut to the essential core |

## Key Principle

This review represents the founder's perspective: what matters is whether this plan moves the business forward with acceptable risk. Technical elegance doesn't matter if the business case is weak. Speed matters, but not at the cost of reliability.
