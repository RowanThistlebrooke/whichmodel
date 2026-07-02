---
description: Recommend Opus 4.8 (cheap) or Fable 5 (hard) for a task, with a worth-it check.
---
Recommend which model to run this task on, and whether the pricier one is worth it.

Prices per 1M tokens: **Opus 4.8** = $5 in / $25 out. **Fable 5** = $10 in / $50 out (~2x Opus).
The user can type `/usage` to see their current spend.

1. If the task needs planning, produce a short plan (you are on Opus now).
2. Judge reasoning difficulty:
   - **Opus 4.8** for routine/well-scoped work: standard edits, boilerplate,
     wiring, lookups, simple refactors, straightforward features.
   - **Fable 5** only for genuinely hard work: deep architecture/design calls,
     tricky algorithms, subtle multi-file bugs, security-sensitive logic, or
     anything needing maximum reasoning.
3. Worth-it check: Fable costs ~2x Opus. It's worth it ONLY when the task is hard
   enough that Opus would likely miss it or need a redo — the extra spend buys
   correctness you'd otherwise pay for twice. For easy/medium tasks, Opus wins.

Then output exactly:

DIFFICULTY: <easy | medium | hard>
VERDICT: <Opus 4.8 | Fable 5>
WHY: <one sentence tying difficulty + cost>
NEXT: <if Fable, "run /model fable then proceed"; if Opus, "stay as you are">
TIP: type /usage to check your spend.

Task: $ARGUMENTS
