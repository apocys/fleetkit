# Decision Escalation Protocol

When agents disagree and can't resolve it themselves, decisions escalate to the human CEO. This protocol ensures escalations are clear, well-framed, and actionable.

---

## When to Escalate

Escalate to the CEO when:

1. **Fundamental disagreement**: Two or more agents hold opposing positions after debate
2. **Resource allocation**: Competing priorities that require trade-offs
3. **Strategic direction**: Decisions that change the company's course
4. **Risk tolerance**: The fleet can't agree on acceptable risk levels
5. **Brand/values**: Anything that touches company identity or ethics

**Don't escalate** when:
- It's a tactical decision within one agent's domain
- The disagreement is about execution details, not direction
- A brainstorm synthesis already includes a clear COO recommendation

---

## Decision Brief Template

The COO prepares the brief. It should be readable in under 2 minutes.

```markdown
# Decision Needed: {TITLE}

**Date:** {DATE}
**Urgency:** 🔴 Urgent (decide today) | 🟡 Important (decide this week) | 🟢 Strategic (decide this month)
**Raised by:** {AGENT}
**Prepared by:** COO

## Context
{2-3 sentences on what happened and why this needs a decision}

## The Question
{One clear sentence. Frame as a choice, not an open question.}

## Options

### Option A: {Name}
- **Championed by:** {AGENT}
- **What:** {What we'd do}
- **Upside:** {Best case}
- **Downside:** {Worst case}
- **Cost:** {Time, money, opportunity cost}

### Option B: {Name}
- **Championed by:** {AGENT}
- **What:** {What we'd do}
- **Upside:** {Best case}
- **Downside:** {Worst case}
- **Cost:** {Time, money, opportunity cost}

### Option C: {Name} (if applicable)
...

## Agent Positions

| Agent | Position | Confidence | Key Argument |
|-------|----------|------------|-------------|
| CRO   | Option A | High       | {one line}  |
| CTO   | Option B | Medium     | {one line}  |
| CMO   | Option A | High       | {one line}  |
| COO   | Option A | Medium     | {one line}  |

## COO Recommendation
{Your recommendation with rationale. Be direct. "I recommend Option A because..."}

## What We Need
{Exact decision needed: "Choose A or B" or "Approve/reject this proposal"}

## Deadline
{When does this need to be decided? What happens if we wait?}
```

---

## Delivery

### Via Telegram/Discord
```
📋 Decision Needed: {TITLE}
Urgency: {🔴/🟡/🟢}

Quick version: {one sentence}

Options:
A) {option} — backed by CRO, CMO
B) {option} — backed by CTO

Atlas recommends: A

Full brief: {link}

Reply A, B, or "need more info"
```

### Via Chat
If the CEO is in an active session, present the brief inline and ask for their decision.

---

## After the Decision

Once the CEO decides:

1. **COO records it** in the decision log with:
   - Date
   - Decision made
   - Rationale (from CEO)
   - Dissenting opinions noted
   - Owner assigned
   - Review date set

2. **Notify all agents** of the decision and their action items

3. **Save the record**:
   ```
   docs/decisions/YYYY-MM-DD-{topic-slug}.md
   ```

---

## Decision Log Format

```markdown
# Decision: {TITLE}

**Date:** {DATE}
**Decided by:** CEO
**Recommendation was:** Option {X} by COO

## Decision
{What was decided, in one paragraph}

## Rationale
{Why, per the CEO}

## Dissenting Views
{Who disagreed and their argument — important for future reference}

## Action Items
- [ ] {Agent}: {Task} — Due: {Date}
- [ ] {Agent}: {Task} — Due: {Date}

## Review Date
{When to revisit this decision to see if it was right}
```

---

## Principles

1. **Never escalate without a recommendation.** The CEO shouldn't have to figure out the answer from scratch.
2. **Frame as choices, not open questions.** "Should we do A or B?" not "What should we do?"
3. **Include dissent.** The CEO needs to know who disagreed and why.
4. **Set a deadline.** Decisions without deadlines don't get made.
5. **Record everything.** Future-you will thank present-you for the decision log.
