<!-- 
  GitHub Topics (add via repo settings):
  ai-agents, multi-agent, llm, claude, openai, automation, no-code, 
  executive-team, brainstorm, ai-workflow, openclaw, prompt-engineering,
  soul-files, agent-framework, strategic-planning
-->

<p align="center">
<pre align="center">
    ███████╗██╗     ███████╗███████╗████████╗██╗  ██╗██╗████████╗
    ██╔════╝██║     ██╔════╝██╔════╝╚══██╔══╝██║ ██╔╝██║╚══██╔══╝
    █████╗  ██║     █████╗  █████╗     ██║   █████╔╝ ██║   ██║   
    ██╔══╝  ██║     ██╔══╝  ██╔══╝     ██║   ██╔═██╗ ██║   ██║   
    ██║     ███████╗███████╗███████╗   ██║   ██║  ██╗██║   ██║   
    ╚═╝     ╚══════╝╚══════╝╚══════╝   ╚═╝   ╚═╝  ╚═╝╚═╝   ╚═╝   
                 ⚡ AI Executive Team in a Box
</pre>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/agents-5-blue?style=flat-square" alt="5 Agents">
  <img src="https://img.shields.io/badge/setup-5_min-green?style=flat-square" alt="5 Min Setup">
  <img src="https://img.shields.io/badge/code-zero-orange?style=flat-square" alt="Zero Code">
  <img src="https://img.shields.io/badge/cost-%241%2Fbrainstorm-yellow?style=flat-square" alt="$1/brainstorm">
  <img src="https://img.shields.io/badge/license-MIT-lightgrey?style=flat-square" alt="MIT License">
</p>

<p align="center">
  <strong>5 AI executives. Brainstorms, standups, debates.<br>Zero code, 5-minute setup, ~$1 per session.</strong>
</p>

<p align="center">
  <a href="#-quick-start">Quick Start</a> •
  <a href="#-what-happens-when-you-run-a-brainstorm">See It Work</a> •
  <a href="#-the-team">Meet the Team</a> •
  <a href="#-how-it-compares">Compare</a> •
  <a href="#-premium-soul-packs">Premium Packs</a>
</p>

---

## What Is FleetKit?

FleetKit is an **open-source starter kit** for running multi-agent AI executive teams on [OpenClaw](https://openclaw.com).

Drop it in your workspace. Tell your AI to brainstorm a topic. Get a structured 3-round debate with genuine disagreement, real strategic insight, and a synthesized recommendation — in under 5 minutes.

**Not a framework.** Not a library. Not a coding project. Just text files — SOUL.md personalities, workflow protocols, and YAML config. Fork it, edit it, make it yours.

---

## 🚀 Quick Start

```bash
# 1. Clone
git clone https://github.com/apocys/fleetkit.git

# 2. Copy to your OpenClaw workspace
cp -r fleetkit/ ~/.openclaw/workspace/fleetkit/

# 3. Tell your agent:
"Run a brainstorm using FleetKit. Topic: Should we go freemium or stay premium?"
```

**That's it.** No Docker. No pip install. No dependencies. Just files.

👉 **[Full 5-minute setup guide →](QUICKSTART.md)**

---

## 🧠 What Happens When You Run a Brainstorm

You type one sentence. FleetKit runs a **3-round structured debate** with your AI executive team. Here's what that actually looks like:

### Round 1 — Opening Positions

Each executive argues their corner. No diplomacy, no balance — just raw perspective.

> **💰 Hunter (CRO):**
> Digital product packs — fastest path to $10K/mo. Developer market pays premium. Revenue by week 4. $5-15K/mo potential. *Focus everything here.*
>
> **🔧 Forge (CTO):**
> 3 days to working MVP. Simplest technically. Existing competitors have terrible UX — that's our gap. Ship the mobile app this week. Test with real users. Scale what works.
>
> **📢 Echo (CMO):**
> *This is our iPhone moment.* Every customer becomes an influencer. 9/10 viral potential. A transformation story beats a utility story every time.

### Round 2 — Debate & Challenge

The executives read each other's positions. Then they **fight**.

> **💰 Hunter → Forge:**
> "Ship a mobile app in 3 days" — technically impressive, totally irrelevant. Speed to build ≠ speed to revenue. Where are the first 100 paying users coming from?
>
> **🔧 Forge → Hunter:**
> "Revenue by week 4" is aggressive bordering on delusional. Product → landing page → traffic → conversion → payment. That's 4 things that all need to work simultaneously.
>
> **🔧 Forge → Echo:**
> "iPhone moment" is inspiring and zero percent actionable. Convert the vision into a spec and I'll build it in a week. Until then, it's poetry.
>
> **📢 Echo → Forge:**
> Don't pretend engineering precedes positioning. If we can't explain WHY someone should buy this in one sentence, no amount of technical excellence saves us.

### Round 3 — Synthesis

The COO reads everything and delivers a structured executive brief.

> **📊 Atlas (COO) — Executive Brief:**
>
> **Consensus:** Kill the SaaS idea (unanimous). Digital packs have the highest ceiling.
>
> **Key Tensions:**
> | Question | CRO | CTO | CMO |
> |---|---|---|---|
> | What ships first? | Packs + store | MVP packs only | Packs + community |
> | Launch strategy? | Paid ads | Just ship it | Big moment campaign |
> | Timeline to revenue? | Week 4 | Week 6-8 | Month 2 (but bigger) |
>
> **Recommendation:** Ship 5 packs in 2 weeks, launch on Product Hunt week 3. Revenue target: 150-350 sales/month = $4K-$25K.
>
> **CEO Decisions Needed:**
> 1. Which 5 packs ship in v1?
> 2. $29 entry / $79 premium, or different structure?
> 3. Product Hunt first, or soft-launch to validate?

**Total time:** ~4 minutes. **Total cost:** ~$1.

📄 **[See the full unedited output →](examples/brainstorm-example.md)**

---

## 👥 The Team

| | Agent | Role | Perspective | Catchphrase |
|---|-------|------|-------------|-------------|
| 👑 | **Chief** | CEO | Vision, long-term, decisive | *"Does this still matter in 5 years?"* |
| 📊 | **Atlas** | COO | Process, documentation, synthesis | *"Has this been documented?"* |
| 💰 | **Hunter** | CRO | Revenue, speed, market timing | *"What's the revenue impact?"* |
| 🔧 | **Forge** | CTO | First principles, optimization, dry humor | *"Delete it. If nobody notices, it wasn't needed."* |
| 📢 | **Echo** | CMO | Story, emotion, brand, provocation | *"Nobody cares about features. What's the feeling?"* |

They're designed to **disagree**. Hunter pushes for speed, Forge pushes back on technical debt. Echo wants bold branding, Atlas wants documented processes. The friction is the feature.

---

## ⚡ Features

- 🧠 **5 Distinct Personalities** — Deep SOUL.md files with unique decision frameworks, communication styles, and blind spots
- 🔄 **3-Round Brainstorm Protocol** — Positions → Debate → Synthesis (genuine disagreement, not theater)
- 📋 **Daily Standups** — Automated morning briefs delivered to Telegram/Discord/Slack
- ⚖️ **Decision Escalation** — Structured protocol when agents can't agree
- 📊 **Fleet Dashboard** — Dark-mode HTML dashboard for agent activity at a glance
- ⏰ **Cron Jobs** — Ready-to-use configs for standups and weekly retros
- 📝 **Memory System** — Agents build context over time through MEMORY.md files
- 🎛️ **YAML Config** — Models, temperatures, schedules, delivery — all in one file
- 💰 **~$1/brainstorm** — Cheaper than a coffee. Standups are ~$0.40.
- 🔌 **Zero Dependencies** — Just text files. Works with any LLM.

---

## 📊 How It Compares

| | FleetKit | CrewAI | AutoGen | LangGraph |
|---|---|---|---|---|
| **Setup** | 5 min | 30+ min | 1+ hr | 2+ hr |
| **Code required** | None | Python | Python | Python |
| **Agent depth** | Deep SOUL files | Basic roles | Minimal | Minimal |
| **Structured debate** | ✅ 3-round | Sequential | Chat | Graph |
| **Cost/brainstorm** | ~$1 | ~$2-5 | ~$3-8 | ~$2-5 |
| **Learning curve** | Read a README | Learn SDK | Learn SDK | Learn SDK |

**Philosophy**: Configuration over code. Edit a SOUL.md, don't write a Python class.

---

## 📁 Project Structure

```
fleetkit/
├── fleetkit.yaml              ← Fleet configuration (models, temps, schedules)
├── agents/                    ← Your AI executive team
│   ├── ceo/SOUL.md            ← Personality & decision framework
│   ├── coo/SOUL.md
│   ├── cto/SOUL.md
│   ├── cro/SOUL.md
│   └── cmo/SOUL.md
├── workflows/                 ← Operational protocols
│   ├── brainstorm.md          ← 3-round debate protocol
│   ├── standup.md             ← Daily sync format
│   └── decision.md            ← Escalation framework
├── cron/                      ← Automation configs
├── dashboard/                 ← Fleet activity dashboard
└── examples/                  ← Real output examples
```

---

## 🎛️ Customization

### Change a personality

Edit `agents/{role}/SOUL.md`. Every word affects behavior:

```markdown
# Before (generic)
You are the CTO. You handle technical decisions.

# After (FleetKit-style)
You think in first principles. When someone says "this is how it's
done," your first question is "why?" and your second is "what if we
deleted that step entirely?"
```

### Add a new agent

```bash
mkdir agents/cpo  # Chief Product Officer
# Create SOUL.md, MEMORY.md, TOOLS.md → add to fleetkit.yaml
```

### Swap models

```yaml
# In fleetkit.yaml — use expensive models for synthesis, cheap for updates
agents:
  coo:
    model: "claude-opus-4"     # Heavy reasoning
  cro:
    model: "claude-haiku"      # Fast and cheap
```

---

## 💎 Premium SOUL Packs

FleetKit is **free and open source** (MIT). Premium SOUL packs offer deeply crafted, battle-tested agent personalities for specific domains:

| Pack | Agents | Price |
|------|--------|-------|
| 🚀 **Startup** | CEO, CTO, Head of Growth, Product Lead, Designer | $29 |
| 🏢 **Enterprise** | CISO, VP Engineering, VP Sales, VP Product, Chief of Staff | $49 |
| 🎨 **Creative Agency** | Creative Director, Copywriter, Strategist, Media Planner, Producer | $39 |
| 📈 **Sales Machine** | VP Sales, SDR Lead, AE, Solutions Engineer, CS Lead | $39 |
| ⚖️ **Legal & Compliance** | General Counsel, Compliance, IP Specialist, Privacy, Contract Reviewer | $49 |

Each pack includes SOUL.md files, domain-specific MEMORY.md templates, and adapted workflows.

<!-- TODO: Replace with actual store URL -->
**[Browse packs →](https://fleetkit.lemonsqueezy.com)**

---

## 🤝 Contributing

We welcome contributions! See **[CONTRIBUTING.md](CONTRIBUTING.md)** for guidelines.

The best contributions:
- 🧠 New SOUL.md personalities
- 🔄 Workflow improvements  
- 📊 Dashboard features
- 📝 Documentation and translations

---

## ❓ FAQ

**Works with GPT-4/Gemini/Llama?** — Yes. Model-agnostic. Change `model` in fleetkit.yaml.

**How much does it cost?** — Standup: ~$0.40. Brainstorm: ~$1. Full day: ~$2-3.

**Can I add more agents?** — Yes. New directory + SOUL.md + config entry. People run fleets of 10+.

**Do agents remember things?** — Yes, through MEMORY.md. More context = sharper output.

---

## License

MIT — do whatever you want. See [LICENSE](LICENSE).

---

<!-- TODO: Replace with actual star history once repo is live -->
<!-- [![Star History Chart](https://api.star-history.com/svg?repos=apocys/fleetkit&type=Date)](https://star-history.com/#apocys/fleetkit&Date) -->

<p align="center">
  <sub>If FleetKit saves you from one bad decision, it's worth a ⭐</sub>
</p>

---

<p align="center">
  <strong>Built by <a href="https://github.com/apocys">@apocys</a></strong><br>
  <sub>Powered by <a href="https://openclaw.com">OpenClaw</a> · Your AI executives are waiting. Give them something to argue about.</sub>
</p>
