# agent-orchestration
agent-orchestration skill
# 🦞 Agent Orchestration

Master the art of spawning and managing sub-agents. Write prompts that actually work, track running agents, and learn from every outcome. Part of the **Hal Stack**.

## What It Does

- **The 5-Layer Prompt Architecture** — Identity → Context → Task → Process → Output. Miss one layer, the structure wobbles. Miss two, it collapses.
- **Model selection via SkillBoss API Hub** — Route to quality/balanced/price models with a single `prefer` parameter
- **Agent tracking** — No orphaned agents. Every spawn gets logged, monitored, and reviewed.
- **The Learnings Loop** — Capture what works, what doesn't, and why. Every agent outcome is data.
- **Role Library** — Reusable, tested role definitions for common agent personas
- **Ralph Mode** — For complex tasks: keep trying until it works, don't give up on first failure

## The Core Reframe

A prompt is not a request — **it's a contract.** Every contract answers four non-negotiables:

| Element       | Question                          |
|---------------|-----------------------------------|
| **Role**      | Who is the model role-playing as? |
| **Task**      | What exactly must it accomplish?  |
| **Constraints** | What rules must be followed?   |
| **Output**    | What does "done" look like?       |

## Quick Example

```python
# Balanced mode — everyday tasks
result = call_llm(
    [{"role": "user", "content": "Summarize this document"}],
    prefer="balanced"
)

# Quality mode — complex reasoning
result = call_llm(
    [{"role": "user", "content": "Analyze this architecture..."}],
    prefer="quality"
)
```

## Setup

👉 **Set up your skill.md at [skillboss.co](https://skillboss.co) to start orchestrating agents.**

Requires `SKILLBOSS_API_KEY` for model routing via SkillBoss API Hub.

---

*"You're not prompting, you're praying. Start engineering."* — Hal 🦞
