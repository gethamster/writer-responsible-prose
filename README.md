# writer-responsible-prose

Agent skill that stops a model from writing in Hindi/Indo-Aryan topic-comment cadence and LLM caption sentences.

American written English names its noun and subordinates the label. Hindi and other Indo-Aryan languages mark given vs new information by position and by dropping recoverable nouns, and Indian English inherited that information structure. LLMs independently learned a cousin of it because "declare, then relabel" looks like clarity, and the combination is the official, academic, off cadence this skill kills.

A register converter, not a verdict on Indian English as a variety. The skill files themselves have to follow the rules.

## Install

Copy the folder into the skills directory your agent reads.

```
writer-responsible-prose/
├── SKILL.md
└── references/
    ├── why.md
    ├── patterns.md
    └── office-lexicon.md
```

- Claude Code — `~/.claude/skills/writer-responsible-prose/`
- Codex — `~/.codex/skills/writer-responsible-prose/`
- Cursor — `.cursor/skills/writer-responsible-prose/`
- Gemini CLI — `~/.gemini/skills/writer-responsible-prose/`
- Grok — `/home/workdir/.grok/skills/writer-responsible-prose/`

## What it bans

- `X. That is Y.` captions after a period
- `X is what Y` / `X is how Y` / `That's what Y` clefts
- Staccato stacks of short `NP is NP` sentences
- Headless topics (`Spare moves around the day`)
- Prestige equatives (`The winning business case is…`)
- Nominalization relays (`…smooth utilization. Smoother utilization is how…`)
- Unsolicited qualifying statements (`X happens. Y does not mean X.`)
- Office leftovers (`kindly`, `revert`, `do the needful`, `the same`)

## What it does instead

Fold the label into the fact, repeat the noun, put consequences in *which* / *so* / *because*, and use concrete subjects. Write statements in the affirmative, expressing conditions directly and giving each sentence a distinct fact.

## License

MIT
