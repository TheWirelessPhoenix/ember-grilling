# ember-grilling

An Agent Skill that interviews you one question at a time to stress-test a plan, design, or idea until every decision is settled, then writes a handoff file a fresh chat can act on.

Works in Claude Code and any agent that supports the open [Agent Skills](https://agentskills.io) format.

## What it does

1. Restates your goal in one sentence and lists the open decisions, ordered so that decisions other choices depend on come first.
2. Checks your code, docs, and files first, so it never asks what it can find out itself.
3. Asks **one numbered question per turn** (Q1, Q2, ...), each with a recommended answer. Reply "yes" to accept it.
4. Updates the plan after each answer, drops questions that no longer matter, and points out contradictions or risky assumptions.
5. Stops when nothing is left open, and writes `<topic>-decisions.md` with the goal, the decisions and reasons behind them, open risks, and the next step.

## Use it if

- you have a plan, feature, or idea that's still fuzzy
- you want someone to poke holes in a design before you build it
- you want a written record of decisions to hand to a fresh chat or a teammate

## Don't use it if

- the task is small and already clear. Just ask for it directly.
- you want answers fast without being asked questions.

## Install

**skills.sh (any compatible agent):**

```bash
npx skills add TheWirelessPhoenix/ember-grilling
```

**Claude Code plugin:**

```text
/plugin marketplace add TheWirelessPhoenix/ember-grilling
/plugin install ember-grilling@ember-grilling
```

**Manual:** copy `skills/ember-grilling/` into `~/.claude/skills/`, or into your agent's skills folder.

## Usage

Say "grill me on this plan", "stress-test this idea", or "help me think through ...", or run `/ember-grilling` (`/ember-grilling:ember-grilling` when installed as a plugin).

## License

MIT
