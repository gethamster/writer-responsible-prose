# Patterns to kill

Rewrite each block as a template rather than swapping adjectives.

## 1. Caption after a period

Template: `FACT. That is LABEL.` / `FACT. This is LABEL.`

If the next sentence only labels what you just said, merge it.

Bad: `In 75% of hours, at least 6% of your own peak tok/s is available to sell. That is incremental revenue on GPUs you already own.`

Good: `In 75% of hours you can sell at least 6% of peak tok/s, extra revenue from GPUs you already own.`

Also good: `In 75% of hours, at least 6% of peak tok/s is sitting idle, so the GPUs you already paid for throw off extra revenue.`

Test: delete the second sentence. If the only loss is a synonym, it was a caption, so merge.

## 2. Staccato equatives

Template: `A is B. C is D. E verbs F.`

Don't stack three short copular sentences without a hinge.

Bad: `List spare and committed-but-unused the way AWS Spot and GCP preemptible instances work. Power is the variable cost. Everything else is already paid. Clearing price turns those hours into margin.`

Good: `List spare and committed-but-unused the way AWS lists Spot and GCP lists preemptible. Power is the only variable cost; everything else is sunk, so a clearing price turns those hours into margin.`

Test: if three consecutive sentences are under ~12 words and two of them are `X is Y`, join two.

## 3. Headless topic

Template: adjective or clipped noun used as subject, heading expected to supply the rest.

Bad: `Spare moves around the day. Sell the quiet hours and keep the busy ones at full price.`

Good: `Spare capacity moves around during the day. Sell the quiet hours; keep the busy ones at full price.`

Bad: `Quiet hours clear.`

Good: `Quiet hours of spare capacity clear when someone will buy them.`

Test: paste the bullet into an empty message. If a stranger asks "spare what?", restore the noun.

## 4. Reversed pseudo-cleft

Template: `X is what Y` / `X is how Y` / `X is where Y` / `That is what Y` / `This is how Y`.

Bad: `An active book of upstream buyers beats selling only direct or through OpenRouter. A real market is what lets quiet hours clear.`

Good: `A book of upstream buyers beats selling only direct or through OpenRouter. Quiet hours clear when a real market can match them to demand.`

Also good: `A market that matches buyers to spare capacity beats being stuck with direct contracts or OpenRouter.`

Test: replace `is what` with `that` or `because`. If meaning holds, the cleft was theatre.

## 5. Prestige equative + follow-up cleft

Template: `The ABSTRACT is DEFINITION. That is what / where CLAUSE.`

Bad: `The winning business case is tokens delivered at a latency. That is what buyers pay for, and where spare shows up hour by hour. GPU-hours hide the mix and the time of day.`

Good: `Buyers pay for tokens delivered at a latency. Spare capacity shows up hour by hour; GPU-hours flatten the mix and the time of day.`

Do not "fix" this with a sales closer (`I can help you make a business case`); keep the claim and kill the frame.

Test: if the subject is *the opportunity / the key / the real value / the business case / the winning move*, drop the subject and start with the actor.

## 6. Nominalization relay

Template: sentence ends on an abstract noun, then the next sentence promotes that noun to subject and clefts it (`is how` / `is why` / `is what`).

Bad: `A liquid spot market raises revenue and lets price discovery smooth utilization. Smoother utilization is how the next cluster gets cheaper to finance.`

Good: `A liquid spot market raises revenue and lets prices clear unused hours, which smooths utilization and makes the next cluster cheaper to finance.`

Test: if sentence 2's subject is a noun phrase copied out of sentence 1, it is a relay, so use *which* or *so*.

## 7. Avoid qualifying statements

Template: `CLAIM. OTHER THING does not / cannot / need not imply CLAIM.`

Write in the affirmative and give each sentence a distinct purpose. Convert a useful qualification into a direct statement of the condition, scope, or process. Remove a qualification that only rebuts an imagined objection. Check the whole paragraph for repeated claim-and-rebuttal pairs, including qualifications introduced with *but*, *while*, or *not automatically*.

Bad: `Providers must sustain improvements in throughput and latency before earning higher performance grades. Recovery checks alone cannot improve a provider's performance grade.`

Good: `Providers must sustain improvements in throughput and latency before earning higher performance grades.`

Bad: `Restrictions apply to the affected GPU supply. A problem with one model need not make other models unavailable, while a shared credential problem can affect multiple connections. Incomplete or ambiguous evidence does not establish recovery.`

Good: `The market restricts GPU supply affected by a fault. A model-specific fault affects that model's supply; a shared credential fault can affect multiple connections. Confirming recovery requires complete, unambiguous evidence.`

Bad: `The market assigns serving-fidelity grades according to its evidence and validation requirements. Individual automated assessments and buyer reports do not automatically change fidelity grades.`

Good: `The market assigns serving-fidelity grades after validating serving evidence against its grading requirements.`

Test: what fact does the qualification add? If it supplies a necessary condition, state that condition directly. If it only denies an unasked alternative, cut it. Preserve the original level of certainty and every condition needed to understand or act on the claim.

## Merge rule

When in doubt:

```
Fact. That is label.
```

becomes

```
Fact, label.
Fact, which label.
Fact, so consequence.
```

Never:

```
Fact.
Label-as-new-sentence.
Essence-cleft.
Abstract-subject follow-up.
```
