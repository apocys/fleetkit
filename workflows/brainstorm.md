# Brainstorm Protocol — 3-Round Structured Debate

A multi-agent brainstorm that produces genuine strategic insight through structured disagreement. Three rounds: positions → debate → synthesis.

---

## Overview

| | |
|---|---|
| **Participants** | CRO, CTO, CMO (+ COO as synthesizer) |
| **Rounds** | 3 |
| **Estimated tokens** | ~50-70K total |
| **Estimated cost** | ~$0.80-1.50 |
| **Output** | Synthesis doc with consensus, tensions, and recommendation |

---

## Round 1: Opening Positions

Each participant agent states their position on the topic. They should be **opinionated and specific** — this is not the round for balance.

### Spawn Prompt (per agent)

```
You are participating in a fleet brainstorm on: "{TOPIC}"

This is Round 1 — Opening Positions.

Read your SOUL.md for your role and perspective. Then state your position on this topic:

1. What's your take? Be specific and opinionated.
2. What opportunities do you see from your domain?
3. What risks or concerns does your role flag?
4. What's your recommended course of action?

Be direct. Be bold. Do NOT try to be balanced — that's what the synthesis round is for. Argue your corner.

Format: Use your title and emoji as header. Keep it to 300-500 words.
```

### What to expect

- CRO leads with revenue impact, market timing, competitive angles
- CTO leads with feasibility, technical cost, optimization opportunities
- CMO leads with positioning, story, customer empathy, viral potential

**Key**: Agents should disagree. If everyone agrees in Round 1, the topic might be too obvious — or the SOUL files need more personality.

---

## Round 2: Debate & Challenge

Each agent reads ALL Round 1 positions, then responds to points they **disagree with**. This is where the real value emerges.

### Spawn Prompt (per agent)

```
You are participating in a fleet brainstorm on: "{TOPIC}"

This is Round 2 — Debate & Challenge.

Here are the Round 1 positions from all participants:

---
{PASTE ALL ROUND 1 OUTPUTS HERE}
---

Now respond:

1. Which positions do you DISAGREE with? Cite the specific agent and their claim.
2. Which positions do you AGREE with? Build on them.
3. Where are the others missing something from YOUR domain's perspective?
4. Has anyone changed your mind on anything? If so, say what and why.

Be direct. Constructive conflict produces better outcomes than polite agreement. Challenge assumptions with evidence.

Format: Use your title and emoji as header. Keep it to 300-500 words.
```

### What to expect

- CRO challenges CTO's timelines and CMO's non-revenue priorities
- CTO challenges CRO's "ship now" urgency and CMO's vagueness
- CMO challenges CRO's revenue-only thinking and CTO's "it's hard" reflexes
- Some positions shift. Some harden. Both are valuable.

---

## Round 3: Synthesis (COO Only)

The COO reads everything and produces a structured executive brief. This is the deliverable.

### Spawn Prompt (COO only)

```
You are synthesizing a fleet brainstorm on: "{TOPIC}"

This is Round 3 — Synthesis. You are the COO. Your job: turn debate into decisions.

Here are all positions from Round 1 and Round 2:

---
{PASTE ALL ROUND 1 AND ROUND 2 OUTPUTS HERE}
---

Produce an executive brief with these sections:

## CONSENSUS
What do all agents agree on? (Bullet points)

## KEY TENSIONS
Where do agents disagree? Present as a table:
| Question | CRO | CTO | CMO |

## COO CHALLENGES
Push back on at least one claim from each agent. Don't let weak arguments pass.

## RECOMMENDATION
Your recommended course of action. Be specific:
- What to do (concrete steps)
- Timeline
- Who owns what
- Expected outcome
- Key risks

## DECISIONS NEEDED
What must the CEO decide? Frame as clear yes/no or A/B/C choices.

Be honest about where consensus exists and where it doesn't. Don't paper over disagreements — surface them clearly for the CEO.
```

---

## Output Structure

Save all outputs in a brainstorm directory:

```
brainstorms/{topic-slug}/
  round-1.md      # All Round 1 positions
  round-2.md      # All Round 2 debates
  synthesis.md     # COO's final brief
```

---

## Running a Brainstorm (Step by Step)

1. **Create the directory**: `brainstorms/{topic-slug}/`
2. **Round 1**: Spawn CRO, CTO, CMO with the Round 1 prompt. Collect outputs into `round-1.md`
3. **Round 2**: Spawn CRO, CTO, CMO with Round 2 prompt (include Round 1 outputs). Collect into `round-2.md`
4. **Round 3**: Spawn COO with synthesis prompt (include all outputs). Save as `synthesis.md`
5. **Deliver**: Send synthesis to CEO via preferred channel (Telegram, Discord, etc.)

---

## Tips

- **Better topics = better brainstorms**: "Should we build X?" is better than "Tell me about X"
- **Add context**: Include market data, customer feedback, or constraints in the prompt for richer debate
- **Vary participants**: Not every brainstorm needs all agents. A CTO+CRO debate on pricing is perfectly valid
- **Run async**: Agents don't need to wait for each other in Round 1. Spawn them in parallel
- **Archive everything**: Brainstorm archives become your institutional memory
