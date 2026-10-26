# writer-responsible-prose

Agent skill that stops a model from writing in Hindi/Indo-Aryan topic-comment cadence and LLM caption sentences.

American written English names its noun and subordinates the label. Hindi and other Indo-Aryan languages mark given vs new information by position and by dropping recoverable nouns, and Indian English inherited that information structure. LLMs independently learned a cousin of it because "declare, then relabel" looks like clarity, and the combination is the official, academic, off cadence this skill kills.

A register converter, not a verdict on any variety of English or the people who speak it. The skill targets a habit of information structure, which spreads through second-language English and office registers and which models then amplify. The skill files themselves have to follow the rules.

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

## Short form

If you do not want to install a skill, paste this into your local LLM rules, custom instructions, or system prompt. It carries the same bans in about a thousand characters, so it fits where a skill folder will not.

```text
Match American writer-responsible English across all prose, including chat replies, commit messages, PR descriptions, and comments. Name the actor and the action in a concrete subject, then subordinate labels and consequences using "which", "so", "and", or "because". Prefer a single clause carrying its own fact over a short sentence followed by an explanatory caption.

Avoid these outright:
- A short declarative followed immediately by "That is...", "This is...", or "That's what..."
- Equative clefts ("is what", "is how", "is where", "is why")
- Three short "X is Y" sentences in a row
- Opening a sentence with an abstract coined noun (e.g., "The winning case is...")
- Nominalization relays that begin a sentence with an abstraction stripped from the preceding clause

Drop archaic administrative boilerplate: kindly, revert (to mean reply), do the needful, the same, prepone, out of station, humble request, for your kind perusal.

This governs phrasing and sentence structure only. Do not slow down or add verification passes for it, and do not apply it to code, identifiers, log lines, or exact quotations.
```

In Conductor, this goes in `~/.conductor/settings.toml` under `[prompts]` as `general = "..."`. Everywhere else, it is a normal standing instruction.

The short form covers the bans and the affirmative rule. It leaves out the preflight scan, the pattern catalog with Bad/Good pairs, and the office-term replacement table, so install the skill when you want a deliberate rewrite pass rather than a background rule.

## License

MIT
