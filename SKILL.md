---
name: writer-responsible-prose
description: Write and edit English so it uses American writer-responsible information structure instead of Hindi or Indo-Aryan topic-comment cadence and LLM caption sentences. Use when drafting, editing, rewriting, or reviewing prose, bullets, emails, memos, product copy, or posts. Also use when the user mentions Indian English, topic-comment, staccato, that is, is what, captions after a period, headless bullets, anti-slop, American register, or asks to make writing sound American.
license: MIT
metadata:
  version: "1.4"
  type: writing
---

# Writer-Responsible Prose

American explanatory English names its noun and subordinates the label. Hindi and other Indo-Aryan languages hang given information out front as a topic, drop recoverable nouns, and put the comment in the next clause. Indian English inherited that information structure, and LLMs independently learned the same move because "declare, then relabel" looks like clarity to a reward model, so the two together produce a cadence Americans hear as official, academic, and off.

This skill converts into American written register without treating Indian English as broken.

These files must follow their own rules. Caption sentences, staccato equatives, and `is what` clefts are banned here too, except inside `Bad:` examples.

Read [references/why.md](references/why.md) if the substrate is unclear. Read [references/patterns.md](references/patterns.md) while rewriting. Read [references/office-lexicon.md](references/office-lexicon.md) for leftover office phrasing.

## Do

1. Fold the label into the fact with *which*, *so*, *and*, or an appositive. One sentence that does two jobs beats two sentences where the second names the first.
2. Repeat the noun. If a bullet cannot be pasted into a blank message and still parse, the noun is missing.
3. Put consequences in a subordinate clause hanging off the fact, not in a new sentence whose subject is a noun you just minted.
4. Give sentences concrete subjects (people, buyers, GPUs, hours, prices) rather than *the winning business case*, *smoother utilization*, or *price discovery*.
5. Prefer *because* / *so* / *which* over *is what* / *is how* / *is where*.

## Avoid qualifying statements

Write statements in the affirmative: say what happens, what applies, or what is required. Give each sentence a distinct fact that advances the reader's understanding. A claim followed by an unsolicited qualification (`X happens. Y does not mean X.`) makes the reader reconstruct an objection they never raised, and repeated use gives the copy a negative, argumentative tone.

Express useful conditions directly: name the evidence needed, the scope affected, or the process that produces the result. Remove qualifications that merely deny an imagined alternative. Preserve factual limits and uncertainty when rewriting; describe them affirmatively using the information supplied. Keep separate facts in separate sentences when that makes them easier to follow.

Bad: `Providers must sustain improvements in throughput and latency before earning higher performance grades. Recovery checks alone cannot improve a provider's performance grade.`

Good: `Providers must sustain improvements in throughput and latency before earning higher performance grades.`

See [the qualifying-statement patterns](references/patterns.md#7-avoid-qualifying-statements) for scope and validation examples.

## Do not

Ban these templates on sight and rewrite them rather than polishing them.

| Ban | Why it jars | Fix |
|---|---|---|
| `X. That is Y.` / `X. This is Y.` | Caption after a period, a reversed pseudo-cleft used as a reformulation. | Merge to `X, which is Y` / `X, Y` / `X, so Y`. |
| `X is what Y` / `X is how Y` / `X is where Y` / `That's what Y` | Specificational cleft that pretends to name an essence and usually adds nothing. | `X that Y` or `Y because X`. |
| Three short `NP is NP` sentences in a row | Parataxis / staccato burst, the LLM default punch. | Join two of them with *and*, *so*, or a semicolon. |
| Bare topic as subject (`Spare moves…`, `Quiet hours clear…` with no noun) | Unlinked topic plus pro-drop from Indo-Aryan, which leaves the reader to supply the noun. | `Spare capacity moves…` |
| `The [abstract noun] is [definition].` | Copular equative with a prestige subject. | State the claim and drop the frame. |
| Next sentence starts with a nominalization stripped from the last one | Relay race of abstractions. | Use *which* / *so*, or keep a concrete subject. |

Also drop Indian-office leftovers. Full list in [references/office-lexicon.md](references/office-lexicon.md). Never write *kindly*, *revert* (for reply), *do the needful*, *the same*, *prepone*, *out of station*, *humble request*, *for your kind perusal*.

## Tiny examples

Bad: `In 75% of hours, at least 6% of peak tok/s is available to sell. That is incremental revenue on GPUs you already own.`

Good: `In 75% of hours you can sell at least 6% of peak tok/s, extra revenue from GPUs you already own.`

Bad: `A real market is what lets quiet hours clear.`

Good: `Quiet hours clear when a real market can match them to demand.`

Bad: `Spare moves around the day.`

Good: `Spare capacity moves around during the day.`

Bad: `The winning business case is tokens delivered at a latency. That is what buyers pay for.`

Good: `Buyers pay for tokens delivered at a latency.`

Bad: `A liquid spot market lets price discovery smooth utilization. Smoother utilization is how the next cluster gets cheaper to finance.`

Good: `A liquid spot market lets prices clear unused hours, which smooths utilization and makes the next cluster cheaper to finance.`

More pairs in [references/patterns.md](references/patterns.md).

## Preflight

Before sending any draft, scan once:

- Does a statement answer an objection the reader never raised? State the useful condition affirmatively or remove the qualification.
- Any sentence start with *That is* / *This is* / *That's what* / *This is what*? Merge it.
- Any *is what* / *is how* / *is where* / *is when* / *is why*? Kill the cleft.
- Three short equatives in a row? Join two.
- Can each bullet stand alone? If not, restore the noun.
- Is the subject an abstract noun you just coined? Recast with a concrete subject.
- Any *kindly*, *revert*, *the same*, *do the needful*? Replace.
- Did you caption a sentence instead of subordinating? Fold.
- Did *this file* just do `Fact. Relabel.`? Merge that too.
- Does a sentence exist only to say what the last sentence was? Cut it or merge it.

If two sentences in a row are `Fact. Relabel.` you are still in topic-comment, so merge them.
