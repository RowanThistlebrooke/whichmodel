# /whichmodel — should you use Opus or Fable?

A Claude Code command that sizes up a task and tells you whether to run it on
**Opus 4.8** (cheap) or **Fable 5** (strong, ~2x the cost) — so Fable is only
spent on the hard stuff. One file, no dependencies.

## Install (easiest — works on Mac, Windows, Linux)
Open Claude Code and paste this:

> Install the whichmodel command from github.com/RowanThistlebrooke/whichmodel into my ~/.claude/commands folder

Then restart Claude Code.

## Install (manual)
Copy `commands/whichmodel.md` into `~/.claude/commands/whichmodel.md`
(Windows: `%USERPROFILE%\.claude\commands\whichmodel.md`), then restart Claude Code.

## Use
```
/whichmodel add a streak counter to the goals tile
```
You get a difficulty read and a verdict. If it says Fable, run `/model fable`,
do the task, then `/model opus` to drop back to cheap.
Type `/usage` anytime to see your spend.
