---
name: comm-audit
description: Audit public or press communication about AI safety research against its primary technical sources. Use for a single explainer, release, thread, post, demo, headline, visual, or a comparative corpus audit when checking claim fidelity, capability versus propensity versus misuse uplift, elicitation conditions, numbers and uncertainty, caveats, anthropomorphism, related work, independence, licensing, dual-use safety, accessibility, and publication readiness.
---

# Audit AI Safety Communication

Evaluate whether an artifact is accurate, scoped, transparent, safe, and useful without rewarding blandness. Preserve strong explanations, structure, imagery, and audience choices when they do not distort the evidence.

## Required inputs

Obtain:

- the artifact or corpus, including headline, captions, visuals, metadata, and short-form derivatives;
- authoritative primary source versions and supplements;
- intended audience, communication goal, channel, date, and word/format constraints;
- the approved claim ledger when another `comm-*` skill produced one;
- relevant related work, corrections, funding/conflicts, and license information when available.

If a main source is inaccessible or its version is uncertain, continue only as a provisional audit and label every affected conclusion `unverified`.

Always read [references/audit-criteria.md](references/audit-criteria.md). Use [assets/audit-report-template.md](assets/audit-report-template.md) for the report.

## Workflow

### 1. Freeze the audit record

Record exact artifact and source URLs/files, titles, publishers/authors, dates, versions, status, and access time. Separate originals, updates, corrections, syndications, and adaptations. Do not audit a search snippet as if it were the artifact.

### 2. Reconstruct the claims

Extract every headline or main takeaway plus any sentence, number, visual, quote, or interaction that could materially change a reader's belief. Map each to:

- its source anchor;
- claim class;
- evidence and comparison;
- model/task/population and evaluation or deployment conditions;
- exact quantitative context;
- scope and caveats;
- whether it is reported, derived, contextual, disputed, speculative, or normative.

Compare this map with any approved ledger. Treat a new unsourced claim in the artifact as a finding, not an automatic ledger update.

### 3. Audit each artifact

Apply every relevant criterion. Mark each item:

- `pass` — supported and appropriately framed;
- `partial` — substantially right but missing a meaningful qualifier or context;
- `fail` — false, materially overstated, misleading, or unsafe;
- `unverified` — evidence needed but unavailable;
- `not applicable` — explain briefly when non-obvious.

Assign severity to non-passing findings:

- **Blocker:** could materially invert the takeaway, create a safety/rights problem, or make publication irresponsible.
- **Major:** likely to leave a typical reader with a materially broader or stronger belief.
- **Moderate:** meaningful loss of context, precision, independence, or usability.
- **Minor:** local wording, clarity, or documentation issue unlikely to change the core takeaway.

For each finding, quote or identify the smallest necessary artifact fragment, cite the source anchor, explain the reader-level consequence, and propose a scoped correction. Do not rewrite more than needed.

### 4. Audit the communication as communication

Identify what works: opening, pacing, concrete examples, analogies, questions, visuals, narrative, explanation order, voice, platform fit, and audience respect. A vivid or simple sentence is not hype merely because it is memorable. Preserve good language when the evidence survives the compression.

Check whether the artifact helps the intended audience state the main finding, conditions, largest limitation, and non-finding. Distinguish factual misunderstanding from value disagreement.

### 5. Compare a corpus consistently

For multiple artifacts, use one coding frame and one authoritative claim ledger. Record primary versus syndicated coverage and do not double-count copied text. Produce:

- a coverage inventory with inclusion/exclusion notes;
- an artifact-by-criterion matrix;
- recurring strengths and failure modes;
- differences by genre, outlet, and proximity to the research team;
- language or structural patterns worth learning;
- a scoped completeness statement describing search dates, queries, languages, databases, and known blind spots.

Do not claim to have found “all coverage” without a defined search universe. Say “all coverage located under the documented protocol” and list likely omissions.

### 6. Decide readiness

Issue one result:

- **Ready:** no unresolved blocker or major finding; material moderate findings repaired or consciously accepted.
- **Ready with disclosed limitations:** no blocker; unresolved issues are visible and do not overturn the main takeaway.
- **Not ready:** any unresolved blocker, material source/version uncertainty, safety/rights failure, or missing human claim approval when the originating authoring workflow or publication process requires that approval. A retrospective third-party audit does not require retroactive author approval; it must instead disclose source/access uncertainty and the auditor's role.

An audit is advisory evidence, not a substitute for author, subject-matter, security, legal, accessibility, or platform approval.

## Output

Deliver:

1. scope, source/version record, and readiness decision;
2. concise claim-to-source matrix;
3. prioritized findings with evidence and minimal corrections;
4. completed checklist;
5. communication strengths worth retaining;
6. unresolved questions and required human approvals;
7. for corpora, inventory, coding matrix, aggregate patterns, and completeness limits.

Never call an artifact source-verified when a main claim remains `unverified`.
