# Brainstorm Protocol — 3-Round Structured Debate

Multi-agent brainstorm that produces strategic insight through structured disagreement.

---

## Overview

| | |
|---|---|
| **Participants** | CRO, CTO, CMO (+ COO as synthesizer) |
| **Rounds** | 3 |
| **Estimated tokens** | ~25-35K total |
| **Estimated cost** | ~$0.15-0.50 (model-dependent) |
| **Output** | Synthesis doc with consensus, tensions, and recommendation |

---

## How to Run (OpenClaw)

Tell your OpenClaw main agent:

> "Run a brainstorm on: **{YOUR TOPIC}**. Use the FleetKit protocol in `fleetkit/workflows/brainstorm.md`."

Or trigger it manually by spawning each agent as a sub-session. Here's the exact flow:

---

## Round 1: Opening Positions

Spawn CRO, CTO, and CMO in parallel. Each gets their SOUL.md + the topic.

### How to Spawn (OpenClaw sessions_spawn)

For each agent (CRO, CTO, CMO), use OpenClaw's `sessions_spawn` tool:

```
Task: "You are {AGENT_NAME}, {TITLE}.

[Paste contents of fleetkit/agents/{agent}/SOUL.md here]

--- BRAINSTORM ---
Topic: {YOUR_TOPIC}

State your position in 200-300 words:
1. Your take (specific, opinionated)
2. Opportunities from your domain
3. Risks your role flags
4. Recommended action

Be direct. Disagree with likely positions of other agents."

Model: sonnet (or your preferred model)
Label: brainstorm-{agent}-r1
```

Collect all 3 responses.

---

## Round 2: Debate & Challenge

Spawn the same 3 agents again, this time with Round 1 results as context.

```
Task: "You are {AGENT_NAME}, {TITLE}.

[SOUL.md contents]

--- BRAINSTORM ROUND 2 ---
Topic: {YOUR_TOPIC}

Round 1 positions:
{PASTE ALL 3 ROUND 1 RESPONSES}

Respond in 200-400 words:
1. Which positions do you DISAGREE with? Name the agent, quote the point, explain why.
2. Which do you agree with? Build on them.
3. Has reading others changed your view? Why or why not?"

Model: sonnet
Label: brainstorm-{agent}-r2
```

---

## Round 3: Synthesis (COO Only)

Spawn the COO with all Round 1 + Round 2 outputs.

```
Task: "You are the COO.

[COO SOUL.md contents]

--- BRAINSTORM SYNTHESIS ---
Topic: {YOUR_TOPIC}

Round 1 positions:
{ALL ROUND 1}

Round 2 debate:
{ALL ROUND 2}

Write an Executive Brief (300-500 words):
1. Consensus — where do agents agree?
2. Key tensions — where do they disagree, and why?
3. Each agent's final position (one line each)
4. Your recommendation — what should the CEO do?
5. Decision needed — frame the specific choice."

Model: opus (or sonnet for budget)
Label: brainstorm-synthesis
```

---

## Automation via Cron

To schedule regular brainstorms, create an OpenClaw cron job:

```json
{
  "name": "Weekly Strategy Brainstorm",
  "schedule": {"kind": "cron", "expr": "0 10 * * 1", "tz": "Europe/Paris"},
  "sessionTarget": "isolated",
  "payload": {
    "kind": "agentTurn",
    "message": "Run a brainstorm using the FleetKit protocol. Topic: [YOUR WEEKLY TOPIC]. Spawn CRO, CTO, CMO for Round 1-2, then COO for synthesis. Deliver results to me.",
    "model": "claude-sonnet-4"
  }
}
```

---

## Tips

- **Better topics = better debates.** "Should we go freemium?" beats "discuss pricing."
- **Add context.** Include market data, competitor info, or constraints in the topic prompt.
- **Parallel spawning.** Round 1 and Round 2 agents can run simultaneously — saves time.
- **Cost control.** Use Sonnet for R1/R2, Opus only for synthesis if budget matters.
- **Save transcripts.** Store results in `brainstorms/{topic}/round-1.md` etc. for reference.
