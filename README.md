<p align="center">
  <img src="https://img.shields.io/badge/agents-5-blue" alt="5 Agents">
  <img src="https://img.shields.io/badge/setup-5_minutes-green" alt="5 Min Setup">
  <img src="https://img.shields.io/badge/code_required-zero-orange" alt="Zero Code">
  <img src="https://img.shields.io/badge/license-MIT-lightgrey" alt="MIT License">
</p>

<h1 align="center">⚡ FleetKit</h1>

<p align="center">
  <strong>Get the strategic insight of a $2M executive team — for $1 per decision.<br>Your AI C-suite debates so you don't make $100K mistakes alone.</strong>
</p>

<p align="center">
  <a href="#quick-start">Quick Start</a> •
  <a href="#what-is-fleetkit">What Is It</a> •
  <a href="#see-it-in-action">Demo</a> •
  <a href="#features">Features</a> •
  <a href="#how-it-compares">Compare</a> •
  <a href="#premium-soul-packs">Premium</a>
</p>

---

<p align="center">
  <strong>🎬 Demo Coming Soon</strong><br>
  <em>Your AI executives debating pricing strategy — 4 perspectives, 1 synthesis, 5 minutes</em><br>
  <sub>Until the demo is ready, check out the <a href="examples/brainstorm-example.md">real brainstorm example →</a></sub>
</p>

---

## Quick Start — 5 Minutes to Your First Executive Debate

```bash
# 1. Clone FleetKit
git clone https://github.com/apocys/fleetkit.git

# 2. Copy to your OpenClaw workspace
cp -r fleetkit/ ~/.openclaw/workspace/fleetkit/

# 3. Tell your OpenClaw agent about FleetKit (via Telegram, Discord, etc.)
# "I've added FleetKit to my workspace at fleetkit/. Read fleetkit/workflows/brainstorm.md 
#  — this is how you run multi-agent brainstorms with my AI executive team."

# 4. Run your first brainstorm
# "Brainstorm using FleetKit: Should we price our product as freemium or premium-only?"
```

**That's it.** No code. No Docker. No dependencies. Just files and conversation.

In 2-5 minutes, your AI executives will debate, disagree, and deliver a synthesis with specific recommendations. Hunter (CRO) will push for revenue, Forge (CTO) will flag technical constraints, Echo (CMO) will focus on brand impact. Atlas (COO) will synthesize their debate into actionable strategy.

👉 **[Complete 5-minute setup guide →](QUICKSTART.md)**

---

## See What Happens

You ask: *"Should we price our SaaS at $29/mo or $99/mo?"*

> **💰 Hunter (CRO):** "$99. Period. Your current users already pay — they'll absorb the increase. $29 attracts tire-kickers who churn in month 2."
>
> **🔧 Forge (CTO):** "Hunter's ignoring infrastructure costs. At $29 we need 3x the users but our backend doesn't scale linearly. I'm with him on $99 — but for engineering reasons, not sales reasons."
>
> **📢 Echo (CMO):** "You're both wrong. $99 kills virality. Nobody screenshots a $99 invoice. $29/mo with a $299/year annual plan. The annual plan is the real product."
>
> **📊 Atlas (COO) — Synthesis:** "Consensus: not $29/mo. Tension: monthly vs annual. Recommendation: Launch at $99/mo with $499/year annual (58% savings). Test for 60 days, measure conversion. Echo runs a $29 experiment on a separate landing page."

**That argument took 4 minutes and cost $0.20.** Your last meeting about pricing took 2 hours and decided nothing.

---

## Before FleetKit vs After FleetKit

**BEFORE:** Tuesday's 3-hour meeting. Hunter wants to move fast. Sarah wants more data. Mike thinks it cheapens the brand. Nothing decided. Meeting rescheduled for Thursday.

**AFTER:** You ask FleetKit the same question. 5 minutes: four perspectives, genuine disagreement, a synthesis with specific next steps. Decision made. Tuesday afternoon freed up.

*This is what happens when your team argues efficiently.*

---

## What Is FleetKit?

FleetKit is an **open-source starter kit** for running multi-agent AI teams on [OpenClaw](https://openclaw.com).

Meet your AI C-suite. They argue about everything. That's the point:

- **5 AI executives** with distinct personalities that genuinely disagree
- **Workflows** for brainstorms, standups, and decision escalation
- **Protocols** that produce real insight, not AI slop
- **A dashboard** to see your fleet's activity

### What FleetKit is NOT

- ❌ Not a framework — it's a template. Fork it, edit it, make it yours.
- ❌ Not autonomous agents — your AI executives advise, YOU decide.
- ❌ Not a coding project — everything is configured through SOUL.md files and YAML.
- ❌ Not magic — it's structured prompting done right. The magic is in the personalities.

---

## The Team

| Agent | Role | Personality | Catchphrase |
|-------|------|-------------|-------------|
| 👑 **Chief** | CEO | Decisive, vision-driven, allergic to theater | *"Does this still matter in 5 years?"* |
| 📊 **Atlas** | COO | Meticulous, process-obsessed, evidence-first | *"Has this been documented?"* |
| 💰 **Hunter** | CRO | Aggressive, numbers-forward, speed-obsessed | *"What's the revenue impact?"* |
| 🔧 **Forge** | CTO | First-principles, optimization-obsessed, dry humor | *"Delete it. If nobody notices, it wasn't needed."* |
| 📢 **Echo** | CMO | Creative, provocative, empathetic, bold | *"Nobody cares about features. What's the feeling?"* |

They're designed to **disagree**. Hunter pushes for speed, Forge pushes back on technical debt. Echo wants bold branding, Atlas wants documented processes. The friction is the feature.

---

## See It In Action

Here's an excerpt from a real brainstorm on revenue strategy:

> **💰 Hunter (CRO):** Digital product packs — fastest path to $10K/mo. Developer market pays premium. Revenue by week 4. $5-15K/mo potential. *Focus everything here.*
>
> **🔧 Forge (CTO):** "Revenue by week 4" is aggressive bordering on delusional. Has Hunter actually mapped the funnel? Product → landing page → traffic → conversion → payment. That's 4 things that all need to work simultaneously.
>
> **📢 Echo (CMO):** *This is our iPhone moment.* Every customer becomes an influencer. 9/10 viral potential. The community becomes a self-reinforcing flywheel.
>
> **🔧 Forge:** "iPhone moment" is inspiring and zero percent actionable. Convert the vision into a spec and I'll build it in a week. Until then, it's poetry.
>
> **📊 Atlas (COO) — Synthesis:** Kill the SaaS idea (unanimous). Digital packs have the highest ceiling. Ship 5 packs in 2 weeks, launch on Product Hunt week 3. Revenue target: 150-350 sales/month = $4K-$25K.

**[See the full example →](examples/brainstorm-example.md)**

---

## Features

- 🧠 **5 Distinct Agent Personalities** — CEO, COO, CRO, CTO, CMO with unique decision frameworks
- 🔄 **3-Round Brainstorm Protocol** — Positions → Debate → Synthesis
- 📋 **Daily Standups** — Automated morning briefs delivered to Telegram/Discord
- ⚖️ **Decision Escalation** — Structured protocol for when agents disagree
- 📊 **Fleet Dashboard** — See agent activity, costs, and status at a glance
- ⏰ **Cron Jobs** — Ready-to-use configs for automated standups and retros
- 📝 **Memory System** — Agents build context over time through MEMORY.md files
- 🎛️ **Fully Configurable** — YAML config for models, temperatures, schedules, delivery
- 💰 **Cost Tracking** — Built-in budget alerts and per-operation cost estimates
- 🔌 **Zero Dependencies** — Just text files. No code, no Docker, no build step.

---

## How It Compares

| Feature | FleetKit | CrewAI | AutoGen | LangGraph |
|---------|----------|--------|---------|-----------|
| Setup time | **5 minutes** | 30+ minutes | 1+ hours | 2+ hours |
| Code required | **None** | Python | Python | Python |
| Agent personality | **Deep SOUL files** | Basic roles | Minimal | Minimal |
| Structured debate | **3-round protocol** | Sequential | Chat | Graph |
| Decision escalation | **Built-in** | Custom code | Custom code | Custom code |
| Daily standups | **Built-in** | Custom code | Custom code | Custom code |
| Dashboard | **Included** | Third-party | Third-party | Third-party |
| Cost per brainstorm | **~$1** | ~$2-5 | ~$3-8 | ~$2-5 |
| Learning curve | **Read a README** | Learn Python SDK | Learn Python SDK | Learn Python SDK |

**FleetKit's philosophy**: Configuration over code. You shouldn't need to be a programmer to run an AI team. Edit a SOUL.md file instead of writing a Python class.

---

## Project Structure

```
fleetkit/
├── README.md                  ← You are here
├── QUICKSTART.md              ← 5-minute setup guide
├── LICENSE                    ← MIT
├── fleetkit.yaml              ← Fleet configuration
│
├── agents/                    ← Your AI executive team
│   ├── ceo/
│   │   ├── SOUL.md            ← Personality & decision framework
│   │   ├── MEMORY.md          ← Long-term memory (grows over time)
│   │   └── TOOLS.md           ← Tool configuration
│   ├── coo/
│   ├── cto/
│   ├── cro/
│   └── cmo/
│
├── workflows/                 ← Operational protocols
│   ├── brainstorm.md          ← 3-round debate protocol
│   ├── standup.md             ← Daily sync format
│   └── decision.md            ← Escalation framework
│
├── cron/                      ← Automation configs
│   ├── morning-standup.json
│   └── weekly-retro.json
│
├── dashboard/                 ← Fleet activity dashboard
│   └── index.html
│
└── examples/                  ← Real output examples
    ├── brainstorm-example.md
    └── standup-example.md
```

---

## Customization

### Change an agent's personality

Edit `agents/{role}/SOUL.md`. Every word affects behavior:

```markdown
# Before (generic)
You are the CTO. You handle technical decisions.

# After (FleetKit-style)
You think in first principles. When someone says "this is how
it's done," your first question is "why?" and your second is
"what if we deleted that step entirely?" You'd rather delete
code than write it.
```

### Add a new agent

```bash
mkdir agents/cpo  # Chief Product Officer
```

Create `SOUL.md`, `MEMORY.md`, `TOOLS.md` in the new directory. Add the agent to `fleetkit.yaml`. Done.

### Swap models

In `fleetkit.yaml`, change `model` per agent. Use expensive models (Opus) for synthesis, cheap models (Haiku) for individual updates:

```yaml
agents:
  coo:
    model: "claude-opus-4"     # Heavy reasoning for synthesis
  cro:
    model: "claude-haiku"      # Fast, cheap for individual updates
```

---

## Premium SOUL Packs

FleetKit is **free and open source** (MIT). Use it, fork it, sell products built with it.

Want specialized, battle-tested agent personalities? **Premium SOUL packs** are available:

| Pack | Agents | Price | Best For |
|------|--------|-------|----------|
| 🚀 **Startup Founders** | CEO, CTO, Head of Growth, Product Lead, Designer | $79 | Early-stage founders making $100K decisions alone |
| 🏢 **Enterprise Suite** | CISO, VP Engineering, VP Sales, VP Product, Chief of Staff | $149 | Corporate strategists needing diverse perspectives |
| 🎨 **Creative Agency** | Creative Director, Copywriter, Strategist, Media Planner, Producer | $79 | Agencies and freelancers who need a team on demand |
| 📈 **Sales Machine** | VP Sales, SDR Lead, AE, Solutions Engineer, CS Lead | $99 | Revenue teams optimizing pipeline and positioning |
| ⚖️ **Legal & Compliance** | General Counsel, Compliance Officer, IP Specialist, Data Privacy, Contract Reviewer | $149 | Founders navigating legal decisions without $500/hr lawyers |

Each pack includes deeply crafted SOUL.md files with real decision frameworks, domain-specific MEMORY.md templates, and adapted workflow protocols.

**One avoided bad hire pays for every pack. One better pricing decision pays for a year of FleetKit.**

**[Browse packs →](https://fleetkit.lemonsqueezy.com)**

---

## Contributing

FleetKit is community-driven. We welcome:

- 🧠 **New SOUL.md personalities** — The more diverse, the better
- 🔄 **Workflow improvements** — Better brainstorm protocols, new workflow types
- 📊 **Dashboard features** — Charts, filters, real-time data
- 📝 **Documentation** — Guides, tutorials, translations
- 🐛 **Bug reports** — Found something off? Tell us.

### How to contribute

1. Fork the repo
2. Create your feature branch (`git checkout -b feature/amazing-soul`)
3. Commit your changes (`git commit -m 'Add amazing CPO soul'`)
4. Push to the branch (`git push origin feature/amazing-soul`)
5. Open a Pull Request

---

## FAQ

**Q: Does this work with GPT-4/Gemini/Llama?**  
A: Yes. FleetKit is model-agnostic. Change the `model` field in `fleetkit.yaml` to any model your OpenClaw instance supports.

**Q: How much does it cost to run?**  
A: With Sonnet: a brainstorm costs ~$0.15-0.25, a standup ~$0.10. With Opus: 3-4x more. A full day of fleet operations runs $0.50-2.00. If you use a flat-rate subscription (Claude Max) via a local proxy, the cost is effectively $0.

**Q: Can I add more than 5 agents?**  
A: Absolutely. Create a new directory in `agents/`, write a SOUL.md, and add it to the config. People run fleets of 10+.

**Q: Do agents remember things between sessions?**  
A: Yes, through MEMORY.md files. Populate them with context and agents get sharper over time.

**Q: Can I use this for my team/company?**  
A: Yes. MIT license. Use it however you want.

---

## Star History

If FleetKit saves you from one bad decision, it's worth a ⭐

[![Star History Chart](https://api.star-history.com/svg?repos=apocys/fleetkit&type=Date)](https://star-history.com/#apocys/fleetkit&Date)

---

## License

MIT — do whatever you want with it. See [LICENSE](LICENSE).

---

<p align="center">
  <strong>Built with ⚡ by the OpenClaw community</strong><br>
  <sub>Your AI executives are waiting. Give them something to argue about.</sub>
</p>
