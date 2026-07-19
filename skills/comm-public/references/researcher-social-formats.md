# Researcher social and forum formats

Use this reference when the requested public package includes X/Twitter, Bluesky, Mastodon, LessWrong, Alignment Forum, a lab blog, or a similar researcher-facing channel. These formats are shorter or less formal than a paper, but they are not permission to weaken the evidence.

## One layered communication system

Treat channel outputs as linked layers rather than isolated summaries:

1. a 30–60 second social entry point;
2. a project page or three-minute public explanation;
3. a five-to-eight-minute researcher post;
4. the paper, supplement, data/code, and living update record.

Keep one approved claim ledger across every layer. Shorter layers may omit secondary detail, but must retain any condition that changes the main claim. Link downward to the evidence and upward to later corrections.

## X/Twitter and short threads

A useful thread sequence is:

1. one-sentence intervention and observed shift;
2. the exact evaluation frame and baseline;
3. one representative example, labeled for representativeness;
4. how the training or test was constructed and what was absent;
5. the strongest control and closest alternative explanation;
6. a clear unresolved question or mechanism uncertainty;
7. source, code/data/demo, related work, and update link.

Use one claim or figure per post. Pair a percentage with its denominator, comparison, uncertainty where available, and the conditions needed to interpret it. Put alt text on figures. A later post cannot repair a false first-post takeaway, so the opening must already distinguish a conditional evaluation result from ordinary use or deployment.

Prefer candid epistemic language—“we observed,” “the control suggests,” “we do not yet know”—over either institutional certainty or artificial suspense. Do not use a curated shocking output without its sampling frequency and selection status. Pin or link a dated correction when a new model, paper version, replication, or challenge changes the result.

Compact deliverable skeleton:

```text
Thread length / platform character limit:
1/N — intervention + observed shift + essential condition
2/N — exact result + baseline + uncertainty/selection status
3/N — representative example + representativeness label
4/N — method + strongest control
5/N — limitation + what is not shown
6/N — source, artifacts, related work, dated update link
Alt text for each figure:
```

## LessWrong, Alignment Forum, and researcher notes

Start with a compact orientation containing:

- the research question and main result;
- the most important number and baseline;
- the conditions that govern interpretation;
- the leading limitation and what the study does not establish;
- paper, code/data, and artifact links;
- epistemic and publication status.

Then provide enough detail for scrutiny: method, hyperparameters when consequential, uncertainty and seed/sample variation, controls, negative results, failed experiments, cost or access constraints, and version/API instability. Separate observations, author hypotheses, external interpretations, and open problems with explicit headings or labels.

An informal first-person voice is useful when it reveals uncertainty or research contingency. Label personal prioritization as personal, and distinguish discovery narrative from confirmatory evidence. Put actionable links at the point of use: repository beside reproduction instructions, appendix beside a caveat, issue tracker beside an open problem.

Compact deliverable skeleton:

```text
Title:
TL;DR:
Epistemic and publication status:
Question and main result:
Method and interpretation-changing conditions:
Results, baselines, and uncertainty:
Controls, negative results, and failed experiments:
Limitations and what is not shown:
Related work / replication / disagreement:
Paper, appendix, data/code, demo, and contact links:
Update and correction log:
```

## Language patterns

- Lead with `intervention → observed output shift → evaluation frame`, not a free-floating dramatic label.
- Follow every vivid example with frequency and representativeness.
- Put the strongest control beside the main claim.
- Include “what this does not show” before broad implications.
- Use plain-English labels first, then operational definitions.
- Preserve exact numbers and conditions in researcher-facing formats even when prose is conversational.
- End with released artifacts, concrete open questions, and a dated update/correction path.

Avoid turning output descriptions into mental-state claims. For example, prefer “produced anti-human statements in sampled responses” to “became anti-human,” and “the contextualized-training control suggests interaction framing mattered” to “the model understood the trainer's intent.”
