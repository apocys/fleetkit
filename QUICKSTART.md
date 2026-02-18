# ⚡ FleetKit Quick Start

Get your AI executive team running in 5 minutes.

---

## Prerequisites

- **OpenClaw** installed and running ([install guide](https://docs.openclaw.ai))
- An LLM provider configured (Claude, OpenAI, or any OpenAI-compatible API)
- A messaging channel connected (Telegram, Discord, etc.)

---

## Step 1: Copy FleetKit to Your Workspace

```bash
# Clone the repo
git clone https://github.com/apocys/fleetkit.git

# Copy to your OpenClaw workspace
cp -r fleetkit/ ~/.openclaw/workspace/fleetkit/
```

---

## Step 2: Tell Your Agent About FleetKit

Open a chat with your OpenClaw agent (via Telegram, Discord, etc.) and say:

> "I've added FleetKit to the workspace at `fleetkit/`. Read `fleetkit/workflows/brainstorm.md` — this is how you run multi-agent brainstorms. The agent personality files are in `fleetkit/agents/`. Use them when I ask for brainstorms or standups."

Your agent will read the files and understand the protocol. That's it — no config, no code.

---

## Step 3: Run Your First Brainstorm

Say to your agent:

> "Brainstorm: Should we price our product as freemium or premium-only?"

Your agent will:
1. Spawn 3 sub-agents (CRO, CTO, CMO) with their SOUL personalities
2. Collect Round 1 positions (each agent argues their corner)
3. Run Round 2 debate (agents challenge each other)
4. Have the COO synthesize into an Executive Brief
5. Deliver the result to you

**Expected time:** 2-5 minutes depending on your model speed.

### ✅ Success Signs

You'll know it's working when you see:
- **Different perspectives**: Hunter (CRO) wants speed, Forge (CTO) flags technical risks, Echo (CMO) focuses on brand perception
- **Genuine disagreement**: Agents should challenge each other's positions, not just agree
- **Executive synthesis**: Atlas (COO) provides a clear recommendation with consensus, tensions, and next steps
- **Real insight**: You get perspectives you hadn't considered, not generic advice

If all agents sound the same or just agree with each other, the SOUL.md files need more personality. Edit them to be more opinionated.

---

## Step 4: Run a Daily Standup (Optional)

Say to your agent:

> "Run a standup using FleetKit. Follow the protocol in `fleetkit/workflows/standup.md`."

Or set up a cron job for automatic daily standups:

```
/cron add
Name: Daily Fleet Standup
Schedule: 0 8 * * 1-5 (8 AM weekdays)
Model: sonnet
Task: "Run a standup using FleetKit protocol at fleetkit/workflows/standup.md. Spawn each agent, collect updates, have COO synthesize. Deliver the summary."
```

---

## Step 5: Customize Your Fleet

### Change agent personalities
Edit the `SOUL.md` files in `fleetkit/agents/{role}/`. Make them match your industry, style, and needs.

### Add memory
After a brainstorm, update `fleetkit/agents/{role}/MEMORY.md` with key decisions. Agents become smarter over time.

### Add agents
Create a new directory in `fleetkit/agents/` with `SOUL.md`, `MEMORY.md`, and `TOOLS.md`. Reference the new agent in your brainstorm prompts.

---

## What It Costs

FleetKit itself is free (MIT license). You pay only for LLM API calls:

| Operation | Tokens (approx) | Cost with Sonnet | Cost with Opus |
|-----------|-----------------|------------------|----------------|
| Brainstorm (3 rounds) | ~25-35K | ~$0.15-0.25 | ~$0.50-1.00 |
| Daily Standup | ~15-20K | ~$0.10-0.15 | ~$0.30-0.50 |

**Tip:** Use Sonnet for Round 1-2 and Opus only for synthesis to optimize cost.

If you use a flat-rate subscription (Claude Max, etc.) via a local proxy, the cost is effectively $0.

---

## Next Steps

- 📖 Read the [Brainstorm Protocol](workflows/brainstorm.md) for advanced options
- 📖 Read the [Standup Protocol](workflows/standup.md) for daily sync setup
- 📖 Read the [Decision Framework](workflows/decision.md) for escalation patterns
- 🎨 Browse [Premium SOUL Packs](https://fleetkit.lemonsqueezy.com) for industry-specific agents
- 💬 Join the [community](https://discord.gg/openclaw) for support and SOUL sharing

---

## ✅ Quick Setup Verification

Before your first brainstorm, verify everything is ready:

```bash
# Check that all required files exist
cd ~/.openclaw/workspace/fleetkit/
ls -la agents/ceo/SOUL.md agents/coo/SOUL.md agents/cro/SOUL.md agents/cto/SOUL.md agents/cmo/SOUL.md
ls -la workflows/brainstorm.md workflows/standup.md workflows/decision.md
ls -la fleetkit.yaml

# If any files are missing, re-run the copy step
```

---

## Troubleshooting

**"My agent doesn't know about FleetKit"**
→ Make sure you copied the files to your OpenClaw workspace directory. Tell your agent explicitly: "Read `fleetkit/workflows/brainstorm.md`."

**"Agents give generic responses"**
→ The SOUL.md files need to be rich and specific. Edit them to match your domain. More personality = better debates.

**"Brainstorm takes too long"**
→ Use a faster model (Sonnet, Haiku). Reduce word limits in prompts. Run agents in parallel.

**"I want more than 5 agents"**
→ Create new directories in `fleetkit/agents/`. Write a SOUL.md with a distinct personality and role. Reference them in your brainstorm prompts. There's no hard limit.

**"All agents agree with each other"**
→ Edit the SOUL.md files to be more opinionated and add more "What Annoys You" sections. Great debates come from productive friction, not consensus.
