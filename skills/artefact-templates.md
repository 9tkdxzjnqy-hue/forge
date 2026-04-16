# Skills · Artefact Templates

Standardised formats for every output this framework produces.
Agents should use these templates as the basis for their outputs —
not verbatim, but structurally consistent.

Consistency matters because: the Synthesis agent reads prior
agent outputs programmatically, the build team reads the brief
at the start of every session, and Linear issues follow a
predictable structure that the Delivery Manager depends on.

---

## brief.md

```markdown
# [Product name or working title]

**Idea slug:** [idea-name]
**Date:** [date]
**Status:** Draft / Refined / Build-ready

---

## The problem
[2–3 sentences: who has it, what it is, why it matters now]

## The user
[Specific human description — not a demographic. Who they are,
what their situation is, and what this problem costs them.]

## Job-to-be-done

**Primary:**
When [situation], I want to [motivation], so I can [outcome].

**Sub-jobs:**
- When [situation], I want to [motivation], so I can [outcome].
- When [situation], I want to [motivation], so I can [outcome].

## The opportunity
[What changes for the user if this works — functionally,
emotionally, and in terms of what they can now do or stop doing]

## Solution direction
[What the product does — intent, not implementation.
2–4 sentences.]

## Success metrics

**North star:** [The one metric that indicates real value is being delivered]
**Definition:** [What this metric measures and how]

**Supporting metrics:**
- [Metric] — [what it measures]
- [Metric] — [what it measures]

## MVP scope

**In v1:**
- As a [user], I can [action], so that [outcome]
- As a [user], I can [action], so that [outcome]

**Out of v1 (and why):**
- [Feature] — [reason for deferral]
- [Feature] — [reason for deferral]

## Key risks
[Top 3 from assumption log — with current status]

1. [Risk] — Status: Open / Defended / Accepted
2. [Risk] — Status: Open / Defended / Accepted
3. [Risk] — Status: Open / Defended / Accepted

## Research recommendation
[Validate before building / Validate in parallel / Build and learn]
[One sentence of reasoning]

## Open questions
[Anything unresolved the build team should be aware of]
```

---

## assumptions.md

```markdown
# Assumption Log: [idea name]

Last updated: [date]

---

| # | Assumption | Type | Risk | Status | Validation method |
|---|-----------|------|------|--------|------------------|
| 1 | [assumption] | Desirability/Viability/Feasibility | High/Med/Low | Open/Defended/Accepted | [how to test] |

---

## Notes on defended assumptions
[For each assumption marked Defended — the human's defence in one sentence]

## Notes on accepted risks
[For each assumption marked Accepted — acknowledgement that the risk is known and the decision to proceed is deliberate]
```

---

## research-plan.md

```markdown
# Research Plan: [idea name]

Last updated: [date]
Recommended approach: [Validate before / during / after build]

---

## Knowledge map

### Known (grounded in evidence)
- [claim] — [basis]

### Assumed (plausible, unverified)
- [claim] — [what would verify it]

### Unknown (not addressed)
- [claim] — [why it matters]

---

## Validation priorities

### Before building
**Assumption being tested:** [what you need to know]
**Method:** [interview / landing page / prototype / survey]
**Success signal:** [what good looks like]
**Suggested screener:** [2–3 questions to find right participants]

### During build
[What can be validated through early releases]

---

## Interview guide
*(if interviews are the recommended method)*

**Session length:** 30 minutes
**Goal:** [What you're trying to learn]

**Warm-up**
1. Tell me a bit about how you currently [relevant activity].

**Core questions**
2. Tell me about the last time you [situation where problem occurs].
3. What did you do when that happened?
4. What was frustrating about that? What worked?
5. How often does this come up?
6. What would have to be true for you to change how you do this?

**Close**
7. Is there anything about [problem area] I haven't asked about
   that you think would be useful to know?
```

---

## ost.md

```markdown
# Opportunity Solution Tree: [idea name]

---

## Outcome
**[North star metric]**
[Definition — what this measures and why it matters]

---

## Opportunities

### [Opportunity 1 name]
[Unmet need or underserved outcome — 1–2 sentences]

Solutions:
- **[Solution A]:** [one sentence description]
- **[Solution B]:** [one sentence description]

### [Opportunity 2 name]
[Unmet need or underserved outcome — 1–2 sentences]

Solutions:
- **[Solution A]:** [one sentence description]
- **[Solution B]:** [one sentence description]

---

## Selected opportunity for v1
**[Opportunity name]** — [one sentence rationale for why this one]

## Selected solution for v1
**[Solution name]** — [one sentence rationale]
```
