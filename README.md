# /whichmodel — should you use Opus or Fable?

A Claude Code command that sizes up a task and tells you whether to run it on
**Opus 4.8** (cheap) or **Fable 5** (strong, ~2x the cost) — so Fable is only
spent on the hard stuff. One file, no dependencies. Same on Mac, Windows, Linux.

## Install
Open Claude Code and paste this whole block, then press enter:

```
Create a file at ~/.claude/commands/whichmodel.md with exactly this content:
---
description: Recommend Opus 4.8 (cheap) or Fable 5 (hard) for a task, with a worth-it check.
---
Recommend which model to run this task on, and whether the pricier one is worth it.

Prices per 1M tokens: Opus 4.8 = $5 in / $25 out. Fable 5 = $10 in / $50 out (~2x Opus).
The user can type /usage to see their current spend.

1. If the task needs planning, produce a short plan (you are on Opus now).
2. Judge difficulty: Opus 4.8 for routine work (edits, boilerplate, wiring, simple refactors); Fable 5 only for genuinely hard work (deep architecture, tricky algorithms, subtle multi-file bugs, security-sensitive logic).
3. Worth-it: Fable is ~2x the cost, worth it only when the task is hard enough that Opus would likely miss it or need a redo.

Then output exactly:
DIFFICULTY: <easy | medium | hard>
VERDICT: <Opus 4.8 | Fable 5>
WHY: <one sentence>
NEXT: <if Fable, "run /model fable then proceed"; if Opus, "stay as you are">
TIP: type /usage to check your spend.

Task: $ARGUMENTS
```

Then restart Claude Code.

## Use
```
/whichmodel add a streak counter to the goals tile
```
You get a difficulty read and a verdict. If it says Fable, run `/model fable`,
do the task, then `/model opus` to drop back to cheap.
Type `/usage` anytime to see your spend.
