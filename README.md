# writer-responsible-prose

Agent skill that removes generated-text tells at every level, from information structure to word choice, built on one thesis: the same reward pressure that makes an LLM write `Fact. That is label.` also makes it write forced triplets, `serves as`, and `I hope this helps`.

American written English names its noun and subordinates the label. Many languages mark given vs new information by position and by dropping recoverable nouns, and second-language English and office registers carry that topic-comment structure into prose. LLMs independently learned a cousin of it because "declare, then relabel" looks like clarity, and the combination is the official, academic, off cadence this skill kills. Version 2.0 extends the same edit above the sentence (rhythm) and below it (diction and formatting), fully subsuming the [humanizer](https://github.com/blader/humanizer) skill, which is built on Wikipedia's ["Signs of AI writing"](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing).

A register converter, not a verdict on any variety of English or the people who speak it, and never a license to change what a text claims. The skill targets a habit of information structure, which spreads through second-language English and office registers and which models then amplify. The skill files themselves have to follow the rules.

## Install

Copy the folder into the skills directory your agent reads.

```
writer-responsible-prose/
├── SKILL.md
├── CHANGELOG.md
└── references/
    ├── why.md
    ├── patterns.md
    ├── rhythm.md
    ├── diction.md
    ├── artifacts.md
    ├── guardrails.md
    └── office-lexicon.md
```

- Claude Code — `~/.claude/skills/writer-responsible-prose/`
- Codex — `~/.codex/skills/writer-responsible-prose/`
- Cursor — `.cursor/skills/writer-responsible-prose/`
- Gemini CLI — `~/.gemini/skills/writer-responsible-prose/`
- Grok — `/home/workdir/.grok/skills/writer-responsible-prose/`

## What it covers

Structure (patterns.md):

- `X. That is Y.` captions after a period
- `X is what Y` / `That's what Y` clefts
- Staccato stacks of short `NP is NP` sentences
- Headless topics (`Spare moves around the day`)
- Prestige equatives and nominalization relays
- Passives and subjectless fragments (`No configuration file needed.`)
- Unsolicited qualifying statements (`X happens. Y does not mean X.`)

Rhythm (rhythm.md):

- Forced triplets, anaphora, escalation ladders
- Contrast scaffolding (`not X but Y`, `X used to be A. Now it's B.`)
- Punchline stacking and rows of dramatic fragments
- Colon-punch labels (`one goal: X`)
- Staged second-person vignettes
- Synonym cycling, repeated openings, meta copy, padding tails

Diction (diction.md):

- The vocabulary watch list (*delve*, *robust*, *testament*, *landscape*, *seamless*…)
- Fancy copulas (*serves as*, *boasts*), shallow *-ing* analysis
- Vague sources, qualifier stacking, filler frames, false ranges
- Fake alternatives, formulaic sayings, fake-candid openers

Artifacts (artifacts.md):

- Em and en dashes, decorative bold, emojis, title-case headings
- Chatbot leftovers, knowledge disclaimers, generic upbeat endings
- Stock "challenges and outlook" sections

Office lexicon (office-lexicon.md):

- *kindly*, *revert*, *do the needful*, *the same*, *prepone*, and friends

Guardrails (guardrails.md): keep every claim, never invent facts, match the writer's sample, and a false-positive list so human quirks survive the edit.

## What it does instead

Fold the label into the fact, repeat the noun, put consequences in *which* / *so* / *because*, use concrete subjects, and default to flat explanation with an emphasis budget of two or three engineered moments per longform piece. Write statements in the affirmative, expressing conditions directly and giving each sentence a distinct fact.

## Growing it

The skill improves by autopsy. When an edit catches a tell no rule names, the template gets added to the owning reference file with a `Bad:` / `Good:` pair and a test, guardrails get the counter-case, and the version bumps. See the growth protocol in SKILL.md and history in CHANGELOG.md.

## Credits

Humanizer patterns from [blader/humanizer](https://github.com/blader/humanizer) (MIT), itself based on Wikipedia's "Signs of AI writing," maintained by WikiProject AI Cleanup. Information-structure analysis draws on Lange (2012) on ICE-India.

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
