# ⚡ FleetKit Quick Start — 5 Minutes to Your First Brainstorm

---

## Prerequisites

- [OpenClaw](https://openclaw.com) installed and running
- An API key for your preferred LLM (Claude, GPT, Gemini, etc.)
- A delivery channel set up (Telegram, Discord, Slack) — optional but recommended

---

## Step 1: Copy FleetKit to Your Workspace

```bash
# Clone the repo (or download and unzip)
git clone https://github.com/apocys/fleetkit.git

# Copy into your OpenClaw workspace
cp -r fleetkit/ ~/.openclaw/workspace/fleetkit/
```

That's it. FleetKit is just files — SOUL.md personalities, workflow protocols, and config. No dependencies, no build step, no Docker.

---

## Step 2: Customize (Optional)

### Edit the config
Open `fleetkit.yaml` and adjust:
- **Model**: Change `claude-sonnet-4` to whatever model you're using
- **Timezone**: Set your local timezone
- **Delivery**: Set your preferred channel (telegram, discord, slack)

### Personalize the agents
Each agent lives in `agents/{role}/SOUL.md`. The default personalities are battle-tested and designed to disagree productively. But you can:
- Change their names
- Adjust their expertise areas
- Tweak their communication style
- Add domain-specific knowledge

### Pro tip
Start with the defaults. Run a brainstorm. *Then* customize based on what you want more or less of.

---

## Step 3: Run Your First Brainstorm

Open a chat with your OpenClaw agent and say:

```
Run a brainstorm using the FleetKit protocol.
Topic: "Should we launch a freemium tier or stay premium-only?"
```

Your agent will:
1. Read the brainstorm protocol from `workflows/brainstorm.md`
2. Spawn CRO, CTO, and CMO with their SOUL.md personalities
3. Run 3 rounds: Positions → Debate → Synthesis
4. Deliver the COO's synthesis to you

**Expected time**: 2-5 minutes  
**Expected cost**: ~$0.80-1.50 (depends on model)

---

## Step 4: Set Up Daily Standups

Tell your OpenClaw agent:

```
Set up a daily standup using FleetKit.
Run it at 8 AM on weekdays. Deliver to Telegram.
```

Or use the cron config directly:

```bash
# Register the cron job with OpenClaw
openclaw cron add cron/morning-standup.json
```

Every morning, you'll get a synthesized brief from your AI executive team — what's happening, what needs attention, and what to decide.

---

## Step 5: Check the Dashboard

Open `dashboard/index.html` in your browser to see your fleet's activity at a glance.

```bash
open dashboard/index.html
```

---

## What's Next?

- **Run a few brainstorms** on real decisions you're facing
- **Populate MEMORY.md** for each agent — the more context they have, the better their output
- **Try the decision protocol** when a brainstorm surfaces disagreements
- **Add new agents** — create a new directory in `agents/` with a SOUL.md
- **Explore premium SOUL packs** for specialized agent personalities (sales, engineering, product, legal, etc.)

---

## Common Commands

| What you want | What to say |
|---|---|
| Run a brainstorm | "Brainstorm: {topic}" |
| Run today's standup | "Run standup" |
| Ask a specific agent | "Ask CRO: what's our pricing strategy?" |
| Check fleet status | "Fleet status" |
| Review a past brainstorm | "Show me the brainstorm on {topic}" |

---

## Troubleshooting

**Agents give generic responses?**
→ Their SOUL.md files are too generic. Add domain-specific expertise and context to make them sharper.

**All agents agree on everything?**
→ Good brainstorms need tension. Make the SOUL personalities more opinionated. Give them things to disagree about.

**Outputs are too long/short?**
→ Adjust `max_tokens` in `fleetkit.yaml` or add word limits to the workflow prompts.

**Costs too high?**
→ Use cheaper models for individual agents (e.g., Haiku) and reserve expensive models (e.g., Opus) for COO synthesis only.

---

## Need Help?

- 📖 [Full documentation](https://github.com/apocys/fleetkit/wiki)
- 💬 [Discord community](https://discord.gg/openclaw)
- 🐛 [Report issues](https://github.com/apocys/fleetkit/issues)
