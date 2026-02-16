# Daily Standup Protocol

A structured daily sync that gives the CEO a unified view of what's happening, what's planned, and what needs attention — without attending a meeting.

---

## Overview

| | |
|---|---|
| **Schedule** | Mon-Fri, 8:00 AM (configurable) |
| **Participants** | CRO, CTO, CMO |
| **Synthesizer** | COO |
| **Estimated tokens** | ~20-30K total |
| **Estimated cost** | ~$0.30-0.50 |
| **Output** | Unified standup report delivered to CEO |

---

## Step 1: Spawn Individual Updates

Spawn CRO, CTO, and CMO in parallel. Each gets the same prompt with their SOUL.md loaded.

### Spawn Prompt (per agent)

```
Daily standup — {DATE}

Read your SOUL.md and MEMORY.md. Answer from your role's perspective:

1. **Since last standup**: What happened in your domain? Key wins, completions, observations.
2. **Today's priorities**: What are you focused on? Be specific.
3. **Blockers & risks**: Anything slowing things down or threatening progress?
4. **CEO attention needed?**: Anything the CEO should know or decide on?

Keep it concise — 150-250 words. Use your emoji and title as header.
Lead with the most important thing. No fluff.
```

---

## Step 2: COO Synthesis

Once all updates are collected, spawn the COO to synthesize.

### Synthesis Prompt

```
Daily standup synthesis — {DATE}

Here are today's individual updates:

---
{PASTE ALL INDIVIDUAL UPDATES HERE}
---

Produce the unified standup report:

## Fleet Standup — {DATE}

### 🔑 Key Highlights
Top 3-5 things the CEO needs to know. One line each.

### Agent Updates
Include each agent's update (cleaned up if needed).

### 📋 Decisions Needed
List any items requiring CEO input. Number them. Include enough context to decide.

### 🎯 COO Recommendation
Your take on today's priorities and any cross-team coordination needed.

Keep the total report under 500 words. The CEO should be able to read this in 2 minutes.
```

---

## Step 3: Delivery

Send the synthesis to the CEO via their preferred channel.

### Telegram Format

```
📊 Fleet Standup — {DATE}

🔑 Key Highlights:
• {highlight 1}
• {highlight 2}
• {highlight 3}

💰 CRO: {one-line summary}
🔧 CTO: {one-line summary}
📢 CMO: {one-line summary}

📋 Decisions Needed:
1. {decision}
2. {decision}

🎯 Atlas recommends: {recommendation}

Full report: {link to standup file}
```

### Discord Format

Same content, wrapped in an embed or code block for readability.

---

## Output Structure

Save standup reports in:

```
standups/YYYY-MM-DD.md
```

---

## Automation with Cron

Set up a cron job to run the standup automatically:

```json
{
  "name": "morning-standup",
  "schedule": "0 8 * * 1-5",
  "timezone": "Europe/Paris",
  "task": "Run the daily standup protocol. Spawn CRO, CTO, CMO for updates, then COO for synthesis. Deliver to Telegram.",
  "model": "claude-sonnet-4",
  "channel": "telegram"
}
```

---

## Tips

- **Consistency > perfection**: A mediocre standup every day beats a perfect one occasionally
- **Memory matters**: Agents produce better standups when their MEMORY.md is populated with recent context
- **Weekend variant**: Consider a Monday "week ahead" format instead of the standard standup
- **Skip when nothing's happening**: If the fleet had no activity, COO can send a one-line "No updates" instead of faking a report
